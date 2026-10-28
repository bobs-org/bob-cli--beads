# Bead: bob-cli-du — Complete labels — relation labels that complete their source task

[Bead Pages](../README.md) / bob-cli-du

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.aw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.aw.md) · **Assignee:** `bob-cli-du.land`
**Created:** 2026-10-28 14:49:53 EDT
**Plan:** [202610/relation\_complete\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_complete_labels.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/relation_complete_labels.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_complete_labels.md

<!-- sase:links:end -->

## Description

Committing a relation whose label is listed in `relations.complete_labels` (starting with `implemented by` and `verified by`) marks the relation's source task Done in the same gesture, exactly as that surface's managed Done gesture would. Every surface names the task before commit (✓ plus words, `↵ link & complete`). Bryan's 14 `implements` links are reversed into `implemented by` by a new, previewed, revertable `bob relations rename --reverse` transaction.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-du.1](bob-cli-du.1.md) | Complete-label contract (§18), reverse-rename contract, inverse pairs, and shared vectors | ✓ closed | medium | 2026-10-28 | 1 | 1 |
| [bob-cli-du.2](bob-cli-du.2.md) | relations.complete\_labels config and capture ~ / ~~ completes the source | ◐ in_progress | large | 2026-10-28 | 1 | 0 |
| [bob-cli-du.3](bob-cli-du.3.md) | Completion, parse, relations list, rename warnings, and zsh show complete labels | ◐ in_progress | medium | 2026-10-28 | 1 | 0 |
| [bob-cli-du.4](bob-cli-du.4.md) | bob relations rename --reverse moves each edge to its other end | ◐ in_progress | large | 2026-10-28 | 1 | 0 |
| [bob-cli-du.5](bob-cli-du.5.md) | task-status-cycler API v3 exposes its Done line rewrite and post-Done pass | ✓ closed | medium | 2026-10-28 | 1 | 1 |
| [bob-cli-du.6](bob-cli-du.6.md) | Obsidian relation writer folds the Done into the source write | ◐ in_progress | large | 2026-10-28 | 1 | 0 |
| [bob-cli-du.7](bob-cli-du.7.md) | Obsidian Links stage ✓ indication, mixed batch confirm, hints, and inverse chips | ◐ in_progress | medium | 2026-10-28 | 1 | 0 |
| [bob-cli-du.8](bob-cli-du.8.md) | Bob Mac Capture renders bob's complete consequences and offers | ◐ in_progress | medium | 2026-10-28 | 1 | 0 |
| [bob-cli-du.9](bob-cli-du.9.md) | Migrate implements, turn it on in chezmoi, record memory, and run acceptance | ◐ in_progress | medium | 2026-10-28 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-du: Complete labels — relation labels that complete their source task [in_progress]"]
    n1["bob-cli-du.1: Complete-label contract (§18), reverse-rename contract, inverse pairs, and shared vectors [closed]"]
    n2["bob-cli-du.2: relations.complete_labels config and capture ~ / ~~ completes the source [in_progress]"]
    n3["bob-cli-du.2.1: Complete relation sources through the shared capture Done path [in_progress]"]
    n4["bob-cli-du.2.1.1: Parse closing-label policy and expose complete verdicts [in_progress]"]
    n5["bob-cli-du.2.1.2: Extract reusable capture completion and aggregate nested outcomes [in_progress]"]
    n6["bob-cli-du.2.1.3: Complete relation sources in the staged capture transaction [in_progress]"]
    n7["bob-cli-du.2.1.4: Verify capture edge cases and update implemented contract markers [in_progress]"]
    n8["bob-cli-du.3: Completion, parse, relations list, rename warnings, and zsh show complete labels [in_progress]"]
    n9["bob-cli-du.4: bob relations rename --reverse moves each edge to its other end [in_progress]"]
    n10["bob-cli-du.5: task-status-cycler API v3 exposes its Done line rewrite and post-Done pass [closed]"]
    n11["bob-cli-du.6: Obsidian relation writer folds the Done into the source write [in_progress]"]
    n12["bob-cli-du.7: Obsidian Links stage ✓ indication, mixed batch confirm, hints, and inverse chips [in_progress]"]
    n13["bob-cli-du.8: Bob Mac Capture renders bob's complete consequences and offers [in_progress]"]
    n14["bob-cli-du.9: Migrate implements, turn it on in chezmoi, record memory, and run acceptance [in_progress]"]
    n0 --> n1
    n0 --> n2
    n2 --> n3
    n3 --> n4
    n3 --> n5
    n3 --> n6
    n3 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n0 --> n14
    n1 -.-> n2
    n1 -.-> n10
    n2 -.-> n8
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
    n8 -.-> n9
    n8 -.-> n13
    n9 -.-> n14
    n10 -.-> n11
    n11 -.-> n12
    n12 -.-> n14
    n13 -.-> n14
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.1/README.md) | [bob-cli-du.1](bob-cli-du.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-du.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.2.md) | [bob-cli-du.2](bob-cli-du.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.1/README.md) | [bob-cli-du.2.1.1](bob-cli-du.2.1.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.2/README.md) | [bob-cli-du.2.1.2](bob-cli-du.2.1.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.3/README.md) | [bob-cli-du.2.1.3](bob-cli-du.2.1.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.4/README.md) | [bob-cli-du.2.1.4](bob-cli-du.2.1.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.land/README.md) | [bob-cli-du.2.1](bob-cli-du.2.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.3/README.md) | [bob-cli-du.3](bob-cli-du.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.4/README.md) | [bob-cli-du.4](bob-cli-du.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.5/README.md) | [bob-cli-du.5](bob-cli-du.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-du.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.6/README.md) | [bob-cli-du.6](bob-cli-du.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.7/README.md) | [bob-cli-du.7](bob-cli-du.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.8/README.md) | [bob-cli-du.8](bob-cli-du.8.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.9/README.md) | [bob-cli-du.9](bob-cli-du.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-du.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.land/README.md) | [bob-cli-du](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`847a3c5`](https://github.com/bobs-org/bob-cli/commit/847a3c5341ea70f00b4ca6f85c0d405cee8836fe) | feat(relations): add complete-label contract, reverse-rename, and shared vectors | [bob-cli-du.1](bob-cli-du.1.md) | 2026-10-28 15:13:07 EDT |
| bob-plugins | [`bob-plugins@3c84ee3`](https://github.com/bobs-org/bob-plugins/commit/3c84ee3a2cb6cfcbc5dd2ba4a41e71a99dde21e7) | feat(task-status-cycler): expose Done line rewrite and post-Done pass as api v3 | [bob-cli-du.5](bob-cli-du.5.md) | 2026-10-28 15:39:19 EDT |
