# Bead: bob-cli-bj — Relation label vocabulary — a chooser that works, hidden and one-off labels, and one global rename

[Bead Pages](../README.md) / bob-cli-bj

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2e.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2e.linker.w0.md) · **Assignee:** `bob-cli-bj.land`
**Created:** 2026-10-24 13:34:45 EDT
**Plan:** [202610/relation\_label\_vocabulary.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/relation_label_vocabulary.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md

<!-- sase:links:end -->

## Description

The Bob Mac Capture relation card is a reliable, beautiful chooser: Ctrl+N/P move a visible highlight through existing relation labels, Tab accepts, and nothing collapses. Relation labels can be hidden from suggestions (Ctrl+D, with undo), shown again (Ctrl+H section) and unhidden, created hidden with `~note:id||label` (with a clear warning when that hides an existing label), and renamed everywhere — from the card, `bob relations rename`, and Obsidian — in one previewed, revertable commit.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-bj.1](bob-cli-bj.1.md) | Mac relation card as a navigate-then-accept chooser | ✓ closed | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bj.10](bob-cli-bj.10.md) | Obsidian rename mode and the relation labels command | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bj.11](bob-cli-bj.11.md) | Decision records, docs sweep, and end-to-end acceptance | ◐ in_progress | small | 2026-10-24 | 1 | 0 |
| [bob-cli-bj.2](bob-cli-bj.2.md) | Shared preference journal, relation label catalog, and bob relations list/hide/unhide | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.3](bob-cli-bj.3.md) | capture-complete relation\_label rows from the catalog | ◐ in_progress | small | 2026-10-24 | 1 | 0 |
| [bob-cli-bj.4](bob-cli-bj.4.md) | Shared vault-rewrite transaction extracted from bob themes rename | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.5](bob-cli-bj.5.md) | The \`\|\|\` one-off relation label capture syntax | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bj.6](bob-cli-bj.6.md) | bob relations rename across every note, done/ included | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bj.7](bob-cli-bj.7.md) | Mac card hide, one-off, Hidden section, and warnings | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bj.8](bob-cli-bj.8.md) | Obsidian label stage parity, JS mirrors, and api.relationLabels | ✓ closed | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bj.9](bob-cli-bj.9.md) | Mac card rename mode | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-bj: Relation label vocabulary — a chooser that works, hidden and one-off labels, and one global rename [in_progress]"]
    n1["bob-cli-bj.1: Mac relation card as a navigate-then-accept chooser [closed]"]
    n2["bob-cli-bj.10: Obsidian rename mode and the relation labels command [in_progress]"]
    n3["bob-cli-bj.11: Decision records, docs sweep, and end-to-end acceptance [in_progress]"]
    n4["bob-cli-bj.2: Shared preference journal, relation label catalog, and bob relations list/hide/unhide [closed]"]
    n5["bob-cli-bj.3: capture-complete relation_label rows from the catalog [in_progress]"]
    n6["bob-cli-bj.4: Shared vault-rewrite transaction extracted from bob themes rename [closed]"]
    n7["bob-cli-bj.5: The `||` one-off relation label capture syntax [in_progress]"]
    n8["bob-cli-bj.6: bob relations rename across every note, done/ included [in_progress]"]
    n9["bob-cli-bj.7: Mac card hide, one-off, Hidden section, and warnings [in_progress]"]
    n10["bob-cli-bj.8: Obsidian label stage parity, JS mirrors, and api.relationLabels [closed]"]
    n11["bob-cli-bj.9: Mac card rename mode [in_progress]"]
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
    n0 --> n11
    n1 -.-> n9
    n2 -.-> n3
    n4 -.-> n5
    n4 -.-> n6
    n4 -.-> n10
    n5 -.-> n7
    n6 -.-> n8
    n7 -.-> n9
    n8 -.-> n2
    n8 -.-> n11
    n9 -.-> n11
    n10 -.-> n2
    n11 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.1.md) | [bob-cli-bj.1](bob-cli-bj.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.10/README.md) | [bob-cli-bj.10](bob-cli-bj.10.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.11/README.md) | [bob-cli-bj.11](bob-cli-bj.11.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.2/README.md) | [bob-cli-bj.2](bob-cli-bj.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.3/README.md) | [bob-cli-bj.3](bob-cli-bj.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.4/README.md) | [bob-cli-bj.4](bob-cli-bj.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.5/README.md) | [bob-cli-bj.5](bob-cli-bj.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.6/README.md) | [bob-cli-bj.6](bob-cli-bj.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.7/README.md) | [bob-cli-bj.7](bob-cli-bj.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.8/README.md) | [bob-cli-bj.8](bob-cli-bj.8.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.9/README.md) | [bob-cli-bj.9](bob-cli-bj.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.land/README.md) | [bob-cli-bj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`57d7761`](https://github.com/bobs-org/bob-cli/commit/57d77612109f72c1f51aecbcb43c6be106e7398b) | feat(relations): shared preference journal, label catalog, and bob relations list/hide/unhide | [bob-cli-bj.2](bob-cli-bj.2.md) | 2026-10-24 15:08:39 EDT |
| bob-cli | [`fd9380c`](https://github.com/bobs-org/bob-cli/commit/fd9380cbaefb8ceb481a914ca6490b6f70e54143) | refactor(themes): extract rename transaction into vault\_rewrite module | [bob-cli-bj.4](bob-cli-bj.4.md) | 2026-10-24 16:07:40 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bj.2][1] | epic context for phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.2/README.md

<!-- sase:referenced-by:end -->
