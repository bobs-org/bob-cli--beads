# Bead: bob-cli-2f — Split the ten largest Rust files into modules of at most 1500 lines

[Bead Pages](../README.md) / bob-cli-2f

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2u](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2u.md) · **Assignee:** `bob-cli-2f.land`
**Created:** 2026-09-28 16:49:29 EDT
**Plan:** [202609/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/split_largest_rust_files.md)

## Description

Each of the ten largest Rust source files in bob-cli is split into cohesive modules in which every resulting file has at most 1500 lines. Behavior does not change, the test count stays the same, and `just all` stays green after every phase.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-2f.1](bob-cli-2f.1.md) | Split tests/cli.rs | ✓ closed | large | 2026-09-28 | 1 | 1 |
| [bob-cli-2f.10](bob-cli-2f.10.md) | Split src/native/capture\_pomodoro\_close.rs | ◐ in_progress | large | 2026-09-28 | 1 | 0 |
| [bob-cli-2f.2](bob-cli-2f.2.md) | Split src/native/capture.rs | ◐ in_progress | large | 2026-09-28 | 1 | 0 |
| [bob-cli-2f.3](bob-cli-2f.3.md) | Split src/native/capture\_language.rs | ◐ in_progress | large | 2026-09-28 | 1 | 0 |
| [bob-cli-2f.4](bob-cli-2f.4.md) | Split src/native/highlights\_ref/mod.rs | ◐ in_progress | large | 2026-09-28 | 1 | 0 |
| [bob-cli-2f.5](bob-cli-2f.5.md) | Split src/native/dataview.rs | ◐ in_progress | large | 2026-09-28 | 1 | 0 |
| [bob-cli-2f.6](bob-cli-2f.6.md) | Split src/native/task\_status\_hooks.rs | ◐ in_progress | large | 2026-09-28 | 1 | 0 |
| [bob-cli-2f.7](bob-cli-2f.7.md) | Split src/native/projects.rs | ◐ in_progress | large | 2026-09-28 | 1 | 0 |
| [bob-cli-2f.8](bob-cli-2f.8.md) | Split src/native/collect\_done.rs | ◐ in_progress | large | 2026-09-28 | 1 | 0 |
| [bob-cli-2f.9](bob-cli-2f.9.md) | Split src/native/task\_status\_groups.rs | ◐ in_progress | large | 2026-09-28 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-2f: Split the ten largest Rust files into modules of at most 1500 lines [in_progress]"]
    n1["bob-cli-2f.1: Split tests/cli.rs [closed]"]
    n2["bob-cli-2f.10: Split src/native/capture_pomodoro_close.rs [in_progress]"]
    n3["bob-cli-2f.2: Split src/native/capture.rs [in_progress]"]
    n4["bob-cli-2f.3: Split src/native/capture_language.rs [in_progress]"]
    n5["bob-cli-2f.4: Split src/native/highlights_ref/mod.rs [in_progress]"]
    n6["bob-cli-2f.5: Split src/native/dataview.rs [in_progress]"]
    n7["bob-cli-2f.6: Split src/native/task_status_hooks.rs [in_progress]"]
    n8["bob-cli-2f.7: Split src/native/projects.rs [in_progress]"]
    n9["bob-cli-2f.8: Split src/native/collect_done.rs [in_progress]"]
    n10["bob-cli-2f.9: Split src/native/task_status_groups.rs [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n1 -.-> n3
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
    n7 -.-> n8
    n8 -.-> n9
    n9 -.-> n10
    n10 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2f.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.1.md) | [bob-cli-2f.1](bob-cli-2f.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-2f.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.10/README.md) | [bob-cli-2f.10](bob-cli-2f.10.md) | 0 |
| [bbugyi200.apollo.bob-cli-2f.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.2/README.md) | [bob-cli-2f.2](bob-cli-2f.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-2f.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.3/README.md) | [bob-cli-2f.3](bob-cli-2f.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-2f.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.4/README.md) | [bob-cli-2f.4](bob-cli-2f.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-2f.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.5/README.md) | [bob-cli-2f.5](bob-cli-2f.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-2f.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.6/README.md) | [bob-cli-2f.6](bob-cli-2f.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-2f.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.7/README.md) | [bob-cli-2f.7](bob-cli-2f.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-2f.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.8/README.md) | [bob-cli-2f.8](bob-cli-2f.8.md) | 0 |
| [bbugyi200.apollo.bob-cli-2f.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.9/README.md) | [bob-cli-2f.9](bob-cli-2f.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-2f.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2f.land/README.md) | [bob-cli-2f](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7d1c8dd`](https://github.com/bobs-org/bob-cli/commit/7d1c8dd3054fd30f6e4f5a15e2dc61c42c3b2593) | refactor(tests): split tests/cli.rs into tests/cli/ target with support and per-command modules | [bob-cli-2f.1](bob-cli-2f.1.md) | 2026-09-28 17:22:16 EDT |
