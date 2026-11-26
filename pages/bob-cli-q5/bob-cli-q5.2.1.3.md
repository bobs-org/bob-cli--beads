# Bead: bob-cli-q5.2.1.3 — Report the snoozed meter and nonbinding wake forecast

[Bead Pages](../README.md) / [bob-cli-q5.2.1](bob-cli-q5.2.1.md) / bob-cli-q5.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.md) · **Assignee:** `bob-cli-q5.2.1.3` · **Size:** medium
**Created:** 2026-11-25 19:37:41 EST · **Closed:** 2026-11-26 05:00:11 EST
**Plan:** [202611/snoozed\_planned\_today.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_planned_today.md)

## Description

plan-forecast: extend PlanReport and every report construction path with snoozed counts, next wake, and an on-clock forecast; add the forecast lint and human line without changing current budget status, Today, or whole-lane meters. Cover missing-ledger, clock-policy, and cap-boundary cases and update docs.

## Notes

[2026-11-26T09:59:55Z · bob-cli-q5.2.1.3] PROPOSED FOLLOW-UP: full `cargo test --workspace` shows pre-existing drawer/capture failures that reproduce identically on the clean base tree (e.g. native::capture::block_diff::annotate_drawer_lines, capture_clip drawer escaping, capture_complete drawer menus, capture::authored/clip drawer cases); unrelated to plan-forecast, leave for existing drawer/capture tracks (predecessor notes cite bob-cli-q9, bob-cli-q4, bob-cli-q7) -r Recording pre-existing check failures

[2026-11-26T10:00:01Z · bob-cli-q5.2.1.3] PROPOSED FOLLOW-UP: task_status_hooks::sync::task_status_hooks_groups_area_project_tasks_after_final_statuses fails identically on the clean base tree (Alpha project grouping header mismatch); unrelated to plan-forecast snoozed enrichment, needs its own track -r Recording pre-existing hooks test failure

[2026-11-26T10:00:11Z · bob-cli-q5.2.1.3] plan-forecast done: PlanReport carries additive snoozed {count,due,blocked,on_clock,next_wake_at,forecast} with schema 3; shared with_snoozed_forecast enriches bob plan (including Snoozed-only notes, outside has_section guard), the empty-report path via assemble, and hooks sync plan_budget; snooze_wake_would_exceed_cap fires only when on_clock>0 pushes forecast over cap, never changes status/links/today/lanes; human adds SNOOZED line (amber due, dimmed blocked, TODAY a/b when all wake, omitted at zero). Verified: 11 new plan_snoozed tests pass (missing-ledger, Snoozed-only, asleep/due/blocked, alias/duplicate, already-linked, explicit+inherited off-clock, exact/over-cap, Today/lane stability), existing plan/plan_off_clock pass, walks snoozed vectors pass, just docs-gen + docs-check pass, fmt/clippy clean. Full workspace failures (drawer/capture suites, one hooks grouping test) reproduce identically on clean base; recorded as PROPOSED FOLLOW-UP. Today stays ledger-derived; no plugin/Mac/memory/release work claimed.

## Dependencies

- **Depends on:** [bob-cli-q5.2.1.1](bob-cli-q5.2.1.1.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q5.2.1.2](bob-cli-q5.2.1.2.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.2.1.4](bob-cli-q5.2.1.4.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.3/README.md) | [bob-cli-q5.2.1.3](bob-cli-q5.2.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4a81217`](https://github.com/bobs-org/bob-cli/commit/4a8121734d0b16b54d377c81708c7671a2d8ee76) | feat(plan): add snoozed forecast enrichment and cap lint | [bob-cli-q5.2.1.3](bob-cli-q5.2.1.3.md) | 2026-11-26 05:01:32 EST |
