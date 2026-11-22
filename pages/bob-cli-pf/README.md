# Bead: bob-cli-pf — Property cards own the frontmatter — foot row, =- drawer, created stamp, =+ editor, takeover

[Bead Pages](../README.md) / bob-cli-pf

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5v.linker.w0.md) · **Assignee:** `bob-cli-pf.land`
**Created:** 2026-11-22 14:35:12 EST
**Plan:** [202611/card\_owned\_frontmatter.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_owned_frontmatter.md)

## Description

On every note a property card mounts on, the card shows the whole frontmatter: a quiet foot row with a concise created stamp and a collapsed read-only Properties drawer toggled by =-. A keyboard-first =+ property editor, backed by a byte-preserving `bob props` writer, does at least everything Obsidian's native Properties can on any Markdown note. Obsidian's native Properties block is hidden on card notes, and every failure path brings it back.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-pf.1](bob-cli-pf.1.md) | Card foot row, drawer, created stamp, and =- (bob-plugins) | ◐ in_progress | large | 2026-11-22 | 1 | 0 |
| [bob-cli-pf.2](bob-cli-pf.2.md) | Generic bob props show\|update (bob-cli) | ◐ in_progress | large | 2026-11-22 | 1 | 0 |
| [bob-cli-pf.3](bob-cli-pf.3.md) | Whole-container ownership primitive and focus spike (bob-plugins) | ✓ closed | medium | 2026-11-22 | 1 | 1 |
| [bob-cli-pf.4](bob-cli-pf.4.md) | The =+ property editor (bob-plugins) | ◐ in_progress | large | 2026-11-22 | 1 | 0 |
| [bob-cli-pf.5](bob-cli-pf.5.md) | Rename, reorder, multi-select, copy/paste, filter, kind change, YAML stage (bob-plugins) | ◐ in_progress | large | 2026-11-22 | 1 | 0 |
| [bob-cli-pf.6](bob-cli-pf.6.md) | Hide native Properties on card notes (bob-plugins, plus memory if approved) | ◐ in_progress | large | 2026-11-22 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-pf: Property cards own the frontmatter — foot row, =- drawer, created stamp, =+ editor, takeover [in_progress]"]
    n1["bob-cli-pf.1: Card foot row, drawer, created stamp, and =- (bob-plugins) [in_progress]"]
    n2["bob-cli-pf.1.1: Card foot row, properties drawer, and equals-minus entry points [in_progress]"]
    n3["bob-cli-pf.1.1.1: Shared created stamp and source-ordered property inventory [in_progress]"]
    n4["bob-cli-pf.1.1.2: Shared foot runtime and Record Card migration [in_progress]"]
    n5["bob-cli-pf.1.1.3: Album, temporal, and bank foot adoption [in_progress]"]
    n6["bob-cli-pf.1.1.4: Equals arm table and drawer commands [in_progress]"]
    n7["bob-cli-pf.1.1.5: Real-Obsidian drawer acceptance and deployment [in_progress]"]
    n8["bob-cli-pf.2: Generic bob props show|update (bob-cli) [in_progress]"]
    n9["bob-cli-pf.2.1: Generic bob props show and update [in_progress]"]
    n10["bob-cli-pf.2.1.1: Ordered frontmatter inventory and authoritative property roles [in_progress]"]
    n11["bob-cli-pf.2.1.2: Strict property operations and byte-exact undo [in_progress]"]
    n12["bob-cli-pf.2.1.3: Guarded props commands, capability, completion, and contract [in_progress]"]
    n13["bob-cli-pf.3: Whole-container ownership primitive and focus spike (bob-plugins) [closed]"]
    n14["bob-cli-pf.4: The =+ property editor (bob-plugins) [in_progress]"]
    n15["bob-cli-pf.5: Rename, reorder, multi-select, copy/paste, filter, kind change, YAML stage (bob-plugins) [in_progress]"]
    n16["bob-cli-pf.6: Hide native Properties on card notes (bob-plugins, plus memory if approved) [in_progress]"]
    n0 --> n1
    n1 --> n2
    n2 --> n3
    n2 --> n4
    n2 --> n5
    n2 --> n6
    n2 --> n7
    n0 --> n8
    n8 --> n9
    n9 --> n10
    n9 --> n11
    n9 --> n12
    n0 --> n13
    n0 --> n14
    n0 --> n15
    n0 --> n16
    n1 -.-> n14
    n1 -.-> n16
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
    n8 -.-> n14
    n10 -.-> n11
    n11 -.-> n12
    n13 -.-> n16
    n14 -.-> n15
    n15 -.-> n16
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.md) | [bob-cli-pf.1](bob-cli-pf.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.1/README.md) | [bob-cli-pf.1.1.1](bob-cli-pf.1.1.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.1.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.2/README.md) | [bob-cli-pf.1.1.2](bob-cli-pf.1.1.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.3/README.md) | [bob-cli-pf.1.1.3](bob-cli-pf.1.1.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.1.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.4/README.md) | [bob-cli-pf.1.1.4](bob-cli-pf.1.1.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.1.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.5/README.md) | [bob-cli-pf.1.1.5](bob-cli-pf.1.1.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.land/README.md) | [bob-cli-pf.1.1](bob-cli-pf.1.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.md) | [bob-cli-pf.2](bob-cli-pf.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.2.1.1/README.md) | [bob-cli-pf.2.1.1](bob-cli-pf.2.1.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.2.1.2/README.md) | [bob-cli-pf.2.1.2](bob-cli-pf.2.1.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.2.1.3/README.md) | [bob-cli-pf.2.1.3](bob-cli-pf.2.1.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.2.1.land/README.md) | [bob-cli-pf.2.1](bob-cli-pf.2.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.3/README.md) | [bob-cli-pf.3](bob-cli-pf.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-pf.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.4/README.md) | [bob-cli-pf.4](bob-cli-pf.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5/README.md) | [bob-cli-pf.5](bob-cli-pf.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6/README.md) | [bob-cli-pf.6](bob-cli-pf.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-pf.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.land/README.md) | [bob-cli-pf](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@394633f`](https://github.com/bobs-org/bob-plugins/commit/394633fb3113fbd2971feff54442ae05e912a23d) | feat(ledger-tools): add unwired frontmatter ownership kit | [bob-cli-pf.3](bob-cli-pf.3.md) | 2026-11-22 15:04:14 EST |
