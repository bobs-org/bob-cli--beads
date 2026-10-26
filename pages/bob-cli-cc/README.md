# Bead: bob-cli-cc — Exact code-block copy from Bob Refs, and Command-Y in Highlights

[Bead Pages](../README.md) / bob-cli-cc

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.land`
**Created:** 2026-10-26 09:00:55 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

While reading a bob-rendered reference in Highlights, Command-Y C Return puts the code block on the current page on the clipboard byte for byte (tabs, indentation, long lines, Mermaid source). The original Markdown of every new reference is preserved in the vault, one key (M) away, and `bob ref code` gives agents and the CLI the same data.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-cc.1](bob-cli-cc.1.md) | Keep bob's note walkers out of .bob | ✓ closed | small | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.10](bob-cli-cc.10.md) | Decision records | ◐ in_progress | xsmall | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.2](bob-cli-cc.2.md) | Render-time code catalog on both pandoc routes | ◐ in_progress | medium | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.3](bob-cli-cc.3.md) | Write-once source store and the source\_markdown pointer | ◐ in_progress | medium | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.4](bob-cli-cc.4.md) | bob ref code read surface | ◐ in_progress | medium | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.5](bob-cli-cc.5.md) | Overwrite repointing and the doctor sources check | ◐ in_progress | medium | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.6](bob-cli-cc.6.md) | Verified attach of existing references' sources | ◐ in_progress | medium | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.7](bob-cli-cc.7.md) | Command-Y takeover in Highlights and type-ahead | ✓ closed | medium | 2026-10-26 | 1 | 1 |
| [bob-cli-cc.8](bob-cli-cc.8.md) | RefsCore code catalog, C and M rows, and the code picker model | ◐ in_progress | medium | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.9](bob-cli-cc.9.md) | Code picker, preview well, and panel wiring | ◐ in_progress | medium | 2026-10-26 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-cc: Exact code-block copy from Bob Refs, and Command-Y in Highlights [in_progress]"]
    n1["bob-cli-cc.1: Keep bob's note walkers out of .bob [closed]"]
    n2["bob-cli-cc.10: Decision records [in_progress]"]
    n3["bob-cli-cc.2: Render-time code catalog on both pandoc routes [in_progress]"]
    n4["bob-cli-cc.3: Write-once source store and the source_markdown pointer [in_progress]"]
    n5["bob-cli-cc.4: bob ref code read surface [in_progress]"]
    n6["bob-cli-cc.5: Overwrite repointing and the doctor sources check [in_progress]"]
    n7["bob-cli-cc.6: Verified attach of existing references' sources [in_progress]"]
    n8["bob-cli-cc.7: Command-Y takeover in Highlights and type-ahead [closed]"]
    n9["bob-cli-cc.8: RefsCore code catalog, C and M rows, and the code picker model [in_progress]"]
    n10["bob-cli-cc.9: Code picker, preview well, and panel wiring [in_progress]"]
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
    n1 -.-> n4
    n3 -.-> n4
    n4 -.-> n5
    n4 -.-> n6
    n4 -.-> n7
    n5 -.-> n7
    n5 -.-> n9
    n6 -.-> n2
    n8 -.-> n9
    n9 -.-> n10
    n10 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.1/README.md) | [bob-cli-cc.1](bob-cli-cc.1.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.10/README.md) | [bob-cli-cc.10](bob-cli-cc.10.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-cc.2.md) | [bob-cli-cc.2](bob-cli-cc.2.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.3/README.md) | [bob-cli-cc.3](bob-cli-cc.3.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.4/README.md) | [bob-cli-cc.4](bob-cli-cc.4.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.5/README.md) | [bob-cli-cc.5](bob-cli-cc.5.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.6/README.md) | [bob-cli-cc.6](bob-cli-cc.6.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.7/README.md) | [bob-cli-cc.7](bob-cli-cc.7.md) | 1 |
| [bbugyi200.athena.bob-cli-cc.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.8/README.md) | [bob-cli-cc.8](bob-cli-cc.8.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.9/README.md) | [bob-cli-cc.9](bob-cli-cc.9.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.land/README.md) | [bob-cli-cc](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7b9bbdd`](https://github.com/bobs-org/bob-mac-capture/commit/7b9bbddabfd2b3368bb77287842e045f677cabb7) | feat(refs): Command-Y takeover opens the Copy card from Highlights | [bob-cli-cc.7](bob-cli-cc.7.md) | 2026-10-26 09:53:32 EDT |
