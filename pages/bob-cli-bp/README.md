# Bead: bob-cli-bp — Day strip — a compact daily-stats receipt at the bottom of Bob daily notes

[Bead Pages](../README.md) / bob-cli-bp

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2f.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2f.linker.w1.md) · **Assignee:** `bob-cli-bp.land`
**Created:** 2026-10-24 16:30:44 EDT
**Plan:** [202610/daily\_note\_day\_strip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_note_day_strip.md)

## Description

Every canonical daily note (`YYYY/YYYYMMDD.md`) ends with a quiet, beautiful Day strip of that day's own facts (Worked, Reviewed, Done, Created, Review closed, and the area time mix). It is painted from cache in the first frame, re-runs `bob stats` only while it is on screen and the data has changed and aged, and is never written into the note.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-bp.1](bob-cli-bp.1.md) | bob stats reads "not yet" for an unmet provisional boolean | ✓ closed | small | 2026-10-24 | 1 | 1 |
| [bob-cli-bp.2](bob-cli-bp.2.md) | Stats fetch service fixes for the Stats page and the strip | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bp.3](bob-cli-bp.3.md) | Day strip model, painter, styles, and preview matrix | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bp.4](bob-cli-bp.4.md) | Day strip data selection, refresh policy, fence, and Stats hand-off | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bp.5](bob-cli-bp.5.md) | Virtual Live Preview mount, controls, and plugin docs | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bp.6](bob-cli-bp.6.md) | Day strip contract in bob-cli docs and memory | ◐ in_progress | small | 2026-10-24 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-bp: Day strip — a compact daily-stats receipt at the bottom of Bob daily notes [in_progress]"]
    n1["bob-cli-bp.1: bob stats reads \"not yet\" for an unmet provisional boolean [closed]"]
    n2["bob-cli-bp.2: Stats fetch service fixes for the Stats page and the strip [in_progress]"]
    n3["bob-cli-bp.3: Day strip model, painter, styles, and preview matrix [in_progress]"]
    n4["bob-cli-bp.4: Day strip data selection, refresh policy, fence, and Stats hand-off [in_progress]"]
    n5["bob-cli-bp.5: Virtual Live Preview mount, controls, and plugin docs [in_progress]"]
    n6["bob-cli-bp.6: Day strip contract in bob-cli docs and memory [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n6
    n2 -.-> n3
    n2 -.-> n4
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bp.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.1/README.md) | [bob-cli-bp.1](bob-cli-bp.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-bp.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.2/README.md) | [bob-cli-bp.2](bob-cli-bp.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-bp.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.3/README.md) | [bob-cli-bp.3](bob-cli-bp.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-bp.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.4/README.md) | [bob-cli-bp.4](bob-cli-bp.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-bp.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.5/README.md) | [bob-cli-bp.5](bob-cli-bp.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-bp.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.6/README.md) | [bob-cli-bp.6](bob-cli-bp.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-bp.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.land/README.md) | [bob-cli-bp](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0fc6ebf`](https://github.com/bobs-org/bob-cli/commit/0fc6ebfaccaca03e00dab4f0ee6552db2c92834c) | fix(stats): mark unmet provisional booleans not yet | [bob-cli-bp.1](bob-cli-bp.1.md) | 2026-10-24 16:51:15 EDT |
