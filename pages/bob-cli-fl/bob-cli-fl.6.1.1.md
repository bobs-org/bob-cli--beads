# Bead: bob-cli-fl.6.1.1 — Supply clock breakdowns for pinned Stats spans

[Bead Pages](../README.md) / [bob-cli-fl.6.1](bob-cli-fl.6.1.md) / bob-cli-fl.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.6.md) · **Assignee:** `bob-cli-fl.6.1.1` · **Size:** medium
**Created:** 2026-11-02 05:03:38 EST · **Closed:** 2026-11-02 05:57:16 EST
**Plan:** [202611/stats\_clock\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock_ui.md)

## Description

clock-presentation-contract: complete the additive Stats presentation data needed by bob-cli-fl.6; expose Bob-computed clock breakdowns and display strings for points, pinned parts, and complete-day totals; preserve existing clock semantics.

## Notes

[2026-11-02T10:57:16Z · bob-cli-fl.6.1.1] Added additive Bob-computed clock breakdowns to the Stats JSON in src/native/stats: ClockBreakdown{worked,off_clock}{value,display} on SeriesPoint (Total always, Worked when off-clock was left out), parts_clock_breakdown[dimension][key] on Total points (exact existing parts), clock_breakdown on Total PartSummary rows, and summary.total_clock_breakdown over exactly the complete days behind summary.total (headline untouched). DailyValue gained a clock tag set by the Pomodoro evaluator; off_clock_parts now survive daily/grouped/prior/provisional series. Existing numeric off_clock fields and all existing values are unchanged. Documented in docs/stats.md (Clock breakdowns + C9 vector). Verified: new unit tests (series/clock_tests.rs: daily, week/month, prior, provisional, adoption clipping, count units, zero/missing, corrupt split), evaluator clock test (metrics.rs), compute-level cross-lens tests on the homes vault (filtered themes/roots, multi-home, pins, formula isolation, day/week/month), and CLI JSON tests (tests/cli/stats_clock.rs); just check passed (fmt, clippy gate, 7626 tests, 0 failed) and just docs-check passed. No epic symbols outstanding.

## Dependencies

- **Blocks:** [bob-cli-fl.6.1.2](bob-cli-fl.6.1.2.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.1/README.md) | [bob-cli-fl.6.1.1](bob-cli-fl.6.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`247440c`](https://github.com/bobs-org/bob-cli/commit/247440cc97349c3ef658b032e281b07b936e531f) | feat(stats): report worked and off-clock clock breakdowns | [bob-cli-fl.6.1.1](bob-cli-fl.6.1.1.md) | 2026-11-02 05:58:33 EST |
