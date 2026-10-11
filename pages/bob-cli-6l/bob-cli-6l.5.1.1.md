# Bead: bob-cli-6l.5.1.1 — Supply chart and calendar presentation data

[Bead Pages](../README.md) / [bob-cli-6l.5.1](bob-cli-6l.5.1.md) / bob-cli-6l.5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6l.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.5.md) · **Assignee:** `bob-cli-6l.5.1.1` · **Size:** medium
**Created:** 2026-10-11 14:15:46 EDT · **Closed:** 2026-10-11 14:43:38 EDT
**Plan:** [202610/stats\_charts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/stats_charts.md)

## Description

chart_data: add schema-1 presentation metadata for grouped chart bands, daily drill-down, checklist states, and chore summaries without changing existing metric values.

## Notes

[2026-10-11T18:43:23Z · bob-cli-6l.5.1.1] PROPOSED FOLLOW-UP: CLI percent-listen tests fail identically on this tree — capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance (listen runner was invoked) and percent_listen_reference_runs_existing_worker_and_installs_audio (read listen invocation: NotFound); tracked by bob-cli-6m; this phase did not touch capture/ref.

[2026-10-11T18:43:38Z · bob-cli-6l.5.1.1] Schema-1 chart/daily_points/checklist_state/chores/parts_display added without changing existing metric values. Golden M-vectors still match; day chart quartiles equal summary p25/p75; week/month bands use displayed bucket values and omit today/lead-in; grouped daily_points clip to the display window; checklist met/missed/not_due/missing/not_tracked and chore N of M days are Rust-derived. docs/stats.md documents fields and old-report fallbacks. cargo test --lib native::stats (139) and CLI stats tests passed. just check: fmt/clippy green; two CLI percent-listen failures match bob-cli-6m. epic-symbols empty.

## Dependencies

- **Blocks:** [bob-cli-6l.5.1.2](bob-cli-6l.5.1.2.md) ◐ · ⧖ 2026-10-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5.1.1/README.md) | [bob-cli-6l.5.1.1](bob-cli-6l.5.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ab314c0`](https://github.com/bobs-org/bob-cli/commit/ab314c061da8da06ed1d821c2afa03979c30cb4c) | feat(stats): add schema-1 chart, daily\_points, checklist, and chore metadata | [bob-cli-6l.5.1.1](bob-cli-6l.5.1.1.md) | 2026-10-11 14:45:40 EDT |
