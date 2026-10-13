# Bead: bob-cli-6u.13 — Ctrl+Shift+P Depends on for ^prj blocks residents

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.13` · **Size:** medium
**Created:** 2026-10-12 10:26:02 EDT · **Closed:** 2026-10-12 14:59:09 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

nav-deps-stage: on ^prj the ordinary Depends on writer also blocks, tags, and unlinks residents with commitment transfer; removal recovers them with [unblocked::]; same-note and cycle guards; api routes and notices.

## Notes

[2026-10-12T18:58:47Z · bob-cli-6u.13] PROPOSED FOLLOW-UP: just check has 2 pre-existing cli failures also red on the clean base (task_status_hooks_reconciles_future_schedules_and_combined_blocking_reasons expects 7 got 11; projects_sync_then_task_status_hooks_blocks_and_recovers_propagated_tasks) — needs a task bead

[2026-10-12T18:58:52Z · bob-cli-6u.13] PROPOSED FOLLOW-UP: full bob-plugins npm test shows only the 5 known baseline failures, identical on the clean base (ledger unblocked-glyph x4, decision-card keep count x1)

[2026-10-12T18:59:09Z · bob-cli-6u.13] nav-deps-stage done: planDependencyEdit blocks/tags residents with strongest-lane transfer on ^prj add, recovers them with [unblocked::] on last-reason removal; same-note refused (planner + stage guard), implicit resident cycle edges, api v3 delegates, project notices; new test-navigation-project-dependency-stage.cjs 17/17 pass, neighbors 151/151 pass, build+validate green, deployed 2.23.0 on this host; full npm test 2505/2510 with only the 5 known baseline failures (identical on clean base); just check has 2 pre-existing cli failures also red on clean base (recorded as follow-ups)

## Dependencies

- **Depends on:** [bob-cli-6u.12](bob-cli-6u.12.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.14](bob-cli-6u.14.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.13/README.md) | [bob-cli-6u.13](bob-cli-6u.13.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a36a39b`](https://github.com/bobs-org/bob-cli/commit/a36a39bd8061286e5080c5636c3cdb6a21f5b0b2) | docs(task-deps): Ctrl+Shift+P Depends on for ^prj blocks residents | [bob-cli-6u.13](bob-cli-6u.13.md) | 2026-10-12 15:00:26 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.13][2] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-6u.8][3] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.13/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
