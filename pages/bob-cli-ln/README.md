# Bead: bob-cli-ln — Generated "## Areas" catalogs for area notes and the area root

[Bead Pages](../README.md) / bob-cli-ln

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e2.md) · **Assignee:** `bob-cli-ln.land`
**Created:** 2026-11-14 16:33:03 EST
**Plan:** [202611/areas\_catalog.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/areas_catalog.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/areas_catalog.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/areas_catalog.md

<!-- sase:links:end -->

## Description

Every area note with sub-areas, and the root note `[[area]]` resolves to (today `area.md`), carries a bob-owned, nested `## Areas` catalog that stays correct through `bob areas sync` and nightly, always sits above `## Projects`, is protected from capture, turns the "areas parent only areas" convention into checked findings, and renders as a calm, colored map card in Obsidian while staying readable as plain Markdown everywhere else.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ln.1](bob-cli-ln.1.md) | Shared catalog engine - AREAS spec, placement order, heading adoption, capture guard | ✓ closed | medium | 2026-11-14 | 1 | 1 |
| [bob-cli-ln.2](bob-cli-ln.2.md) | Area graph and pure catalog planner | ◐ in_progress | medium | 2026-11-14 | 1 | 1 |
| [bob-cli-ln.3](bob-cli-ln.3.md) | bob areas list and check | ◐ in_progress | medium | 2026-11-14 | 1 | 0 |
| [bob-cli-ln.4](bob-cli-ln.4.md) | bob areas sync, nightly step, and Highlights coverage | ◐ in_progress | medium | 2026-11-14 | 1 | 0 |
| [bob-cli-ln.5](bob-cli-ln.5.md) | bob-ledger-tools Areas card shell | ◐ in_progress | medium | 2026-11-14 | 1 | 0 |
| [bob-cli-ln.6](bob-cli-ln.6.md) | Areas card folds, chips, tooltips, and add-summary | ◐ in_progress | medium | 2026-11-14 | 1 | 0 |
| [bob-cli-ln.7](bob-cli-ln.7.md) | Decision record and glossary update | ◐ in_progress | small | 2026-11-14 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ln: Generated \"## Areas\" catalogs for area notes and the area root [in_progress]"]
    n1["bob-cli-ln.1: Shared catalog engine - AREAS spec, placement order, heading adoption, capture guard [closed]"]
    n2["bob-cli-ln.2: Area graph and pure catalog planner [in_progress]"]
    n3["bob-cli-ln.3: bob areas list and check [in_progress]"]
    n4["bob-cli-ln.4: bob areas sync, nightly step, and Highlights coverage [in_progress]"]
    n5["bob-cli-ln.5: bob-ledger-tools Areas card shell [in_progress]"]
    n6["bob-cli-ln.6: Areas card folds, chips, tooltips, and add-summary [in_progress]"]
    n7["bob-cli-ln.7: Decision record and glossary update [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
    n3 -.-> n5
    n4 -.-> n6
    n4 -.-> n7
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ln.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.1/README.md) | [bob-cli-ln.1](bob-cli-ln.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ln.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ln.2.md) | [bob-cli-ln.2](bob-cli-ln.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ln.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.3/README.md) | [bob-cli-ln.3](bob-cli-ln.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-ln.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.4/README.md) | [bob-cli-ln.4](bob-cli-ln.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-ln.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.5/README.md) | [bob-cli-ln.5](bob-cli-ln.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-ln.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.6/README.md) | [bob-cli-ln.6](bob-cli-ln.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-ln.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.7/README.md) | [bob-cli-ln.7](bob-cli-ln.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-ln.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.land/README.md) | [bob-cli-ln](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`13fdf78`](https://github.com/bobs-org/bob-cli/commit/13fdf78d201c696cb0501c1b6b60c45246db1b45) | feat(areas): shared catalog engine for generated Areas catalogs | [bob-cli-ln.1](bob-cli-ln.1.md) | 2026-11-14 17:15:25 EST |
| bob-cli | [`719dbd4`](https://github.com/bobs-org/bob-cli/commit/719dbd45cbf4eaf21cdf96bd3f46eaa6da2c5974) | feat(areas): validated area graph and pure nested catalog planner | [bob-cli-ln.2](bob-cli-ln.2.md) | 2026-11-14 19:10:11 EST |
