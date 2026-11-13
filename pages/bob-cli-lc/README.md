# Bead: bob-cli-lc — Bank, weekly — file every row with one key

[Bead Pages](../README.md) / bob-cli-lc

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c7.md) · **Assignee:** `bob-cli-lc.land`
**Created:** 2026-11-13 10:55:28 EST
**Plan:** [202611/bank\_weekly\_category\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_weekly_category_walk.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_weekly_category_walk.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_weekly_category_walk.md

<!-- sase:links:end -->

## Description

Bank tracking becomes one Monday chore: a Wells Fargo download link, one import command, then Ctrl+Enter on each waiting bank row opens a Category card where a single key ticks the row, files its category from Bryan's own list, and lands the cursor on the next waiting row, so a week of transactions takes about two minutes.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-lc.1](bob-cli-lc.1.md) | One weekly Bank chore with the Wells Fargo link | ✓ closed | small | 2026-11-13 | 1 | 0 |
| [bob-cli-lc.2](bob-cli-lc.2.md) | Clean Wells Fargo QFX payees and merchant keys | ✓ closed | medium | 2026-11-13 | 1 | 1 |
| [bob-cli-lc.3](bob-cli-lc.3.md) | Category hotkeys, groups, hidden, and row suggestions | ◐ in_progress | medium | 2026-11-13 | 1 | 0 |
| [bob-cli-lc.4](bob-cli-lc.4.md) | Bryan's taxonomy in bank.md and clean seed rows | ◐ in_progress | small | 2026-11-13 | 1 | 0 |
| [bob-cli-lc.5](bob-cli-lc.5.md) | Pure Category card, write, and advance models | ◐ in_progress | medium | 2026-11-13 | 1 | 0 |
| [bob-cli-lc.6](bob-cli-lc.6.md) | The Category card, the walk, and Bank set category | ◐ in_progress | medium | 2026-11-13 | 1 | 0 |
| [bob-cli-lc.7](bob-cli-lc.7.md) | Ctrl+Enter hand-off, jump history, real-Obsidian proof, deploy | ◐ in_progress | medium | 2026-11-13 | 1 | 0 |
| [bob-cli-lc.8](bob-cli-lc.8.md) | Weekly guide, contract docs, memory, and the trial | ◐ in_progress | medium | 2026-11-13 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-lc: Bank, weekly — file every row with one key [in_progress]"]
    n1["bob-cli-lc.1: One weekly Bank chore with the Wells Fargo link [closed]"]
    n2["bob-cli-lc.2: Clean Wells Fargo QFX payees and merchant keys [closed]"]
    n3["bob-cli-lc.3: Category hotkeys, groups, hidden, and row suggestions [in_progress]"]
    n4["bob-cli-lc.4: Bryan's taxonomy in bank.md and clean seed rows [in_progress]"]
    n5["bob-cli-lc.5: Pure Category card, write, and advance models [in_progress]"]
    n6["bob-cli-lc.6: The Category card, the walk, and Bank set category [in_progress]"]
    n7["bob-cli-lc.7: Ctrl+Enter hand-off, jump history, real-Obsidian proof, deploy [in_progress]"]
    n8["bob-cli-lc.8: Weekly guide, contract docs, memory, and the trial [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n1 -.-> n8
    n2 -.-> n3
    n3 -.-> n4
    n3 -.-> n5
    n4 -.-> n7
    n5 -.-> n6
    n6 -.-> n7
    n7 -.-> n8
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.1/README.md) | [bob-cli-lc.1](bob-cli-lc.1.md) | 0 |
| [bbugyi200.athena.bob-cli-lc.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lc.2.md) | [bob-cli-lc.2](bob-cli-lc.2.md) | 1 |
| [bbugyi200.athena.bob-cli-lc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.3/README.md) | [bob-cli-lc.3](bob-cli-lc.3.md) | 0 |
| [bbugyi200.athena.bob-cli-lc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.4/README.md) | [bob-cli-lc.4](bob-cli-lc.4.md) | 0 |
| [bbugyi200.athena.bob-cli-lc.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.5/README.md) | [bob-cli-lc.5](bob-cli-lc.5.md) | 0 |
| [bbugyi200.athena.bob-cli-lc.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.6/README.md) | [bob-cli-lc.6](bob-cli-lc.6.md) | 0 |
| [bbugyi200.athena.bob-cli-lc.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.7/README.md) | [bob-cli-lc.7](bob-cli-lc.7.md) | 0 |
| [bbugyi200.athena.bob-cli-lc.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.8/README.md) | [bob-cli-lc.8](bob-cli-lc.8.md) | 0 |
| [bbugyi200.athena.bob-cli-lc.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.land/README.md) | [bob-cli-lc](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d6d755a`](https://github.com/bobs-org/bob-cli/commit/d6d755a1da262080f5a78196a653f5f296017475) | feat(bank): clean QFX payees and merchant keys | [bob-cli-lc.2](bob-cli-lc.2.md) | 2026-11-13 12:08:10 EST |
