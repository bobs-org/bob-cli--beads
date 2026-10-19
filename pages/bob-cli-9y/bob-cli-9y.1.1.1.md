# Bead: bob-cli-9y.1.1.1 — Build the pure task-move planner

[Bead Pages](../README.md) / [bob-cli-9y.1.1](bob-cli-9y.1.1.md) / bob-cli-9y.1.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-9y.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9y.1.md) · **Assignee:** `bob-cli-9y.1.1.1` · **Size:** medium
**Created:** 2026-10-19 16:37:59 EDT · **Closed:** 2026-10-19 17:10:00 EDT
**Plan:** [202610/task\_move.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_move.md)

## Description

move-planner: implement and test snapshot-only selection, task-block movement, identity validation, collision renaming, and contextual vault-wide link repair in bob-cli; preserve task metadata and existing archive behavior.

## Notes

[2026-10-19T21:10:00Z · bob-cli-9y.1.1.1] Implemented the snapshot-only task-move planner under src/native/task_move/{mod,plan,tests}.rs. Public-to-crate interface: crate::native::task_move::{load_vault_snapshot, plan_task_move, MovePlan, MoveRequest, MoveSelector, PlanError, VaultSnapshot} plus crate::native::task_move::plan::{MoveRecord, RenameRecord, RepairedFile, TaskCandidate}. Temporary unused-code gate: #[cfg(test)] mod task_move in src/native.rs until bob-cli-9y.1.1.2 wires production dispatch; nested types are reachable via pub(crate) mod plan. Reused collect_done helpers (task_block_end, next_available_block_id with reserved co-moved ids, NoteIndex/MovedBlockTargets/repair_links_in_note) via pub(crate) re-exports; archive behavior unchanged. Verified cargo test --lib native::task_move (23 passed) and native::collect_done (69 passed), cargo fmt --all -- --check, and cargo clippy --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces. No --epic-symbol leftovers. Did not add bob task move CLI.

## Dependencies

- **Blocks:** [bob-cli-9y.1.1.2](bob-cli-9y.1.1.2.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9y.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9y.1.1.1/README.md) | [bob-cli-9y.1.1.1](bob-cli-9y.1.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bfca341`](https://github.com/bobs-org/bob-cli/commit/bfca3419c3f5c4caa9a609c6e4f64a2dc6a86111) | feat(task-move): add snapshot-only task-move planner | [bob-cli-9y.1.1.1](bob-cli-9y.1.1.1.md) | 2026-10-19 17:10:56 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9y.1.1.1][1] | Need remaining DECISIONS, notes, and close-out constraints | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9y.1.1.1/README.md

<!-- sase:referenced-by:end -->
