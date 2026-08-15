# Bead: bob-cli-t — Multi-item capture for Bob Mac Capture

[Bead Pages](../README.md) / bob-cli-t

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.024.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.024.w1.md) · **Assignee:** `bob-cli-t.land`
**Created:** 2026-08-15 09:47:49 EDT
**Plan:** [202608/multi\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/multi_capture.md)

## Description

One Bob Mac Capture draft atomically captures every blank-line-separated task or note, with intuitive native editing, complete preview and notification feedback, and backward-compatible Bob protocols.

## Notes

[2026-08-15T15:29:17Z · bob-cli-t.land] DISCOVERED ISSUE: Concurrent epic bob-cli-u landed bob-cli commit 2037307 and bob-mac-capture commit dff08a7 after bob-cli-t began. The implementations preserve Bob current item-aware completion and the mac model stores draft-global replacement ranges, but neither repository has focused coverage for --all-tasks missing-ID completion in a later batch item or for the Add block ID prompt replacing only that later item while preserving the earlier draft and rerunning one-process aggregate preview. Add this cross-feature regression coverage and fix any behavior it exposes before landing bob-cli-t.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-t.1](bob-cli-t.1.md) | Add Bob's batch grammar, protocol, and atomic transaction | ✓ closed | medium | 2026-08-15 | 1 | 1 |
| [bob-cli-t.2](bob-cli-t.2.md) | Integrate batch results and native editor behavior in the mac app | ✓ closed | medium | 2026-08-15 | 1 | 1 |
| [bob-cli-t.3](bob-cli-t.3.md) | Deliver complete, polished single and batch notifications | ✓ closed | small | 2026-08-15 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-t: Multi-item capture for Bob Mac Capture [in_progress]"]
    n1["bob-cli-t.1: Add Bob's batch grammar, protocol, and atomic transaction [closed]"]
    n2["bob-cli-t.2: Integrate batch results and native editor behavior in the mac app [closed]"]
    n3["bob-cli-t.3: Deliver complete, polished single and batch notifications [closed]"]
    n4["bob-cli-t.4: Finish and land multi-item capture [in_progress]"]
    n5["bob-cli-t.4.1: Restore the macOS test and release pipeline [closed]"]
    n6["bob-cli-t.4.2: Integrate later-item task-ID assignment with batch capture [closed]"]
    n7["bob-cli-t.4.3: Validate the integrated CLI and installed macOS experience [in_progress]"]
    n8["bob-cli-t.4.4: Close bob-cli-t and clean its expired symbol allowances [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n4 --> n5
    n4 --> n6
    n4 --> n7
    n4 --> n8
    n1 -.-> n2
    n2 -.-> n3
    n5 -.-> n7
    n6 -.-> n7
    n7 -.-> n8
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-t.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.1/README.md) | [bob-cli-t.1](bob-cli-t.1.md) | 1 |
| [bbugyi200.athena.bob-cli-t.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.2/README.md) | [bob-cli-t.2](bob-cli-t.2.md) | 1 |
| [bbugyi200.athena.bob-cli-t.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.3/README.md) | [bob-cli-t.3](bob-cli-t.3.md) | 1 |
| [bbugyi200.athena.bob-cli-t.4.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.4.1/README.md) | [bob-cli-t.4.1](bob-cli-t.4.1.md) | 1 |
| [bbugyi200.athena.bob-cli-t.4.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.4.2/README.md) | [bob-cli-t.4.2](bob-cli-t.4.2.md) | 2 |
| [bbugyi200.athena.bob-cli-t.4.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.4.3/README.md) | [bob-cli-t.4.3](bob-cli-t.4.3.md) | 1 |
| [bbugyi200.athena.bob-cli-t.4.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.4.4/README.md) | [bob-cli-t.4.4](bob-cli-t.4.4.md) | 0 |
| [bbugyi200.athena.bob-cli-t.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.4.land/README.md) | [bob-cli-t.4](bob-cli-t.4.md) | 0 |
| [bbugyi200.athena.bob-cli-t.land](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.bob-cli-t.land.md) | [bob-cli-t](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a8c9ad8`](https://github.com/bobs-org/bob-cli/commit/a8c9ad8e8909008a64a1929e97fb831ce7339a69) | feat(capture)!: add atomic batch capture support | [bob-cli-t.1](bob-cli-t.1.md) | 2026-08-15 10:17:05 EDT |
| bob-mac-capture | [`bob-mac-capture@4c22525`](https://github.com/bobs-org/bob-mac-capture/commit/4c2252578bc1c18b629ce369de8d71c2f32d0a5e) | feat: integrate batch capture results in mac app | [bob-cli-t.2](bob-cli-t.2.md) | 2026-08-15 10:44:23 EDT |
| bob-mac-capture | [`bob-mac-capture@c95ba0e`](https://github.com/bobs-org/bob-mac-capture/commit/c95ba0e34b4a63b8c5223f02a2d9983b8253c0ae) | feat: polish batch capture notifications | [bob-cli-t.3](bob-cli-t.3.md) | 2026-08-15 11:18:13 EDT |
| bob-mac-capture | [`bob-mac-capture@fc1c16b`](https://github.com/bobs-org/bob-mac-capture/commit/fc1c16b1aa8ab0f47069eb6c8c5fe0e8398c15a4) | fix: expose pure indentation resolver off main actor | [bob-cli-t.4.1](bob-cli-t.4.1.md) | 2026-08-15 11:37:29 EDT |
| bob-cli | [`3beae5b`](https://github.com/bobs-org/bob-cli/commit/3beae5bf7ee67486d0c721e8beaf92f57847e5d8) | test: cover all-task completion ranges in later batch items | [bob-cli-t.4.2](bob-cli-t.4.2.md) | 2026-08-15 11:47:01 EDT |
| bob-mac-capture | [`bob-mac-capture@49f0037`](https://github.com/bobs-org/bob-mac-capture/commit/49f0037c25038ec44641aab4d6de4229322fab83) | test: cover later batch task ID assignment | [bob-cli-t.4.2](bob-cli-t.4.2.md) | 2026-08-15 11:47:46 EDT |
| bob-mac-capture | [`bob-mac-capture@181a644`](https://github.com/bobs-org/bob-mac-capture/commit/181a64459e96d0be332a58422ff724fa2710ad78) | test: stabilize later batch task completion fixture | [bob-cli-t.4.3](bob-cli-t.4.3.md) | 2026-08-15 11:55:29 EDT |
