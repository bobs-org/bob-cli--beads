# Bead: bob-cli-q5.8.1.2 — Decode wake receipts and model notice delivery

[Bead Pages](../README.md) / [bob-cli-q5.8.1](bob-cli-q5.8.1.md) / bob-cli-q5.8.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.md) · **Assignee:** `bob-cli-q5.8.1.2` · **Size:** medium
**Created:** 2026-11-26 12:54:20 EST · **Closed:** 2026-11-26 14:39:16 EST
**Plan:** [202611/mac\_snooze\_wake\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice.md)

## Description

notice-core: implement portable receipt, list, and add-response models, bounded receipt reading, independent subprocess lanes, and a deterministic presence, meeting, revalidation, and expiry policy with clock-controlled tests.

## Notes

[2026-11-26T19:39:16Z · bob-cli-q5.8.1.2] notice-core done in bob-mac-capture: SnoozeWakeReceipt + 4MB bounded reader (XDG/HOME paths, schema-1 ignore, nonfatal diagnostics), SnoozeWakeListResponse/SnoozeWakeAddResponse with wake_notice_version capability probe (missing/unknown ownership or eligibility never permits announce), BobProcessClient snooze-list read lane + non-cancelling snooze-add mutation lane with exact argv/env and per-executable unsupported caching, deterministic SnoozeWakeNoticePolicy (injected clocks; 179.9/180s idle, each away signal, hold toggles, 1.5s settle, hold-during-verify, overlapping meetings, exact end boundaries, buffered-vs-actual spans, cancelled rows, stale phase labels, day/clock/vault changes, 4h cutoff, future-dated rejection, duplicate/distinct IDs, empty/partial/failed verification, generation tokens, bob-offset wall-time zones) and pure SnoozeWakeNoticePresentation + bounded day-scoped acknowledgement store (single/batch/over-cap copy from list budget, stable snooze-woken IDs, all ack triggers). fake-bob extended with snooze list/add branches. Verified: just portable-check green (format lint exit 0, build exit 0, 2908 tests 0 failures; one parallel-run MeetingNotesSessionTests ordering flake seen once, passes in isolation, in-suite, and on full re-run).

## Dependencies

- **Depends on:** [bob-cli-q5.8.1.1](bob-cli-q5.8.1.1.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.8.1.3](bob-cli-q5.8.1.3.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.2/README.md) | [bob-cli-q5.8.1.2](bob-cli-q5.8.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@08e7251`](https://github.com/bobs-org/bob-mac-capture/commit/08e72511fe0d2148c6f6a3862574e52bf19004e8) | feat(snooze): decode wake receipts and model notice delivery | [bob-cli-q5.8.1.2](bob-cli-q5.8.1.2.md) | 2026-11-26 14:40:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.2][1] | Need phase scope and design file | 3 |
| read-by | [agent:bob-cli-q5.8.1.5][2] | Need sibling phase status to avoid duplication | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.5/README.md

<!-- sase:referenced-by:end -->
