# Bead: bob-cli-dm — Task theme suggestions: suggest, explain, remember

[Bead Pages](../README.md) / bob-cli-dm

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2s.linker.w0.md) · **Assignee:** `bob-cli-dm.land`
**Created:** 2026-10-28 08:45:53 EDT
**Plan:** [202610/task\_theme\_suggestions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_suggestions.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/task_theme_suggestions.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_suggestions.md

<!-- sase:links:end -->

## Description

Every task-aware Pomodoro menu preselects the theme a task most likely belongs to, says why in the same words on every surface, and remembers deliberate exceptions as a `[theme:: X]` field on the task line. One Rust-owned rule drives bob-cli, the Obsidian plugins mirror it under shared vectors, and Bob Mac Capture renders bob's JSON.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-dm.1](bob-cli-dm.1.md) | bob-cli suggestion rule, task field, and \`bob themes suggest\` | ✓ closed | large | 2026-10-28 | 1 | 0 |
| [bob-cli-dm.2](bob-cli-dm.2.md) | Suggestions in capture completion and \`bob ref today\` | ✓ closed | medium | 2026-10-28 | 1 | 1 |
| [bob-cli-dm.3](bob-cli-dm.3.md) | Theme rename covers note defaults and task fields | ✓ closed | medium | 2026-10-28 | 1 | 1 |
| [bob-cli-dm.4](bob-cli-dm.4.md) | Capture remembers deliberate \`#NAME\` choices | ✓ closed | large | 2026-10-28 | 1 | 0 |
| [bob-cli-dm.5](bob-cli-dm.5.md) | Ledger Tools mirror, field writer, and task-theme pill | ✓ closed | large | 2026-10-28 | 1 | 0 |
| [bob-cli-dm.6](bob-cli-dm.6.md) | Link to today preselects, explains, and remembers | ◐ in_progress | large | 2026-10-28 | 1 | 0 |
| [bob-cli-dm.7](bob-cli-dm.7.md) | Task Card theme stage and successor retarget | ◐ in_progress | large | 2026-10-28 | 1 | 0 |
| [bob-cli-dm.8](bob-cli-dm.8.md) | Bob Mac Capture renders suggestions and theme changes | ○ open | medium | 2026-10-28 | 1 | 0 |
| [bob-cli-dm.9](bob-cli-dm.9.md) | Seed the first note defaults in the vault | ◐ in_progress | xsmall | 2026-10-28 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-dm: Task theme suggestions: suggest, explain, remember [in_progress]"]
    n1["bob-cli-dm.1: bob-cli suggestion rule, task field, and `bob themes suggest` [closed]"]
    n2["bob-cli-dm.1.1: Rust task theme suggestions and canonical task fields [closed]"]
    n3["bob-cli-dm.1.1.1: Implement task theme rules and shared vectors [closed]"]
    n4["bob-cli-dm.1.1.2: Expose suggestions and unknown note defaults [closed]"]
    n5["bob-cli-dm.1.1.3: Verify field preservation and publish the contract [closed]"]
    n6["bob-cli-dm.2: Suggestions in capture completion and `bob ref today` [closed]"]
    n7["bob-cli-dm.3: Theme rename covers note defaults and task fields [closed]"]
    n8["bob-cli-dm.4: Capture remembers deliberate `#NAME` choices [closed]"]
    n9["bob-cli-dm.5: Ledger Tools mirror, field writer, and task-theme pill [closed]"]
    n10["bob-cli-dm.5.1: Ledger task-theme mirror and pills [closed]"]
    n11["bob-cli-dm.5.1.1: Mirror the task-theme rule and expose the synchronous API [closed]"]
    n12["bob-cli-dm.5.1.2: Render task-theme pills in Live Preview and activate PT6 colors [closed]"]
    n13["bob-cli-dm.5.1.3: Render task-theme pills in Reading view and query rows [closed]"]
    n14["bob-cli-dm.6: Link to today preselects, explains, and remembers [in_progress]"]
    n15["bob-cli-dm.7: Task Card theme stage and successor retarget [in_progress]"]
    n16["bob-cli-dm.8: Bob Mac Capture renders suggestions and theme changes [open]"]
    n17["bob-cli-dm.9: Seed the first note defaults in the vault [in_progress]"]
    n0 --> n1
    n1 --> n2
    n2 --> n3
    n2 --> n4
    n2 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n9 --> n10
    n10 --> n11
    n10 --> n12
    n10 --> n13
    n0 --> n14
    n0 --> n15
    n0 --> n16
    n0 --> n17
    n1 -.-> n6
    n1 -.-> n7
    n1 -.-> n9
    n3 -.-> n4
    n4 -.-> n5
    n6 -.-> n8
    n6 -.-> n14
    n6 -.-> n16
    n7 -.-> n8
    n7 -.-> n14
    n8 -.-> n16
    n8 -.-> n17
    n9 -.-> n14
    n11 -.-> n12
    n12 -.-> n13
    n14 -.-> n15
    n14 -.-> n17
    n16 -.-> n17
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.1.md) | [bob-cli-dm.1](bob-cli-dm.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-dm.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.1.1.1.md) | [bob-cli-dm.1.1.1](bob-cli-dm.1.1.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-dm.1.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.1.1.2.md) | [bob-cli-dm.1.1.2](bob-cli-dm.1.1.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-dm.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.1.1.3/README.md) | [bob-cli-dm.1.1.3](bob-cli-dm.1.1.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-dm.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.1.1.land.md) | [bob-cli-dm.1.1](bob-cli-dm.1.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-dm.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.2.md) | [bob-cli-dm.2](bob-cli-dm.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-dm.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.3/README.md) | [bob-cli-dm.3](bob-cli-dm.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-dm.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.4.md) | [bob-cli-dm.4](bob-cli-dm.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-dm.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.5.md) | [bob-cli-dm.5](bob-cli-dm.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-dm.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.5.1.1/README.md) | [bob-cli-dm.5.1.1](bob-cli-dm.5.1.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-dm.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.5.1.2/README.md) | [bob-cli-dm.5.1.2](bob-cli-dm.5.1.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-dm.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.5.1.3/README.md) | [bob-cli-dm.5.1.3](bob-cli-dm.5.1.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-dm.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.5.1.land.md) | [bob-cli-dm.5.1](bob-cli-dm.5.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-dm.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.6/README.md) | [bob-cli-dm.6](bob-cli-dm.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-dm.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.7/README.md) | [bob-cli-dm.7](bob-cli-dm.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-dm.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.8/README.md) | [bob-cli-dm.8](bob-cli-dm.8.md) | 0 |
| [bbugyi200.apollo.bob-cli-dm.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.9/README.md) | [bob-cli-dm.9](bob-cli-dm.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-dm.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.land/README.md) | [bob-cli-dm](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a1b8766`](https://github.com/bobs-org/bob-cli/commit/a1b8766bbf6afd54c80c3aba73d496861288e11f) | feat(themes): add task theme suggestion model and field helpers | [bob-cli-dm.1.1.1](bob-cli-dm.1.1.1.md) | 2026-10-28 10:16:59 EDT |
| bob-cli | [`9409bfa`](https://github.com/bobs-org/bob-cli/commit/9409bfa58011ed66aeb1ccf3c0a7125a332748d3) | feat(themes): explain task suggestions and cache unknown note defaults | [bob-cli-dm.1.1.2](bob-cli-dm.1.1.2.md) | 2026-10-28 16:01:52 EDT |
| bob-cli | [`c624347`](https://github.com/bobs-org/bob-cli/commit/c6243477c4cbc7778cfe4749bb9c6d24a40f2b9e) | feat(themes): publish PT13 pomodoro-theme contract and preservation regressions | [bob-cli-dm.1.1.3](bob-cli-dm.1.1.3.md) | 2026-10-28 16:52:22 EDT |
| bob-cli | [`fc59428`](https://github.com/bobs-org/bob-cli/commit/fc594281b1f623738b6ee0f71c8ff86df0285246) | fix(themes): repair task-theme scalars, placement, and unused-code gates | [bob-cli-dm.1.1](bob-cli-dm.1.1.md) | 2026-10-28 17:41:19 EDT |
| bob-cli--plans | [`bob-cli--plans@7020103`](https://github.com/bobs-org/bob-cli--plans/commit/702010391ff5580edf863bb4f88c763acbf5eb6d) | docs(plan): mark task\_theme\_core done after bob-cli-dm.1.1 landing | [bob-cli-dm.1.1](bob-cli-dm.1.1.md) | 2026-10-28 17:42:16 EDT |
| bob-plugins | [`bob-plugins@25d864e`](https://github.com/bobs-org/bob-plugins/commit/25d864e2af1e5039e4644f1f4b260d3fe0767e6c) | feat(plugins): add task-theme API and picker support | [bob-cli-dm.5.1.1](bob-cli-dm.5.1.1.md) | 2026-10-28 18:11:32 EDT |
| bob-cli | [`13b2430`](https://github.com/bobs-org/bob-cli/commit/13b243032a212a5671d569d438b7f5d2f880b80c) | feat(themes): rewrite note defaults and task fields on rename | [bob-cli-dm.3](bob-cli-dm.3.md) | 2026-10-28 18:23:08 EDT |
| bob-cli | [`ac13ab5`](https://github.com/bobs-org/bob-cli/commit/ac13ab543347f173aa729744bd08b98d637fc804) | feat(capture): suggest task themes in completion and ref today | [bob-cli-dm.2](bob-cli-dm.2.md) | 2026-10-28 18:35:38 EDT |
| bob-plugins | [`bob-plugins@4721a74`](https://github.com/bobs-org/bob-plugins/commit/4721a74dee66a36279cc6032bf6f5fa708650064) | feat(ledger-tools): live preview task theme marks with editor decorations | [bob-cli-dm.5.1.2](bob-cli-dm.5.1.2.md) | 2026-10-28 18:40:03 EDT |
| bob-plugins | [`bob-plugins@ae40495`](https://github.com/bobs-org/bob-plugins/commit/ae40495ab5f98a458358dcfb62dffb5be51ccf98) | feat(ledger-tools): render task-theme pills in Reading view and query rows | [bob-cli-dm.5.1.3](bob-cli-dm.5.1.3.md) | 2026-10-28 19:09:07 EDT |
| bob-plugins | [`bob-plugins@bc245fc`](https://github.com/bobs-org/bob-plugins/commit/bc245fc054c99bfcc0d67f2aa978f9c01a01999b) | fix(ledger-tools): land PT13 task-theme pills across editor and rendered views | [bob-cli-dm.5.1](bob-cli-dm.5.1.md) | 2026-10-28 20:00:06 EDT |
| bob-cli--plans | [`bob-cli--plans@236ca9c`](https://github.com/bobs-org/bob-cli--plans/commit/236ca9c3260f970042e05c03569494d4c03ad3b7) | docs(plan): mark ledger task-theme mirror epic done | [bob-cli-dm.5.1](bob-cli-dm.5.1.md) | 2026-10-28 20:01:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dk.land][1] | Check whether the later task-theme epic depends on or overlaps configured themes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dk.land/README.md

<!-- sase:referenced-by:end -->
