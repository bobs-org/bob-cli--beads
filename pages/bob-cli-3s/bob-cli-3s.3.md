# Bead: bob-cli-3s.3 — Split guarded task status writes into focused modules

[Bead Pages](../README.md) / [bob-cli-3s](README.md) / bob-cli-3s.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vn.md) · **Assignee:** `bob-cli-3s.3` · **Size:** large
**Created:** 2026-10-03 05:16:50 EDT · **Closed:** 2026-10-03 06:36:15 EDT
**Plan:** [202610/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_rust_files.md)

## Description

split-task-status-hooks-write: After split-capture-task-toggle, reinspect src/native/task_status_hooks_write.rs and plan its final split; consider model, snapshots/preflight, apply orchestration, recovery, filesystem staging, and tests. Keep every resulting Rust file at most 1500 lines and preserve guarded-write sequencing, platform behavior, and coverage.

## Notes

[2026-10-03T10:36:08Z · bob-cli-3s.3] PROPOSED FOLLOW-UP: one-off full-suite flake in capture_pomodoros missing_note_and_missing_section_are_warning_successes (passed in isolation and on lib rerun 1561/1561); watch for recurrence

[2026-10-03T10:36:15Z · bob-cli-3s.3] Split task_status_hooks_write.rs (2398 lines) into facade (31) plus task_status_hooks_write/: model.rs 409, snapshot.rs 217, preflight.rs 240, apply.rs 151, recovery.rs 269, staging.rs 303, tests.rs 859; all files at most 1500. cargo fmt --check pass; cargo clippy --all-targets --all-features pass (warnings only); cargo test task_status_hooks_write 21 passed; cargo test --test cli task_status_hooks 67 passed; cargo test --test randomize 15 passed; cargo test --lib 1561 passed on rerun. Notes: tree holds 21 unit tests (plan named 20; deletion_prevents_write moved unchanged too); enum-variant fields keep shared enum visibility (qualifiers rejected by E0449).

[2026-10-03T10:39:24Z · bob-cli-3s.3] PROPOSED FOLLOW-UP (evidence): capture_pomodoros missing_note flake is a process-global BOB_DAY_FILE race via unlocked with_env (capture_pomodoros.rs:1277); fails only under default parallel full cargo test (2 of 4 runs), passes in isolation and 1561/1561 with --test-threads=4; split adds/removes no tests and touches no env handling

## Dependencies

- **Depends on:** [bob-cli-3s.2](bob-cli-3s.2.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3s.4](bob-cli-3s.4.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3s.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3s.3.md) | [bob-cli-3s.3](bob-cli-3s.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b4a5022`](https://github.com/bobs-org/bob-cli/commit/b4a5022515e08c764299614c1c473a5199867608) | refactor(native): split task\_status\_hooks\_write into focused modules | [bob-cli-3s.3](bob-cli-3s.3.md) | 2026-10-03 06:40:14 EDT |
