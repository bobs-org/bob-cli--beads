# Bead: bob-cli-q4 — Better o / Ctrl+Shift+O and gesture-settled task structure

[Bead Pages](../README.md) / bob-cli-q4

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.land`
**Created:** 2026-11-25 08:51:35 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/better_o_gesture_settle.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md

<!-- sase:links:end -->

## Description

Vim `o`, `O`, and `Ctrl+Shift+O` in Obsidian write into the right zone of a task block and never split a task from its children. Every bob-cli writer and every Obsidian gesture that changes a task's status or note settles that note's local structure in the same write. That means the local future-schedule Blocked rule, the `## Tasks` status groups, and the badge row. `bob task reconcile` then only does clock-driven and vault-wide work, and the drift numbers prove it.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-q4.1](bob-cli-q4.1.md) | Hand-edit mirror never writes across notes | ✓ closed | medium | 2026-11-25 | 1 | 1 |
| [bob-cli-q4.10](bob-cli-q4.10.md) | Navigation gestures settle both notes they write | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q4.11](bob-cli-q4.11.md) | Link and Pomodoro target writes settle their target notes | ◐ in_progress | medium | 2026-11-25 | 1 | 0 |
| [bob-cli-q4.12](bob-cli-q4.12.md) | Ctrl+Shift+O opens a note where note\_home says | ◐ in_progress | medium | 2026-11-25 | 1 | 0 |
| [bob-cli-q4.13](bob-cli-q4.13.md) | End-to-end settle acceptance and re-measure | ◐ in_progress | medium | 2026-11-25 | 1 | 0 |
| [bob-cli-q4.2](bob-cli-q4.2.md) | o and O open real siblings after the whole subtree | ✓ closed | medium | 2026-11-25 | 1 | 1 |
| [bob-cli-q4.3](bob-cli-q4.3.md) | One pure Rust settle\_note that reconcile composes | ✓ closed | medium | 2026-11-25 | 1 | 1 |
| [bob-cli-q4.4](bob-cli-q4.4.md) | Reconcile drift meter and recorded baseline | ◐ in_progress | medium | 2026-11-25 | 1 | 0 |
| [bob-cli-q4.5](bob-cli-q4.5.md) | Plain split and BLOCKS placement match the layout contract | ✓ closed | medium | 2026-11-25 | 1 | 2 |
| [bob-cli-q4.6](bob-cli-q4.6.md) | Capture settles every note it touches | ✓ closed | medium | 2026-11-25 | 1 | 1 |
| [bob-cli-q4.7](bob-cli-q4.7.md) | Task commands and sync writers settle their notes | ◐ in_progress | medium | 2026-11-25 | 1 | 0 |
| [bob-cli-q4.8](bob-cli-q4.8.md) | Vector-pinned JS settle twin behind a ledger-tools API | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q4.9](bob-cli-q4.9.md) | Cycler gestures settle, including recurring spawns and cycling | ◐ in_progress | large | 2026-11-25 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-q4: Better o / Ctrl+Shift+O and gesture-settled task structure [in_progress]"]
    n1["bob-cli-q4.1: Hand-edit mirror never writes across notes [closed]"]
    n2["bob-cli-q4.10: Navigation gestures settle both notes they write [in_progress]"]
    n3["bob-cli-q4.11: Link and Pomodoro target writes settle their target notes [in_progress]"]
    n4["bob-cli-q4.12: Ctrl+Shift+O opens a note where note_home says [in_progress]"]
    n5["bob-cli-q4.13: End-to-end settle acceptance and re-measure [in_progress]"]
    n6["bob-cli-q4.2: o and O open real siblings after the whole subtree [closed]"]
    n7["bob-cli-q4.3: One pure Rust settle_note that reconcile composes [closed]"]
    n8["bob-cli-q4.4: Reconcile drift meter and recorded baseline [in_progress]"]
    n9["bob-cli-q4.5: Plain split and BLOCKS placement match the layout contract [closed]"]
    n10["bob-cli-q4.6: Capture settles every note it touches [closed]"]
    n11["bob-cli-q4.7: Task commands and sync writers settle their notes [in_progress]"]
    n12["bob-cli-q4.8: Vector-pinned JS settle twin behind a ledger-tools API [in_progress]"]
    n13["bob-cli-q4.8.1: Vector-pinned taskSettle provider for ledger-tools [in_progress]"]
    n14["bob-cli-q4.8.1.1: Port the pure settle transform and pin Rust parity [closed]"]
    n15["bob-cli-q4.8.1.2: Add the guarded editor adapter and cursor policy [in_progress]"]
    n16["bob-cli-q4.8.1.3: Publish taskSettle v1 with the pending scheduler [in_progress]"]
    n17["bob-cli-q4.9: Cycler gestures settle, including recurring spawns and cycling [in_progress]"]
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
    n0 --> n12
    n12 --> n13
    n13 --> n14
    n13 --> n15
    n13 --> n16
    n0 --> n17
    n1 -.-> n5
    n1 -.-> n9
    n2 -.-> n5
    n3 -.-> n5
    n4 -.-> n5
    n6 -.-> n4
    n6 -.-> n5
    n6 -.-> n17
    n7 -.-> n5
    n7 -.-> n10
    n7 -.-> n11
    n7 -.-> n12
    n8 -.-> n5
    n9 -.-> n2
    n9 -.-> n5
    n9 -.-> n11
    n10 -.-> n5
    n11 -.-> n5
    n12 -.-> n2
    n12 -.-> n3
    n12 -.-> n5
    n12 -.-> n17
    n14 -.-> n15
    n15 -.-> n16
    n17 -.-> n4
    n17 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.1/README.md) | [bob-cli-q4.1](bob-cli-q4.1.md) | 1 |
