# Bead: bob-cli-16 — Pomodoro sub-bullet moves and named Pomodoros

[Bead Pages](../README.md) / bob-cli-16

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0eb](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0eb.md) · **Assignee:** `bob-cli-16.land`
**Created:** 2026-08-26 10:04:14 EDT
**Plan:** [202608/pomodoro\_bullet\_move.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/pomodoro_bullet_move.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202608/pomodoro_bullet_move.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202608/pomodoro_bullet_move.md

<!-- sase:links:end -->

## Description

`<ctrl+shift+m>` on a Pomodoro sub-bullet moves that bullet — and, with a count, the next N sibling bullets — into another open Pomodoro in the same note, or into a new named Pomodoro created just below the current one, and the Pomodoro glossary entry documents named Pomodoros and this keymap.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-16.1](bob-cli-16.1.md) | Pure named-Pomodoro model, discovery, and planner | ✓ closed | medium | 2026-08-26 | 1 | 1 |
| [bob-cli-16.2](bob-cli-16.2.md) | Picker, routing, and commit | ✓ closed | medium | 2026-08-26 | 1 | 1 |
| [bob-cli-16.3](bob-cli-16.3.md) | Docs, version, sync, and glossary | ✓ closed | small | 2026-08-26 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-16: Pomodoro sub-bullet moves and named Pomodoros [in_progress]"]
    n1["bob-cli-16.1: Pure named-Pomodoro model, discovery, and planner [closed]"]
    n2["bob-cli-16.2: Picker, routing, and commit [closed]"]
    n3["bob-cli-16.3: Docs, version, sync, and glossary [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n2
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-16.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-16.1/README.md) | [bob-cli-16.1](bob-cli-16.1.md) | 1 |
| [bbugyi200.athena.bob-cli-16.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-16.2/README.md) | [bob-cli-16.2](bob-cli-16.2.md) | 1 |
| [bbugyi200.athena.bob-cli-16.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-16.3/README.md) | [bob-cli-16.3](bob-cli-16.3.md) | 1 |
| [bbugyi200.athena.bob-cli-16.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-16.land/README.md) | [bob-cli-16](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@117e33c`](https://github.com/bobs-org/bob-plugins/commit/117e33c63c45ddc46ac2d78ff214177559f90b30) | feat(bob-navigation-hotkeys): add named-Pomodoro grammar and bullet-move planner | [bob-cli-16.1](bob-cli-16.1.md) | 2026-08-26 10:56:45 EDT |
| bob-plugins | [`bob-plugins@87d38d6`](https://github.com/bobs-org/bob-plugins/commit/87d38d6de676787997197d2a037ccb25fafd16b1) | feat(navigation-hotkeys): add pomodoro bullet move picker | [bob-cli-16.2](bob-cli-16.2.md) | 2026-08-26 11:12:48 EDT |
| bob-cli | [`78e219b`](https://github.com/bobs-org/bob-cli/commit/78e219b61e4b1482bcf500d26485705420478ff1) | docs(memory): update Pomodoro glossary | [bob-cli-16.3](bob-cli-16.3.md) | 2026-08-26 11:18:40 EDT |
