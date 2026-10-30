# Bead: bob-cli-e6.5 — Rust routing planners and the type\_mismatch lint

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.5` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-29 20:07:37 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

routing-core: add the pure agreement, retype, placement, and relocation planners with shared vectors, plus a read-only type_mismatch lint in bob plan.

## Notes

[2026-10-30T00:07:19Z · bob-cli-e6.5] PROPOSED FOLLOW-UP: cargo fmt --check flags pre-existing drift in src/native/config/themes.rs:370 on the clean base tree; just check fmt gate fails without this phase touching that file

[2026-10-30T00:07:26Z · bob-cli-e6.5] PROPOSED FOLLOW-UP: 12 cli integration tests (capture plan_budget/task_theme/pomodoro_close/task_complete, catalog protocol_1, plan human budget, ref_library today) fail identically on the clean base tree; stats/completion and complete_themes shell tests flake under parallel load — none caused by routing-core

[2026-10-30T00:07:37Z · bob-cli-e6.5] routing-core done: src/native/pomodoro_themes/routing.rs adds pure type_components/agrees/retype/place/relocate planners (running_retype=absorb) with 41 shared agree/retype/place/relocate vectors; bob plan emits read-only type_mismatch lint with additive link/entry/task_type/entry_types (verified live: mismatch flagged, agreement quiet); docs updated in task-types.md, plan.md, json-outputs.md. Verified: routing vectors ok, 48 pomodoro_themes + 29 plan_budget lib tests ok, clippy exit 0, docs-check and docs-gen pass. Full cli suite failures reproduce identically on clean tree (recorded as follow-ups). Work left uncommitted per review norm.

## Dependencies

- **Depends on:** [bob-cli-e6.4](bob-cli-e6.4.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.6](bob-cli-e6.6.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.8](bob-cli-e6.8.md) ○ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.5/README.md) | [bob-cli-e6.5](bob-cli-e6.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1750474`](https://github.com/bobs-org/bob-cli/commit/17504745c584e7e0bffc25342ce3791e3857560c) | feat(types): add task-type routing planners and type\_mismatch lint | [bob-cli-e6.5](bob-cli-e6.5.md) | 2026-10-29 20:09:50 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.5][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.5/README.md

<!-- sase:referenced-by:end -->
