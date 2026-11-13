# Bead: bob-cli-kx.1 — Mutation-path spike

[Bead Pages](../README.md) / [bob-cli-kx](README.md) / bob-cli-kx.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bt](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bt.md) · **Assignee:** `bob-cli-kx.1` · **Size:** small
**Created:** 2026-11-12 11:11:53 EST · **Closed:** 2026-11-12 11:21:13 EST
**Plan:** [202611/gmail\_archive\_on\_task\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_on_task_close.md)

## Description

spike: De-risk the mutation path before any code lands: audit gog's HTTP retry behavior on the mutation path in the upstream checkout, verify the write-call flag fence composes, settle whether label:bob search matches messages labelled only bob/closed, and draft the honest gmail.modify consent copy. Findings land as phase-bead notes; anything that bends the core contract is flagged loudly.

## Notes

[2026-11-12T16:20:00Z · bob-cli-kx.1] SPIKE Q1 — gog retries batchModify at the transport layer, idempotent-safe. All Gmail API calls are built via tokenSourceClientOptions → readOnlyTransportFromContext(ctx, newAuthenticatedRetryTransport(...)) (internal/googleapi/client.go:233-246), so gmail batch modify (single BatchModify.Do, internal/cmd/gmail_batch.go:120-124) rides RetryTransport: up to 6 retries on 429/403-rate-limit with exp backoff from 1s, plus 1 retry on 5xx (retry_constants.go; transport.go:47-64,156-203). It does NOT opt out via WithoutRetries (only contacts-dedupe, sheets-write, drive-upload, generic batch_transport do). Label add+remove is idempotent, so a retried-after-timeout call converges to the same label set — no partial state. Core implication (no contract bend): call straight, journal gmail.archived ONLY on process success (exit 0 + parsed receipt), never before the call; a ultimately-failed call surfaces as a normal error and the thread stays eligible for the next run. invalid_grant aborts without retry (transport.go:123-142), matching the plan. Verified against gogcli @6f910fff; installed gog is v0.44.0, the plan floor.

[2026-11-12T16:20:18Z · bob-cli-kx.1] SPIKE Q2 — write-call flag fence composes; verified empirically on installed gog v0.44.0 (no account/network, dry-run only). `gog --no-input --json --color never --client bob-gmail --gmail-no-send --enable-commands-exact gmail.batch.modify --dry-run gmail batch modify MSGID123 --remove INBOX --add-label bob/closed` exits 0 and echoes op gmail.batch.modify with ids/add/remove (both --remove and literal --remove-label/--add-label spellings accepted, normalized in echo). Same allowlist blocks siblings: `gmail send` → `command "gmail send" is not enabled` usage error. Code basis: --gmail-no-send gates only send paths (gmail_no_send.go:12-22 map; batch.modify not listed) so keeping it is harmless; --readonly is enforced at the HTTP transport (googleapi/read_only.go blocks the batchModify POST) so omitting it is exactly what opens the write — the same shape as bob draft_write_flags (src/native/gmail/gog.rs:383-388, keeps --gmail-no-send, omits --readonly). Core implication: the plan argv works verbatim; fake-gog argv assertions must pin --gmail-no-send present, --readonly absent, --enable-commands-exact gmail.batch.modify.

[2026-11-12T16:20:35Z · bob-cli-kx.1] SPIKE Q3 — label:bob does NOT match bob/closed-only mail (docs consensus; live check deferred). Gmail nesting is display-only: mailsweeper ("Opening or searching the parent does not list mail that only has a child label"), an 18-year-mailbox writeup ("Mail tagged Family/Extended will not show up when you click Family"), and a GAS maintainer ("when searching a label Gmail does not automatically include its descendants") all agree parent label: search excludes child-only mail. Could NOT live-verify on athena: the only grant here is the bob-gcal OAuth client, which has no Gmail scopes (gmail labels list / gmail search label:bob → 403 insufficientPermissions). No mutation attempted. TRY-IT FOR BRYAN (30s, Mac writer holds the Gmail grant): label one test message bob/closed only, compare `label:bob` vs `label:bob/closed` in the Gmail search box — expect the parent query to exclude it. Core implication if docs hold (expected): no discovery filter needed. LOUD CONDITIONAL: if the try-it ever shows leakage, core MUST filter receipt-labelled threads out of discovery explicitly, or archived threads re-enter discovery forever and the one-shot journal fold misfires.

[2026-11-12T16:20:51Z · bob-cli-kx.1] SPIKE Q4 — draft gmail.modify consent copy for `bob gmail login -s modify` (style matches login.rs/cli.rs: short scope word + parenthetical honesty, cf. "compose (also permits sending)"). Proposed login-step line: `modify — archive-only: Bob may remove INBOX from and add one receipt label (bob/closed) to messages it already saved, after all linking tasks close. It never trashes, deletes, marks read/unread, stars, or sends; sending still needs -s compose and its own confirmation.` Proposed -s help: `OAuth scope: readonly, compose (also permits sending), or modify (archive-on-close only: remove INBOX + add receipt label on saved messages)`. Rationale line for docs/gmail.md: Google consent screen describes gmail.modify in broad read/compose/send/delete terms; Bob requests it on the isolated bob-gmail client, gates every write behind --enable-commands-exact gmail.batch.modify, and the only expressible mutation is the INBOX+receipt label pair. Core owns final wording + the setup-error hint when archive:on meets a modify-less grant (exit 2).

[2026-11-12T16:21:13Z · bob-cli-kx.1] Spike done, no repo changes (plan forbids them for this phase). Q1: batchModify rides gog RetryTransport (6x rate-limit + 1x 5xx retries), idempotent, journal-on-success-only. Q2: flag fence verified live on gog v0.44.0 dry-run (exact allowlist + no-send composes, send blocked, readonly-omission opens the write). Q3: label:bob excludes bob/closed-only mail per 3+ independent docs; athena has no Gmail scopes so live confirm is a 30s Mac try-it recorded on the bead. Q4: modify consent copy drafted. No contract bends; one loud conditional (receipt discovery filter) if the try-it ever contradicts docs.

## Dependencies

- **Blocks:** [bob-cli-kx.2](bob-cli-kx.2.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.1/README.md) | [bob-cli-kx.1](bob-cli-kx.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.4][1] | Need the recorded gog v0.44 batch-modify and label-create transport findings before implementing the assigned adapter | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.4/README.md

<!-- sase:referenced-by:end -->
