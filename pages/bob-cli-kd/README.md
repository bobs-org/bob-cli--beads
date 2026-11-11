# Bead: bob-cli-kd — Bank — acknowledge every transaction daily, prove it weekly

[Bead Pages](../README.md) / bob-cli-kd

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1be.md) · **Assignee:** `bob-cli-kd.land`
**Created:** 2026-11-11 11:24:16 EST
**Plan:** [202611/bank\_daily\_acknowledgment.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_daily_acknowledgment.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md

<!-- sase:links:end -->

## Description

Bryan restarts his daily bank habit right away. Every posted transaction and deposit becomes one checkbox row in a monthly bank note under a new `bank` sub-area of `cash`. Typing a row acknowledges it. A weekly `bob bank import` of a Wells Fargo QFX file writes, unchecked, only the rows he missed, and a balance proof shows that nothing was skipped. Every total is computed when it is drawn (terminal, month card, queue card, daily chip) and never written into notes. A missed week costs one sitting to catch up, not a retyping spiral.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-kd.1](bob-cli-kd.1.md) | Restart the habit in the vault with no code | ✓ closed | small | 2026-11-11 | 1 | 0 |
| [bob-cli-kd.2](bob-cli-kd.2.md) | The bank module, row grammar, and bob bank check | ✓ closed | medium | 2026-11-11 | 1 | 1 |
| [bob-cli-kd.3](bob-cli-kd.3.md) | Read the bank — list, report, ensure, and ack | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |
| [bob-cli-kd.4](bob-cli-kd.4.md) | Weekly QFX import that writes only what you missed | ◐ in_progress | large | 2026-11-11 | 1 | 0 |
| [bob-cli-kd.5](bob-cli-kd.5.md) | Prove every transaction — coverage, presence, balance | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |
| [bob-cli-kd.6](bob-cli-kd.6.md) | Obsidian bank cards, styled rows, and the daily chip | ◐ in_progress | large | 2026-11-11 | 1 | 0 |
| [bob-cli-kd.7](bob-cli-kd.7.md) | End-to-end proof, the guide, docs audit, memory, and follow-ups | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-kd: Bank — acknowledge every transaction daily, prove it weekly [in_progress]"]
    n1["bob-cli-kd.1: Restart the habit in the vault with no code [closed]"]
    n2["bob-cli-kd.2: The bank module, row grammar, and bob bank check [closed]"]
    n3["bob-cli-kd.3: Read the bank — list, report, ensure, and ack [in_progress]"]
    n4["bob-cli-kd.4: Weekly QFX import that writes only what you missed [in_progress]"]
    n5["bob-cli-kd.5: Prove every transaction — coverage, presence, balance [in_progress]"]
    n6["bob-cli-kd.6: Obsidian bank cards, styled rows, and the daily chip [in_progress]"]
    n7["bob-cli-kd.7: End-to-end proof, the guide, docs audit, memory, and follow-ups [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n7
    n2 -.-> n3
    n3 -.-> n4
    n3 -.-> n6
    n4 -.-> n5
    n5 -.-> n7
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.1/README.md) | [bob-cli-kd.1](bob-cli-kd.1.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.2.md) | [bob-cli-kd.2](bob-cli-kd.2.md) | 1 |
| [bbugyi200.athena.bob-cli-kd.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.3/README.md) | [bob-cli-kd.3](bob-cli-kd.3.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4/README.md) | [bob-cli-kd.4](bob-cli-kd.4.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.5/README.md) | [bob-cli-kd.5](bob-cli-kd.5.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6/README.md) | [bob-cli-kd.6](bob-cli-kd.6.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.7/README.md) | [bob-cli-kd.7](bob-cli-kd.7.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.land/README.md) | [bob-cli-kd](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`07f1c74`](https://github.com/bobs-org/bob-cli/commit/07f1c7442bb24d50658167856fb5816312199423) | feat(bank): add bank grammar, month notes, and read-only bob bank check | [bob-cli-kd.2](bob-cli-kd.2.md) | 2026-11-11 12:58:45 EST |
