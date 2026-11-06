# Bead: bob-cli-hg.12.1 — Gmail compose, reply, draft, and confirmed send

[Bead Pages](../README.md) / [bob-cli-hg.12](bob-cli-hg.12.md) / bob-cli-hg.12.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.md) · **Assignee:** `bob-cli-hg.12.1.land`
**Created:** 2026-11-06 07:12:28 EST · **Closed:** 2026-11-06 16:28:33 EST
**Plan:** [202611/gmail\_compose.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_compose.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_compose.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_compose.md

<!-- sase:links:end -->

## Description

Complete bob-cli-hg.12 with editable compose/reply notes, exact draft previews, confirmed draft-id sends, crash recovery, and preserved sent notes.

## Notes

[2026-11-06T21:28:33Z · bob-cli-hg.12.1.land] Landing verified all six phases (2a37f8ce, ee05db4d, b6a96243, 8935148f, 57af3ead, ae624e27) against plan:202611/gmail_compose.md and parent 5.12: new/reply/reply-all with Notes-excluding source regions; conservative pulldown-cmark render with 10 typed refusals and flattened links; private 0700/0600 attachment and body staging; drafts create/update/get with --gmail-no-send plus exact allowlists, --reply-to-message-id threading verified on readback, in-memory MIME readback, versioned canonical digest; durable gmail_send state with draft-id-only drafts send and three-outcome recovery; TTY/non-TTY confirmation, in-place promotion, Reply removal, [!mail-sent] cards, idempotent body-free gmail.sent. No memory edits; DECISIONS honored. Landing fixes: removed the five intermediate module-wide #[allow(dead_code)] allowances in compose/mod.rs plus the now-consumed GmailConfig::signature allowance, resolving the 5 dead items they hid (attachments _dir field + test-only dir(), RenderRefusal kind()/line() removed, dispatch_once cfg(test), SendState::is_terminal removed). Closed acceptance-test gaps the compose-docs audit overstated: unit test canonical_digest_is_stable_and_binds_every_preview_field (every field incl. HTML-only, Bcc, signature, attachments, note) and CLI test html_only_and_remote_draft_edits_invalidate_confirmation (HTML-only edit -> confirmation_mismatch; Gmail-side draft edit -> draft_remote_conflict with no update/send); extended the promotion test to prove list indexes and save refreshes the promoted note in place. Integration with concurrent hg.7/hg.8/hg.14/hg.10: compose notes stay out of the saved-thread index until promotion; removed stale 'Dedicated task linking remains later work' from docs/gmail.md; added new/reply/draft/send to docs/reference/json-outputs.md (within its 6000-word cap) and linked compose JSON from gmail.md#json-output. Gates: just check rc=0; just docs-check all gates passed (447 passed, 1 skipped). Follow-ups: hg.12.1.1/.2/.3 README snapshot proposals -> already fixed by b6a96243 rebaseline, recorded as note on bob-cli-hs (no new task); hg.12.1.6 complete_themes flake -> +1 on bob-cli-g8 (same test, same 150 ms deadline root cause); stale 'coming in bob-mail' line in docs/guides/link-emails-to-tasks.md and other phases' stale gmail allowances -> DISCOVERED ISSUE note on active parent epic bob-cli-hg (caused by hg.8/hg.10 ordering, not this epic). epic-symbols: none.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.12.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.land/README.md) | [bob-cli-hg.12.1](bob-cli-hg.12.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f1d8285`](https://github.com/bobs-org/bob-cli/commit/f1d8285ef1be73aa036e001a17e6e39bc887db96) | fix(gmail): land compose epic without intermediate allowances | [bob-cli-hg.12.1](bob-cli-hg.12.1.md) | 2026-11-06 16:29:53 EST |
| bob-cli--plans | [`bob-cli--plans@1b20daf`](https://github.com/bobs-org/bob-cli--plans/commit/1b20daf288e8d98eb8463f44da4bd3b4d43ddd78) | chore(plans): mark gmail\_compose epic plan done | [bob-cli-hg.12.1](bob-cli-hg.12.1.md) | 2026-11-06 16:30:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.12.1.1][1] | Need final epic decisions governing this phase | 1 |
| read-by | [agent:bob-cli-hg.12.1.4][2] | Need epic scope and DECISIONS | 1 |
| read-by | [agent:bob-cli-hg.12.1.land][3] | Need the epic scope, children, and linked plan file | 1 |
| read-by | [agent:cq][4] | Understand compose child epic phase status (which parts landed) | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.land/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.cq/README.md

<!-- sase:referenced-by:end -->
