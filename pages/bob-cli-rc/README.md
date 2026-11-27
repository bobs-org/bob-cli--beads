# Bead: bob-cli-rc — Ctrl+J / Ctrl+K Section Map

[Bead Pages](../README.md) / bob-cli-rc

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hg](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hg.md) · **Assignee:** `bob-cli-rc.land`
**Created:** 2026-11-27 15:06:05 EST
**Plan:** [202611/ctrl\_jk\_section\_map.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ctrl_jk_section_map.md)

## Description

Every successful Ctrl+J / Ctrl+K section jump in Obsidian briefly shows a passive, beautiful Section Map in the jumping pane: the note's headings, where you are, where you came from, where the next press lands, and when a press wrapped. The map is built from the same scanner and jump function the keys use, so it never disagrees with them, and it never takes focus, keys, or clicks.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-rc.1](bob-cli-rc.1.md) | Shared heading scanner and Section Map model | ✓ closed | medium | 2026-11-27 | 1 | 2 |
| [bob-cli-rc.2](bob-cli-rc.2.md) | Section Map card painter, placement, and styles | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |
| [bob-cli-rc.3](bob-cli-rc.3.md) | Jump integration, lifecycle controller, landing flash, and peek | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |
| [bob-cli-rc.4](bob-cli-rc.4.md) | Real-Obsidian acceptance, docs, and deploy | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-rc: Ctrl+J / Ctrl+K Section Map [in_progress]"]
    n1["bob-cli-rc.1: Shared heading scanner and Section Map model [closed]"]
    n2["bob-cli-rc.2: Section Map card painter, placement, and styles [in_progress]"]
    n3["bob-cli-rc.3: Jump integration, lifecycle controller, landing flash, and peek [in_progress]"]
    n4["bob-cli-rc.4: Real-Obsidian acceptance, docs, and deploy [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n1 -.-> n3
    n2 -.-> n3
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rc.1.md) | [bob-cli-rc.1](bob-cli-rc.1.md) | 2 |
| [bbugyi200.athena.bob-cli-rc.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rc.2/README.md) | [bob-cli-rc.2](bob-cli-rc.2.md) | 0 |
| [bbugyi200.athena.bob-cli-rc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rc.3/README.md) | [bob-cli-rc.3](bob-cli-rc.3.md) | 0 |
| [bbugyi200.athena.bob-cli-rc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rc.4/README.md) | [bob-cli-rc.4](bob-cli-rc.4.md) | 0 |
| [bbugyi200.athena.bob-cli-rc.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rc.land/README.md) | [bob-cli-rc](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@44425a4`](https://github.com/bobs-org/bob-plugins/commit/44425a4929a93d170b1ed0845d7ded3b5ef9adf3) | feat(navigation): add shared Section Map model | [bob-cli-rc.1](bob-cli-rc.1.md) | 2026-11-27 15:24:25 EST |
| bob-plugins | [`bob-plugins@d4edb02`](https://github.com/bobs-org/bob-plugins/commit/d4edb022697087d994ded538800a77a00063af2a) | fix(navigation): refresh the Section Map bundle for single-heading notes | [bob-cli-rc.1](bob-cli-rc.1.md) | 2026-11-27 15:45:38 EST |
