# Bead: bob-cli-go.4 — Rust merge engine for task, drawer, and section containers

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.4` · **Size:** large
**Created:** 2026-11-03 16:11:30 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

merge-engine: implement plan_task_merge, which validates, cuts each source's notes into the container, re-points dependents, writes the relation or Cancel Log provenance, cancels, prunes today's links, offers the target, and reports, with idempotent re-runs and property tests.

## Notes

[2026-11-03T23:11:21Z · bob-cli-go.4] PROPOSED FOLLOW-UP: Parent design research reference is missing — audited read of research:202611/task_move_merge_split_design/task_move_merge_split_design.md returned status missing on 2026-11-03; plan:202611/task_move_merge_split.md and docs/task-merge.md remain available and sufficient for the engine plan. Land agent should repair the stale citation or restore the artifact.

## Dependencies

- **Depends on:** [bob-cli-go.1](bob-cli-go.1.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-go.2](bob-cli-go.2.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.5](bob-cli-go.5.md) ◐ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.6](bob-cli-go.6.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.md) | [bob-cli-go.4](bob-cli-go.4.md) | 0 |
