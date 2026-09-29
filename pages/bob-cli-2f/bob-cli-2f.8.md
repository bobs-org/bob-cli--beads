# Bead: bob-cli-2f.8 — Split src/native/collect\_done.rs

[Bead Pages](../README.md) / [bob-cli-2f](README.md) / bob-cli-2f.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2u](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2u.md) · **Assignee:** `bob-cli-2f.8` · **Size:** large
**Created:** 2026-09-28 16:49:29 EDT · **Closed:** 2026-09-28 20:18:16 EDT
**Plan:** [202609/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/split_largest_rust_files.md)

## Description

split-collect-done: turn move-done-tasks collection into a directory module (plan, git, archive, link repair, markdown transform, split tests) and fix relative include_str! fixture paths.

## Notes

[2026-09-29T00:18:05Z · bob-cli-2f.8] PROPOSED FOLLOW-UP: cargo clippy --all-targets fails in tests/cli/capture/pomodoro_name.rs:808 overly_complex_bool_expr (pre-existing, files untouched by split-collect-done; just all blocked by this)

[2026-09-29T00:18:16Z · bob-cli-2f.8] Split collect_done.rs (4344 lines, 67 tests) into directory module; all files <=1500 lines (mod 342, plan 427, git 205, archive 336, link_repair 840, transform 385, tests/mod 116, tests/unit 932, tests/plan 718); cargo test -- --list 1794 matches baseline, rg #[test] totals 67, cargo test passes 67/67 collect_done and full suite; cargo fmt --check passes, no clippy warnings in collect_done; just all blocked by pre-existing clippy overly_complex_bool_expr in tests/cli/capture/pomodoro_name.rs:808 (untouched, noted as follow-up)

## Dependencies

- **Depends on:** [bob-cli-2f.7](bob-cli-2f.7.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2f.9](bob-cli-2f.9.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2f.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.8.md) | [bob-cli-2f.8](bob-cli-2f.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`65a3917`](https://github.com/bobs-org/bob-cli/commit/65a39179b278f4eee9d6cd8b0e44432e52dfbf13) | feat(collect-done): split collect\_done.rs into directory module | [bob-cli-2f.8](bob-cli-2f.8.md) | 2026-09-28 20:19:28 EDT |
