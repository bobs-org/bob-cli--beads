# Bead: bob-cli-2f.7 — Split src/native/projects.rs

[Bead Pages](../README.md) / [bob-cli-2f](README.md) / bob-cli-2f.7

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2u](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2u.md) · **Assignee:** `bob-cli-2f.7` · **Size:** large
**Created:** 2026-09-28 16:49:29 EDT
**Plan:** [202609/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/split_largest_rust_files.md)

## Description

split-projects: turn the projects command into a directory module (model, scan/parse, sync planning, edits, tags/inline fields, output, split tests).

## Notes

[2026-09-28T23:49:21Z · bob-cli-2f.7] Split complete: src/native/projects.rs (4652 lines, 53 tests) -> projects/ directory module. Files: mod.rs 201, model.rs 455, scan.rs 576, sync.rs 766, edits.rs 696, tags.rs 242, output.rs 351, tests/mod.rs 67, tests/parse.rs 254 (12 tests), tests/sync.rs 642 (21 tests), tests/edits.rs 476 (20 tests). All 53 unit tests pass; 22 projects integration tests pass; full cargo test passes (1139 lib + 515 cli). cargo fmt clean. PROPOSED FOLLOW-UP: just all lint fails on clean-base unrelated file tests/cli/capture/pomodoro_name.rs:808 (clippy overly_complex_bool_expr deny for || true, introduced in 7d1c8dd); untouched by this phase. Also pre-existing clippy warning in moved code projects/scan.rs:215 (let-else vs ?), moved verbatim.

## Dependencies

- **Depends on:** [bob-cli-2f.6](bob-cli-2f.6.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2f.8](bob-cli-2f.8.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2f.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.7.md) | [bob-cli-2f.7](bob-cli-2f.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0abb2bd`](https://github.com/bobs-org/bob-cli/commit/0abb2bd6f45cd587fc0d66f1e1f8af096b751b61) | refactor(projects): split command into directory module under 1500 lines | [bob-cli-2f.7](bob-cli-2f.7.md) | 2026-09-28 19:51:32 EDT |
