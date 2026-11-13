# Bead: bob-cli-kx.3.1 — Gmail archive receipts and explicit undo

[Bead Pages](../README.md) / [bob-cli-kx.3](bob-cli-kx.3.md) / bob-cli-kx.3.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.md) · **Assignee:** `bob-cli-kx.3.1.land`
**Created:** 2026-11-13 08:02:46 EST
**Plan:** [202611/gmail\_archive\_receipts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_receipts.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_archive_receipts.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_receipts.md

<!-- sase:links:end -->

## Description

Complete bob-cli-kx.3 with safe explicit unarchive, durable mail receipts, desktop notifications, task chips, and morning notices.

## Notes

[2026-11-13T19:39:05Z · bob-cli-kx.3.1.land] LAND FOLLOW-UP TRIAGE (bob-cli-kx.3.1.land): (1) 3.1.1 #1 lychee docs/gcal-notes.md link -> duplicate, +1 bob-cli-l7. (2) 3.1.2 #1 / 3.1.3 #1 / 3.1.4 #2 / 3.1.6 #1 word budgets -> bob-ledger-tools.md is a duplicate (+1 bob-cli-il, 6115/6000) and bob-navigation-hotkeys.md is a duplicate (+1 bob-cli-jz, 6021/6000). The json-outputs.md overrun from 3.1.4 #2 no longer reproduces (docs-check reports only the two plugin pages), so it was declined. (3) 3.1.4 #1 clippy deny-errors in unarchive.rs -> declined as a follow-up because this epic caused it; the lander fixed it (needless_borrow x4, useless_conversion) along with a collapsible_if in tests/gmail_support/mod.rs from 3.1.4. (4) 3.1.6 #1 timing flakes -> already tracked by bob-cli-io, bob-cli-km, and bob-cli-ej; this landing also saw and +1'd bob-cli-ju, bob-cli-ki, bob-cli-kl, and bob-cli-l2 (gcal sync_args failure). No new task beads were created.

[2026-11-13T19:47:25Z · bob-cli-kx.3.1.land] LAND AUDIT (bob-cli-kx.3.1.land): Verified that phases 3.1.1-3.1.6 landed (bob-cli c994cfbd 59b6149a 2ddfc944 cd6aefae 01ab0767; bob-plugins b519508 e102fe2). Projection, receipts, unarchive, notify, banner, and chips match the plan contracts. No unrelated post-start commit touches Gmail. Landing fixes made: clippy deny-errors (unarchive.rs, tests/gmail_support/mod.rs); a catalog Excluded row for gmail unarchive (fixed public_leaves_are_entries_or_excluded); and the bob-mail Move-back argv bug. The old argv '-- NOTE -f json' parsed -f/json as extra operands and returned human text; it is now '-f json -- NOTE', with a pin test in gmail/cli.rs, rebuilt and deployed via the documented clean-then-dirty bob plugins sync (no -F). Gates: just check passes except the tracked bob-cli-l2 and bob-cli-kl; just docs-gen is clean; docs-check fails only on the bob-cli-il and bob-cli-jz budgets; lychee shows only bob-cli-l7; bob-plugins validate passes and npm test passes except load flakes bob-cli-ju and bob-cli-ki. Remaining work, planned as a tale: the plan's unarchive fault/fence tests (wrong writer, missing scope, partial failure, journal-append failure, stale ownership, invalid_grant, policy, identity, unsafe journal), the complete-flow tests, the reopen hint still saying restore is manual-only, the receipts acceptance matrix, and the closeout of bob-cli-kx.3.1 and then phase bob-cli-kx.3.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.land/README.md) | [bob-cli-kx.3.1](bob-cli-kx.3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e245e46`](https://github.com/bobs-org/bob-cli/commit/e245e46281291c02ff3fa93984b1f0ea59b0fd4a) | fix(gmail): land archive receipt integration fixes | [bob-cli-kx.3.1](bob-cli-kx.3.1.md) | 2026-11-13 14:48:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.3.1.2][1] | Need child epic DECISIONS | 2 |
| read-by | [agent:bob-cli-kx.3.1.4][2] | Need parent epic scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.4/README.md

<!-- sase:referenced-by:end -->
