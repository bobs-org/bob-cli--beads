# Bead: bob-cli-ms — Record Card: an editable value sheet under the H1 of every record note

[Bead Pages](../README.md) / bob-cli-ms

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.55.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.55.linker.w0.md) · **Assignee:** `bob-cli-ms.land`
**Created:** 2026-11-17 11:29:54 EST
**Plan:** [202611/record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/record_card.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card.md

<!-- sase:links:end -->

## Description

Every healthy record note shows its album-defined fields as a quiet, beautiful record sheet under the H1 and above ## Notes, in bob's vocabulary. Every value is editable from a keyboard-first Record Card (== , Ctrl+Shift+P, palette, Command Mode, or a click) through one guarded bob writer, with Undo. Native Properties hide only when the sheet shows every key and bob can write.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ms.1](bob-cli-ms.1.md) | Per-record read and record fingerprint in bob records show | ◐ in_progress | medium | 2026-11-17 | 1 | 1 |
| [bob-cli-ms.2](bob-cli-ms.2.md) | Guarded JSON envelope for bob records update | ◐ in_progress | medium | 2026-11-17 | 1 | 0 |
| [bob-cli-ms.3](bob-cli-ms.3.md) | Read-only record sheet under the H1 (Live Preview and Reading) | ◐ in_progress | large | 2026-11-17 | 1 | 0 |
| [bob-cli-ms.4](bob-cli-ms.4.md) | Record update service and guarded session with direct apply | ◐ in_progress | medium | 2026-11-17 | 1 | 0 |
| [bob-cli-ms.5](bob-cli-ms.5.md) | Record Card shell, browse keys, choices, and discrete actions | ◐ in_progress | large | 2026-11-17 | 1 | 0 |
| [bob-cli-ms.6](bob-cli-ms.6.md) | Typed Record Card stages and Tab fill-out | ◐ in_progress | large | 2026-11-17 | 1 | 0 |
| [bob-cli-ms.7](bob-cli-ms.7.md) | Entry points, == on records, and the Properties hide | ◐ in_progress | medium | 2026-11-17 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ms: Record Card: an editable value sheet under the H1 of every record note [in_progress]"]
    n1["bob-cli-ms.1: Per-record read and record fingerprint in bob records show [in_progress]"]
    n2["bob-cli-ms.2: Guarded JSON envelope for bob records update [in_progress]"]
    n3["bob-cli-ms.3: Read-only record sheet under the H1 (Live Preview and Reading) [in_progress]"]
    n4["bob-cli-ms.4: Record update service and guarded session with direct apply [in_progress]"]
    n5["bob-cli-ms.5: Record Card shell, browse keys, choices, and discrete actions [in_progress]"]
    n6["bob-cli-ms.6: Typed Record Card stages and Tab fill-out [in_progress]"]
    n7["bob-cli-ms.7: Entry points, == on records, and the Properties hide [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n2
    n2 -.-> n4
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.1.md) | [bob-cli-ms.1](bob-cli-ms.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ms.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.2/README.md) | [bob-cli-ms.2](bob-cli-ms.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-ms.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.3.md) | [bob-cli-ms.3](bob-cli-ms.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-ms.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.4/README.md) | [bob-cli-ms.4](bob-cli-ms.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-ms.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.5/README.md) | [bob-cli-ms.5](bob-cli-ms.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-ms.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.6/README.md) | [bob-cli-ms.6](bob-cli-ms.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-ms.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.7/README.md) | [bob-cli-ms.7](bob-cli-ms.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-ms.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.land/README.md) | [bob-cli-ms](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9900597`](https://github.com/bobs-org/bob-cli/commit/99005975e15aaa3c2440b36e8f87dc4481908500) | feat(records): add per-record show STEM and fingerprint | [bob-cli-ms.1](bob-cli-ms.1.md) | 2026-11-17 13:38:16 EST |
