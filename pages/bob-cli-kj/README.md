# Bead: bob-cli-kj — Fix the impact-ranked open task beads

[Bead Pages](../README.md) / bob-cli-kj

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.land`
**Created:** 2026-11-11 17:20:03 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/impact_ranked_bead_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md

<!-- sase:links:end -->

## Description

The three red verification gates every landing re-triages (macOS CI, bob-cli docs-check, the bob-plugins wikilink perf budgets) are green again and the two diagnosed user-facing bugs are fixed, so beads bob-cli-jx, -jy, -h9, -jz, -jr, -k8, -f8, and -hp can be closed with verified evidence.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-kj.1](bob-cli-kj.1.md) | Isolation-correct alias test teardowns | ✓ closed | small | 2026-11-11 | 1 | 1 |
| [bob-cli-kj.2](bob-cli-kj.2.md) | Mounted reference pages back under the word cap | ◐ in_progress | medium | 2026-11-11 | 1 | 1 |
| [bob-cli-kj.3](bob-cli-kj.3.md) | Stats RefCell double-borrow panic | ◐ in_progress | small | 2026-11-11 | 1 | 0 |
| [bob-cli-kj.4](bob-cli-kj.4.md) | Configured-timezone created stamps | ◐ in_progress | small | 2026-11-11 | 1 | 0 |
| [bob-cli-kj.5](bob-cli-kj.5.md) | Deterministic alias-tip CI timeouts | ✓ closed | large | 2026-11-11 | 1 | 0 |
| [bob-cli-kj.6](bob-cli-kj.6.md) | Task-wikilink CPU budget investigation | ◐ in_progress | large | 2026-11-11 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-kj: Fix the impact-ranked open task beads [in_progress]"]
    n1["bob-cli-kj.1: Isolation-correct alias test teardowns [closed]"]
    n2["bob-cli-kj.2: Mounted reference pages back under the word cap [in_progress]"]
    n3["bob-cli-kj.3: Stats RefCell double-borrow panic [in_progress]"]
    n4["bob-cli-kj.4: Configured-timezone created stamps [in_progress]"]
    n5["bob-cli-kj.5: Deterministic alias-tip CI timeouts [closed]"]
    n6["bob-cli-kj.6: Task-wikilink CPU budget investigation [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kj.1/README.md) | [bob-cli-kj.1](bob-cli-kj.1.md) | 1 |
| [bbugyi200.athena.bob-cli-kj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kj.2/README.md) | [bob-cli-kj.2](bob-cli-kj.2.md) | 1 |
| [bbugyi200.athena.bob-cli-kj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.3.md) | [bob-cli-kj.3](bob-cli-kj.3.md) | 0 |
| [bbugyi200.athena.bob-cli-kj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kj.4/README.md) | [bob-cli-kj.4](bob-cli-kj.4.md) | 0 |
| [bbugyi200.athena.bob-cli-kj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.5.md) | [bob-cli-kj.5](bob-cli-kj.5.md) | 0 |
| [bbugyi200.athena.bob-cli-kj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.6.md) | [bob-cli-kj.6](bob-cli-kj.6.md) | 0 |
| [bbugyi200.athena.bob-cli-kj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kj.land/README.md) | [bob-cli-kj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1e83c03`](https://github.com/bobs-org/bob-mac-capture/commit/1e83c032217a9d6c90827ee467e5c60b57069d88) | fix(tests): isolate alias ledger teardown on main actor | [bob-cli-kj.1](bob-cli-kj.1.md) | 2026-11-11 17:32:23 EST |
| bob-mac-capture | [`bob-mac-capture@2007294`](https://github.com/bobs-org/bob-mac-capture/commit/2007294cdc29ef379f6959ef2f05b87d75681e45) | docs: trim mounted reference pages back under the word cap | [bob-cli-kj.2](bob-cli-kj.2.md) | 2026-11-11 17:54:54 EST |
