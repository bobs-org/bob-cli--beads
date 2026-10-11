# Bead: bob-cli-6l — Daily Stats — derived daily metrics, a review journal, bob stats, and an Obsidian Stats page

[Bead Pages](../README.md) / bob-cli-6l

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.0u.linker.w0/README.md) · **Assignee:** `bob-cli-6l.land`
**Created:** 2026-10-11 07:01:05 EDT
**Plan:** [202610/daily\_stats.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/daily_stats.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats.md

<!-- sase:links:end -->

## Description

Bryan can open Stats (Obsidian) or run `bob stats` (terminal) during the weekly prune, understand how the last weeks went in about a minute, trust where every number came from, and add a new daily metric with a few lines of config — with no daily logging habit and no data written that the vault already keeps.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-6l.1](bob-cli-6l.1.md) | Start the clock — the review journal writer | ✓ closed | medium | 2026-10-11 | 1 | 1 |
| [bob-cli-6l.2](bob-cli-6l.2.md) | The stats engine in bob-cli | ◐ in_progress | large | 2026-10-11 | 1 | 0 |
| [bob-cli-6l.3](bob-cli-6l.3.md) | The bob stats command | ◐ in_progress | medium | 2026-10-11 | 1 | 0 |
| [bob-cli-6l.4](bob-cli-6l.4.md) | Obsidian Stats page — data path, tiles, and table | ◐ in_progress | medium | 2026-10-11 | 1 | 0 |
| [bob-cli-6l.5](bob-cli-6l.5.md) | Obsidian Stats page — focus chart, context panels, and interaction | ◐ in_progress | large | 2026-10-11 | 1 | 0 |
| [bob-cli-6l.6](bob-cli-6l.6.md) | Rollout — real-vault verification, docs, and memory | ◐ in_progress | small | 2026-10-11 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-6l: Daily Stats — derived daily metrics, a review journal, bob stats, and an Obsidian Stats page [in_progress]"]
    n1["bob-cli-6l.1: Start the clock — the review journal writer [closed]"]
    n2["bob-cli-6l.2: The stats engine in bob-cli [in_progress]"]
    n3["bob-cli-6l.2.1: Daily Stats engine for bob-cli-6l.2 [in_progress]"]
    n4["bob-cli-6l.2.1.1: Define the stats model and configurable metric registry [closed]"]
    n5["bob-cli-6l.2.1.2: Build the single-pass vault and journal index [closed]"]
    n6["bob-cli-6l.2.1.3: Implement ranges, grouping, summaries, and display strings [closed]"]
    n7["bob-cli-6l.2.1.4: Evaluate Pomodoro, task, checklist, and field metrics [in_progress]"]
    n8["bob-cli-6l.2.1.5: Evaluate review answers and formulas [in_progress]"]
    n9["bob-cli-6l.2.1.6: Assemble compute, prove the schema, and document the engine [in_progress]"]
    n10["bob-cli-6l.3: The bob stats command [in_progress]"]
    n11["bob-cli-6l.4: Obsidian Stats page — data path, tiles, and table [in_progress]"]
    n12["bob-cli-6l.5: Obsidian Stats page — focus chart, context panels, and interaction [in_progress]"]
    n13["bob-cli-6l.6: Rollout — real-vault verification, docs, and memory [in_progress]"]
    n0 --> n1
    n0 --> n2
    n2 --> n3
    n3 --> n4
    n3 --> n5
    n3 --> n6
    n3 --> n7
    n3 --> n8
    n3 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n1 -.-> n2
    n2 -.-> n10
    n4 -.-> n5
    n4 -.-> n6
    n5 -.-> n7
    n6 -.-> n9
    n7 -.-> n8
    n8 -.-> n9
    n10 -.-> n11
    n11 -.-> n12
    n12 -.-> n13
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.1/README.md) | [bob-cli-6l.1](bob-cli-6l.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.2.md) | [bob-cli-6l.2](bob-cli-6l.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.1/README.md) | [bob-cli-6l.2.1.1](bob-cli-6l.2.1.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.2.1.2.md) | [bob-cli-6l.2.1.2](bob-cli-6l.2.1.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.3/README.md) | [bob-cli-6l.2.1.3](bob-cli-6l.2.1.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.4/README.md) | [bob-cli-6l.2.1.4](bob-cli-6l.2.1.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.2.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.5/README.md) | [bob-cli-6l.2.1.5](bob-cli-6l.2.1.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.2.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.6/README.md) | [bob-cli-6l.2.1.6](bob-cli-6l.2.1.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.land/README.md) | [bob-cli-6l.2.1](bob-cli-6l.2.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.3/README.md) | [bob-cli-6l.3](bob-cli-6l.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.4/README.md) | [bob-cli-6l.4](bob-cli-6l.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5/README.md) | [bob-cli-6l.5](bob-cli-6l.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.6/README.md) | [bob-cli-6l.6](bob-cli-6l.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.land/README.md) | [bob-cli-6l](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1023e6c`](https://github.com/bobs-org/bob-cli/commit/1023e6cb14cfbf68d8a1ef43cf288e855d6ab6f7) | feat(stats): add review answer journal contract | [bob-cli-6l.1](bob-cli-6l.1.md) | 2026-10-11 07:21:27 EDT |
| bob-cli | [`d513f01`](https://github.com/bobs-org/bob-cli/commit/d513f013bb713434f631f488c00bd531487b1a36) | feat(stats): define engine types, isolated config, and metric registry | [bob-cli-6l.2.1.1](bob-cli-6l.2.1.1.md) | 2026-10-11 08:29:03 EDT |
| bob-cli | [`e27fe70`](https://github.com/bobs-org/bob-cli/commit/e27fe7020e80c1856899cc757f4b0c1e0675076d) | feat(stats): build single-pass vault and journal index | [bob-cli-6l.2.1.2](bob-cli-6l.2.1.2.md) | 2026-10-11 08:58:30 EDT |
| bob-cli | [`7f14f5f`](https://github.com/bobs-org/bob-cli/commit/7f14f5fd47d80227adc7c376d1523e2933e881af) | feat(stats): implement range and series reporting | [bob-cli-6l.2.1.3](bob-cli-6l.2.1.3.md) | 2026-10-11 09:08:21 EDT |
