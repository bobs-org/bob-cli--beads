# Bead: bob-cli-fe — Merged Pomodoros: merge by default, split and merge by type, honest close names

[Bead Pages](../README.md) / bob-cli-fe

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c4.md) · **Assignee:** `bob-cli-fe.land`
**Created:** 2026-11-01 16:00:42 EST
**Plan:** [202611/merged\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merged_pomodoros.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/merged_pomodoros.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merged_pomodoros.md

<!-- sase:links:end -->

## Description

A Pomodoro that holds several task types is a first-class merged Pomodoro. Linking or moving a task into another type's Pomodoro merges that type into the name instead of retyping the task. Capture `=*` and `=/` merge and split Pomodoros by type, and so does Obsidian Ctrl+S. `x` names the closed and carried sessions after the work that was actually done and is still planned. bob-cli, bob-plugins, and Bob Mac Capture all agree, through shared vectors.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-fe.1](bob-cli-fe.1.md) | Pure planners and shared vectors (bob-cli) | ✓ closed | medium | 2026-11-01 | 1 | 1 |
| [bob-cli-fe.10](bob-cli-fe.10.md) | Merged Pomodoro memory (bob-cli) | ◐ in_progress | small | 2026-11-01 | 1 | 0 |
| [bob-cli-fe.2](bob-cli-fe.2.md) | Capture lands by merging (bob-cli) | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fe.3](bob-cli-fe.3.md) | The =/ split syntax end to end (bob-cli) | ◐ in_progress | large | 2026-11-01 | 1 | 0 |
| [bob-cli-fe.4](bob-cli-fe.4.md) | The =\* merge syntax end to end (bob-cli) | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fe.5](bob-cli-fe.5.md) | x narrows the closed name and sheds the carried name (bob-cli) | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fe.6](bob-cli-fe.6.md) | Obsidian pickers merge by default (bob-plugins) | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fe.7](bob-cli-fe.7.md) | Ctrl+S splits the selected Pomodoro (bob-plugins) | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fe.8](bob-cli-fe.8.md) | Ctrl+Enter Pomodoro completion parity (bob-plugins) | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fe.9](bob-cli-fe.9.md) | Present split, merge, merged links, and close names (Bob Mac Capture) | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-fe: Merged Pomodoros: merge by default, split and merge by type, honest close names [in_progress]"]
    n1["bob-cli-fe.1: Pure planners and shared vectors (bob-cli) [closed]"]
    n2["bob-cli-fe.10: Merged Pomodoro memory (bob-cli) [in_progress]"]
    n3["bob-cli-fe.2: Capture lands by merging (bob-cli) [in_progress]"]
    n4["bob-cli-fe.3: The =/ split syntax end to end (bob-cli) [in_progress]"]
    n5["bob-cli-fe.4: The =* merge syntax end to end (bob-cli) [in_progress]"]
    n6["bob-cli-fe.5: x narrows the closed name and sheds the carried name (bob-cli) [in_progress]"]
    n7["bob-cli-fe.6: Obsidian pickers merge by default (bob-plugins) [in_progress]"]
    n8["bob-cli-fe.7: Ctrl+S splits the selected Pomodoro (bob-plugins) [in_progress]"]
    n9["bob-cli-fe.8: Ctrl+Enter Pomodoro completion parity (bob-plugins) [in_progress]"]
    n10["bob-cli-fe.9: Present split, merge, merged links, and close names (Bob Mac Capture) [in_progress]"]
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
    n1 -.-> n4
    n1 -.-> n6
    n1 -.-> n7
    n3 -.-> n2
    n3 -.-> n10
    n4 -.-> n5
    n5 -.-> n2
    n5 -.-> n10
    n6 -.-> n2
    n6 -.-> n9
    n6 -.-> n10
    n7 -.-> n8
    n8 -.-> n2
    n8 -.-> n9
    n9 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fe.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.1/README.md) | [bob-cli-fe.1](bob-cli-fe.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-fe.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.10/README.md) | [bob-cli-fe.10](bob-cli-fe.10.md) | 0 |
| [bbugyi200.apollo.bob-cli-fe.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.2/README.md) | [bob-cli-fe.2](bob-cli-fe.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-fe.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.3/README.md) | [bob-cli-fe.3](bob-cli-fe.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-fe.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.4/README.md) | [bob-cli-fe.4](bob-cli-fe.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-fe.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.5/README.md) | [bob-cli-fe.5](bob-cli-fe.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-fe.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.6/README.md) | [bob-cli-fe.6](bob-cli-fe.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-fe.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.7/README.md) | [bob-cli-fe.7](bob-cli-fe.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-fe.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.8/README.md) | [bob-cli-fe.8](bob-cli-fe.8.md) | 0 |
| [bbugyi200.apollo.bob-cli-fe.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.9/README.md) | [bob-cli-fe.9](bob-cli-fe.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-fe.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.land/README.md) | [bob-cli-fe](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`675330d`](https://github.com/bobs-org/bob-cli/commit/675330dd5e4be39ebe920931b28a01b852bf78d5) | feat(types): add merged-Pomodoro routing planners | [bob-cli-fe.1](bob-cli-fe.1.md) | 2026-11-01 17:35:55 EST |
