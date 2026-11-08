# Bead: bob-cli-ii.7 — Reply badge, no-reply pill, and the daily-note Gmail sync

[Bead Pages](../README.md) / [bob-cli-ii](README.md) / bob-cli-ii.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19q.md) · **Assignee:** `bob-cli-ii.7` · **Size:** medium
**Created:** 2026-11-07 17:21:22 EST · **Closed:** 2026-11-08 12:28:35 EST
**Plan:** [202611/gmail\_sync\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_reply_watch.md)

## Description

signals: add the display-only reply badge on mail links, the muted no-reply pill on nudge-due rows, the Also replied tooltip pip, and a once-per-day Ledger Tools gmail sync when today's daily note is created.

## Notes

[2026-11-08T17:28:35Z · bob-cli-ii.7] Verified signals phase: mail-link-marks contract (order 43) plus no-reply pill and Also-replied tooltip pip; Ledger Tools reply badge, no-reply pills, tooltip pip, and once-per-path daily-note `bob gmail sync -q -f json -r 30` after gcal settles. just docs-check passed (447 tests); bob-plugins npm test passed (5745, including mail-link-marks, no-reply-pills, block-marks AP1-AP4, and gmail sync). bob plugins sync deployed bob-ledger-tools. epic-symbols: none leftover.

## Dependencies

- **Depends on:** [bob-cli-ii.2](bob-cli-ii.2.md) ✓ · ⧖ 2026-11-07
- **Depends on:** [bob-cli-ii.3](bob-cli-ii.3.md) ✓ · ⧖ 2026-11-07
- **Depends on:** [bob-cli-ii.6](bob-cli-ii.6.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.7/README.md) | [bob-cli-ii.7](bob-cli-ii.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`126958b`](https://github.com/bobs-org/bob-cli/commit/126958b2f5ff0a3bb05d0ad6ebb75b6e02f0d4c5) | docs(mail): add reply-badge and no-reply-pill display contracts | [bob-cli-ii.7](bob-cli-ii.7.md) | 2026-11-08 12:30:03 EST |
| bob-plugins | [`bob-plugins@d962fb1`](https://github.com/bobs-org/bob-plugins/commit/d962fb10c6e6229641c707a0016fb34b2663c666) | feat(ledger-tools): add reply badges, no-reply pills, and daily Gmail sync | [bob-cli-ii.7](bob-cli-ii.7.md) | 2026-11-08 12:36:27 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-in.3][1] | Need to identify whether unused sync read APIs have a real consumer in the open Gmail health phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-in.3/README.md

<!-- sase:referenced-by:end -->
