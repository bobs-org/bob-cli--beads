# Bead: bob-cli-2f.6 — Split src/native/task\_status\_hooks.rs

[Bead Pages](../README.md) / [bob-cli-2f](README.md) / bob-cli-2f.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2u](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2u.md) · **Assignee:** `bob-cli-2f.6` · **Size:** large
**Created:** 2026-09-28 16:49:29 EDT
**Plan:** [202609/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/split_largest_rust_files.md)

## Description

split-task-status-hooks: turn the task status hook engine into a directory module (model, retry, sync, pomodoro, settings, structure, references, compose, output, split tests).

## Notes

[2026-09-28T23:30:03Z · bob-cli-2f.6] PROPOSED FOLLOW-UP: cargo clippy --all-targets --all-features fails on clean tree at tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr with || true) plus pre-existing warnings in capture_language, plugins, projects, task_status_groups, vault_sync; reproduces on HEAD, unrelated to task_status_hooks split

## Dependencies

- **Depends on:** [bob-cli-2f.5](bob-cli-2f.5.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2f.7](bob-cli-2f.7.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2f.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.6.md) | [bob-cli-2f.6](bob-cli-2f.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a89dff8`](https://github.com/bobs-org/bob-cli/commit/a89dff84d9d5c07662bd1482aa0ca78d08e6c09c) | refactor(task-status-hooks): split engine into directory module under 1500 lines | [bob-cli-2f.6](bob-cli-2f.6.md) | 2026-09-28 19:32:17 EDT |