| [bbugyi200.athena.bob-cli-q4.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.10/README.md) | [bob-cli-q4.10](bob-cli-q4.10.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.11/README.md) | [bob-cli-q4.11](bob-cli-q4.11.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.12/README.md) | [bob-cli-q4.12](bob-cli-q4.12.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.13/README.md) | [bob-cli-q4.13](bob-cli-q4.13.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.2/README.md) | [bob-cli-q4.2](bob-cli-q4.2.md) | 1 |
| [bbugyi200.athena.bob-cli-q4.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.3.md) | [bob-cli-q4.3](bob-cli-q4.3.md) | 1 |
| [bbugyi200.athena.bob-cli-q4.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.4/README.md) | [bob-cli-q4.4](bob-cli-q4.4.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.5.md) | [bob-cli-q4.5](bob-cli-q4.5.md) | 2 |
| [bbugyi200.athena.bob-cli-q4.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.6.md) | [bob-cli-q4.6](bob-cli-q4.6.md) | 1 |
| [bbugyi200.athena.bob-cli-q4.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.7/README.md) | [bob-cli-q4.7](bob-cli-q4.7.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.md) | [bob-cli-q4.8](bob-cli-q4.8.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.1/README.md) | [bob-cli-q4.8.1.1](bob-cli-q4.8.1.1.md) | 2 |
| [bbugyi200.athena.bob-cli-q4.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.2/README.md) | [bob-cli-q4.8.1.2](bob-cli-q4.8.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.3/README.md) | [bob-cli-q4.8.1.3](bob-cli-q4.8.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.land/README.md) | [bob-cli-q4.8.1](bob-cli-q4.8.1.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.9/README.md) | [bob-cli-q4.9](bob-cli-q4.9.md) | 0 |
| [bbugyi200.athena.bob-cli-q4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.land/README.md) | [bob-cli-q4](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9a98738`](https://github.com/bobs-org/bob-plugins/commit/9a987385709c0d4ada689c94b9c0e66798e81c2f) | fix(nav): drop debounced hand-edit mirror pass when the editor switched notes | [bob-cli-q4.1](bob-cli-q4.1.md) | 2026-11-25 09:07:04 EST |
| bob-plugins | [`bob-plugins@a971285`](https://github.com/bobs-org/bob-plugins/commit/a971285b2fe70720dd0a3429512879737810120e) | feat(task-status-cycler): open real siblings with o and O | [bob-cli-q4.2](bob-cli-q4.2.md) | 2026-11-25 09:17:28 EST |
| bob-cli | [`9395683`](https://github.com/bobs-org/bob-cli/commit/9395683818ef4a11527fda82c5290e20ef6aebe6) | feat(task): add pure note settle helper | [bob-cli-q4.3](bob-cli-q4.3.md) | 2026-11-25 10:18:20 EST |
| bob-cli | [`814b658`](https://github.com/bobs-org/bob-cli/commit/814b6583e63165a4f2419158af50d4774fc8b034) | fix(task-split): route plain-split back-link through managed-link zone | [bob-cli-q4.5](bob-cli-q4.5.md) | 2026-11-25 10:19:06 EST |
| bob-plugins | [`bob-plugins@eac9d74`](https://github.com/bobs-org/bob-plugins/commit/eac9d7448d056e60af1e0f4224554c6ca1ed28d2) | fix(nav-split): mirror managed back-link and BLOCKS-after-Depends-On order | [bob-cli-q4.5](bob-cli-q4.5.md) | 2026-11-25 10:19:46 EST |
| bob-cli | [`007ef5e`](https://github.com/bobs-org/bob-cli/commit/007ef5ed819595338ad7f629e660c43fcf2b496f) | feat(capture): settle touched notes before reporting lines | [bob-cli-q4.6](bob-cli-q4.6.md) | 2026-11-25 10:40:41 EST |
| bob-cli | [`5c0f816`](https://github.com/bobs-org/bob-cli/commit/5c0f81608f94cd41ceddb726736a79ea944030bd) | feat(task-settle): add canonical task-settle fixture README | [bob-cli-q4.8.1.1](bob-cli-q4.8.1.1.md) | 2026-11-25 11:10:42 EST |
| bob-plugins | [`bob-plugins@824d8e4`](https://github.com/bobs-org/bob-plugins/commit/824d8e4951ef11c492cf515b4200390b4c0a35fd) | feat(ledger-tools): port task-settle to pure-twin fragments 139a-d | [bob-cli-q4.8.1.1](bob-cli-q4.8.1.1.md) | 2026-11-25 11:11:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.2][1] | Need parent epic DECISIONS, phases, and overall design | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.2/README.md

<!-- sase:referenced-by:end -->
