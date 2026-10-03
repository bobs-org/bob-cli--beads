# Bead: bob-cli-3s.5 — Split plugin management into focused modules

[Bead Pages](../README.md) / [bob-cli-3s](README.md) / bob-cli-3s.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vn.md) · **Assignee:** `bob-cli-3s.5` · **Size:** large
**Created:** 2026-10-03 05:16:50 EDT
**Plan:** [202610/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_rust_files.md)

## Description

split-plugins: After split-capture-clip, reinspect src/native/plugins.rs and plan its final split; consider CLI, discovery/models, Git refresh, sync, diff/rendering, and tests. Keep every resulting Rust file at most 1500 lines, preserve plugin management behavior and coverage, and verify the cumulative file-size and test results for all five refactors.

## Dependencies

- **Depends on:** [bob-cli-3s.4](bob-cli-3s.4.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3s.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3s.5/README.md) | [bob-cli-3s.5](bob-cli-3s.5.md) | 0 |
