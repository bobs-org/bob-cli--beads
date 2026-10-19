# Bead: bob-cli-9r.2 — Today cache details, generation guard, and revalidation

[Bead Pages](../README.md) / [bob-cli-9r](README.md) / bob-cli-9r.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11r](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11r.md) · **Assignee:** `bob-cli-9r.2` · **Size:** medium
**Created:** 2026-10-19 09:47:17 EDT · **Closed:** 2026-10-19 10:05:13 EDT
**Plan:** [202610/today\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/today_marks.md)

## Description

cache: extend the bob-ledger-tools Today cache with per-key Pomodoro details, a per-note id index, entered-key timestamps, and a details signature that refreshes only the marks. Add an async generation guard and focus/visibility revalidation, all with clock-injected tests.

## Notes

[2026-10-19T14:04:53Z · bob-cli-9r.2] PROPOSED FOLLOW-UP: Record decisions:today-mark-shows-ledger-today — epic decision memory_today_mark_record=no skipped the new decisions-web strand; land agent should file it if Bryan wants the record.

[2026-10-19T14:04:58Z · bob-cli-9r.2] PROPOSED FOLLOW-UP: npm test still fails the known clean-base cases — bob-cli-6v (unblocked-glyph x4), bob-cli-6w (Keep counts once), bob-cli-7i (forward conversion BLOCKS Work_ship#^prj); reproduced on original ledger-tools main.js.

[2026-10-19T14:05:13Z · bob-cli-9r.2] Today cache now carries per-key Pomodoro details, idsByPath, detailsSignature, and enteredAt stamps (ready same-date/path only, prune >2s). Generation guard drops stale async reads; sync daily-note writes bump gen first. Focus/visibility revalidateTodayCache is throttled to 1s. 32/32 today tests pass with injected clocks; fragments stay under 1000 lines; ledger-tools 1.58.2 built, validated, and synced. npm test extra failures are the known clean-base bob-cli-6v/6w/7i cases.

## Dependencies

- **Blocks:** [bob-cli-9r.3](bob-cli-9r.3.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9r.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9r.2/README.md) | [bob-cli-9r.2](bob-cli-9r.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ee9d7e6`](https://github.com/bobs-org/bob-plugins/commit/ee9d7e6b4a7eecd744f47a0269bdcb443efbf161) | feat(ledger-tools): cache Today Pomodoro details with a generation guard | [bob-cli-9r.2](bob-cli-9r.2.md) | 2026-10-19 10:06:22 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9r.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9r.2/README.md

<!-- sase:referenced-by:end -->
