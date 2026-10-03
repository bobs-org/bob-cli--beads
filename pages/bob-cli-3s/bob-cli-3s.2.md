# Bead: bob-cli-3s.2 — Split task toggle and link planners into focused modules

[Bead Pages](../README.md) / [bob-cli-3s](README.md) / bob-cli-3s.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vn.md) · **Assignee:** `bob-cli-3s.2` · **Size:** large
**Created:** 2026-10-03 05:16:50 EDT · **Closed:** 2026-10-03 06:16:02 EDT
**Plan:** [202610/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_rust_files.md)

## Description

split-capture-task-toggle: After split-capture-complete, reinspect src/native/capture_task_toggle.rs and plan its final split; consider task updates, link insertion/removal, relocation, ledger planning, text edits, and tests. Keep every resulting Rust file at most 1500 lines and preserve pure-planner behavior and coverage.

## Notes

[2026-10-03T10:15:49Z · bob-cli-3s.2] PROPOSED FOLLOW-UP: just all intermittently fails on native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes (BOB_DAY_FILE race); reproduces on clean base tree 2/3 runs, passes in isolation; already tracked by bob-cli-2e

[2026-10-03T10:16:02Z · bob-cli-3s.2] Split src/native/capture_task_toggle.rs (2507 lines) into facade (45) plus capture_task_toggle/text.rs (280), task_update.rs (329), links.rs (388), relocation.rs (394), ledger.rs (329), tests.rs (810); all files at most 1500, capture_complete files still at most 1500 (max 496). cargo fmt --check pass; cargo clippy --all-targets --all-features pass (exit 0); cargo test capture_task_toggle: 49 lib + 15 CLI pass; cargo test --test cli capture: 461 pass; cargo test --test randomize: 15 pass. Full just all flakes on pre-existing BOB_DAY_FILE race (bob-cli-2e, reproduces 2/3 on clean base).

## Dependencies

- **Depends on:** [bob-cli-3s.1](bob-cli-3s.1.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3s.3](bob-cli-3s.3.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3s.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3s.2.md) | [bob-cli-3s.2](bob-cli-3s.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c9a6f1b`](https://github.com/bobs-org/bob-cli/commit/c9a6f1b453b12730f1a64b4d2b16a2314e383c1d) | refactor(capture): split capture\_task\_toggle into focused modules | [bob-cli-3s.2](bob-cli-3s.2.md) | 2026-10-03 06:17:25 EDT |
