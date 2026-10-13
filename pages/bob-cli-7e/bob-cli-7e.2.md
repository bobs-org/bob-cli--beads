# Bead: bob-cli-7e.2 — Rust grammar, shared planner, guards, projects-sync anchor, and config

[Bead Pages](../README.md) / [bob-cli-7e](README.md) / bob-cli-7e.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4d.linker.w0.md) · **Assignee:** `bob-cli-7e.2` · **Size:** medium
**Created:** 2026-10-13 11:09:49 EDT · **Closed:** 2026-10-13 12:21:12 EDT
**Plan:** [202610/prerequisite\_blocks\_lines.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prerequisite_blocks_lines.md)

## Description

cli-core: add task_dependencies::blocks (parser, formatter, canonical sort, slot, and the one shared line planner), guard every Rust Task Link and tree-close scanner against both managed dependency lines, anchor Sub-projects after BLOCKS, and load dependencies.blocks_lines.

## Notes

[2026-10-13T16:20:32Z · bob-cli-7e.2--1] Scanner audit: capture-pomodoro-close, capture-pomodoros-agenda, and capture-pomodoro-start remain safe by exact bare-link shape; guards now exclude both managed dependency lines from reconcile Pomodoro scanning, plan-budget link scanning, completable placement, close-ledger classification, and embedded-tree close.

[2026-10-13T16:20:37Z · bob-cli-7e.2--1] PROPOSED FOLLOW-UP: Fix the existing percent-listen capture worker tests — just check failed capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio and capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance; both fail identically on clean base HEAD 4f72e5c (missing fake-listen invocation log / runner not invoked), so this phase records the baseline failure without expanding its scope.

[2026-10-13T16:21:12Z · bob-cli-7e.2--1] Implemented the BLOCKS parser/planner, config seam, projects-sync anchor, and managed-line scan guards. `just check` ran: format and clippy passed; 1,465 tests passed and two percent-listen worker tests failed, both reproduced identically on clean base HEAD 4f72e5c and recorded as a proposed follow-up. Scanner audit is recorded; epic-symbol check found no remaining entries.

## Dependencies

- **Depends on:** [bob-cli-7e.1](bob-cli-7e.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7e.5](bob-cli-7e.5.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7e.6](bob-cli-7e.6.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7e.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7e.2.md) | [bob-cli-7e.2](bob-cli-7e.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8e575c7`](https://github.com/bobs-org/bob-cli/commit/8e575c73570b68f991806f6b890a9a9440cc1f9b) | feat(task-dependencies): add BLOCKS parsing and managed-line guards | [bob-cli-7e.2](bob-cli-7e.2.md) | 2026-10-13 12:22:45 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7e.2--1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7e.2.md

<!-- sase:referenced-by:end -->
