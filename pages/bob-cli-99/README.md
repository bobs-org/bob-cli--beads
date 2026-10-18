# Bead: bob-cli-99 — Reading Board — a read-only kanban of the reading queue, drawn by bob

[Bead Pages](../README.md) / bob-cli-99

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8z.md) · **Assignee:** `bob-cli-99.land`
**Created:** 2026-10-18 13:02:21 EDT
**Plan:** [202610/reading\_board.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/reading_board.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/reading_board.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/reading_board.md

<!-- sase:links:end -->

## Description

dash_references opens on a calm, read-only Reading Board (📖 Reading · ⭐ Next · 📥 Ready · 💤 Snoozed) whose lanes, wake dates, and waiting-on reasons come from `bob ref list` JSON, so the board, the terminal, and Bob Mac Capture always agree on what can be read now.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-99.1](bob-cli-99.1.md) | Reading-task facts and blocked reasons in bob ref JSON | ✓ closed | medium | 2026-10-18 | 1 | 1 |
| [bob-cli-99.2](bob-cli-99.2.md) | Board data path and pure lane models | ✓ closed | medium | 2026-10-18 | 1 | 1 |
| [bob-cli-99.3](bob-cli-99.3.md) | The bob-reading-board block, interaction, and look | ◐ in_progress | medium | 2026-10-18 | 1 | 0 |
| [bob-cli-99.4](bob-cli-99.4.md) | Put it on dash\_references, document, verify live | ◐ in_progress | small | 2026-10-18 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-99: Reading Board — a read-only kanban of the reading queue, drawn by bob [in_progress]"]
    n1["bob-cli-99.1: Reading-task facts and blocked reasons in bob ref JSON [closed]"]
    n2["bob-cli-99.2: Board data path and pure lane models [closed]"]
    n3["bob-cli-99.3: The bob-reading-board block, interaction, and look [in_progress]"]
    n4["bob-cli-99.4: Put it on dash_references, document, verify live [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n1 -.-> n4
    n2 -.-> n3
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-99.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.1/README.md) | [bob-cli-99.1](bob-cli-99.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-99.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-99.2.md) | [bob-cli-99.2](bob-cli-99.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-99.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.3/README.md) | [bob-cli-99.3](bob-cli-99.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-99.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.4/README.md) | [bob-cli-99.4](bob-cli-99.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-99.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.land/README.md) | [bob-cli-99](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b88195e`](https://github.com/bobs-org/bob-cli/commit/b88195e7d5b1f40ecca031260dd32922edfc0721) | feat(ref): add blocked\_by reasons and task priority/scheduled | [bob-cli-99.1](bob-cli-99.1.md) | 2026-10-18 14:06:48 EDT |
| bob-plugins | [`bob-plugins@8a0be74`](https://github.com/bobs-org/bob-plugins/commit/8a0be74b5d590a5b3fcbb953b5b4e6fcd4086adb) | feat(reading-board): add board data and lane models | [bob-cli-99.2](bob-cli-99.2.md) | 2026-10-18 14:45:32 EDT |
