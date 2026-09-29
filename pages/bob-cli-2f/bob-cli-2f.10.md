# Bead: bob-cli-2f.10 — Split src/native/capture\_pomodoro\_close.rs

[Bead Pages](../README.md) / [bob-cli-2f](README.md) / bob-cli-2f.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2u](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2u.md) · **Assignee:** `bob-cli-2f.10` · **Size:** large
**Created:** 2026-09-28 16:49:30 EDT · **Closed:** 2026-09-28 21:15:26 EDT
**Plan:** [202609/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/split_largest_rust_files.md)

## Description

split-capture-pomodoro-close: separate the ledger close planner, link and marker parsing, the linked-task close planner, and their two test modules into a directory module.

## Notes

[2026-09-29T01:15:05Z · bob-cli-2f.10] PROPOSED FOLLOW-UP: 'cargo clippy --all-targets --all-features' (and 'just all' lint stage) fails on clean base with 'clippy::overly_complex_bool_expr' denied at tests/cli/capture/pomodoro_name.rs:808 ('|| true' in boolean expression). Identical failure with and without this phase's split; unrelated file, left untouched. Already tracked in prior phase notes (e.g. bob-cli-2f.9, bob-cli-2f.8).

[2026-09-29T01:15:11Z · bob-cli-2f.10] PROPOSED FOLLOW-UP: Required 're-export every pub(crate) item' leaves 10 unused_import warnings in src/native/capture_pomodoro_close/mod.rs (ClassifiedLink, CloseTiming, NamedPomodoro, NextPomodoro, WorkLogNoteGroup, close_timing, CloseTaskRole, PomodoroCloseSummary, PomodoroCloseTask, exact_struck) since nothing names those paths via the parent. Warnings only; cargo build/test green. Future cleanup could narrow the parent re-exports to the 16 externally-used paths.

[2026-09-29T01:15:26Z · bob-cli-2f.10] Split src/native/capture_pomodoro_close.rs (2982 lines) into capture_pomodoro_close/ directory: mod.rs 41 (facade with close_task_text and pub(crate) re-exports), ledger.rs 864, links.rs 341 (MarkerPolicy through bare_embedded_link plus POMODORO_MARKER), linked_tasks.rs 972, tests.rs 467 (18 tests), linked_task_tests.rs 341 (7 tests). All files under 1500-line cap. 25 #[test] fns retained (18+7) and pass; full cargo test green (1139 lib + all integration, 0 failed); cargo fmt clean; git status shows changes only inside src/native/capture_pomodoro_close/. Callers compile with no edits via parent re-exports. just all lint stage fails identically on clean base at tests/cli/capture/pomodoro_name.rs:808 overly_complex_bool_expr deny (recorded as PROPOSED FOLLOW-UP); 10 unused_import warnings from required re-export-all recorded as second PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-2f.9](bob-cli-2f.9.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2f.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.10.md) | [bob-cli-2f.10](bob-cli-2f.10.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f8b03c2`](https://github.com/bobs-org/bob-cli/commit/f8b03c2bc696c6020a1d246cd29d555e54c6fa1b) | refactor(native): split capture\_pomodoro\_close into directory module | [bob-cli-2f.10](bob-cli-2f.10.md) | 2026-09-28 21:17:06 EDT |
