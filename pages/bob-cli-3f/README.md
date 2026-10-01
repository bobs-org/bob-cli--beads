# Bead: bob-cli-3f — Per-note Ready cap: crowded notes in the CLI, dash, and notes

[Bead Pages](../README.md) / bob-cli-3f

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0v5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0v5.md) · **Assignee:** `bob-cli-3f.land`
**Created:** 2026-10-01 17:55:47 EDT
**Plan:** [202610/per\_note\_ready\_cap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/per_note_ready_cap.md)

## Description

Every area/project note has a soft cap on its Ready lane (plan.max_ready_per_note, default 5, per-note ready_cap override). Crowded notes are named, counted, and easy to act on: in a new `bob ready` CLI view, a dash CROWDED chip that opens crowded.md, and a live chip on each note's `## Tasks` heading. All surfaces share one read-time contract, implemented in Rust and in bob-ledger-tools and pinned by shared vectors. The keymap-notice work is fully specified and filed to start after the freshness trial.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-3f.1](bob-cli-3f.1.md) | Ready-lane-per-note contract, config, and Rust evaluator | ✓ closed | medium | 2026-10-01 | 1 | 1 |
| [bob-cli-3f.2](bob-cli-3f.2.md) | bob ready command | ✓ closed | medium | 2026-10-01 | 1 | 1 |
| [bob-cli-3f.3](bob-cli-3f.3.md) | bob-ledger-tools noteReady API | ✓ closed | medium | 2026-10-01 | 1 | 1 |
| [bob-cli-3f.4](bob-cli-3f.4.md) | CROWDED chip, bob-ready-notes block, and Tasks heading chip | ✓ closed | medium | 2026-10-01 | 1 | 1 |
| [bob-cli-3f.5](bob-cli-3f.5.md) | Vault rollout, docs, and live verification | ◐ in_progress | medium | 2026-10-01 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-3f: Per-note Ready cap: crowded notes in the CLI, dash, and notes [in_progress]"]
    n1["bob-cli-3f.1: Ready-lane-per-note contract, config, and Rust evaluator [closed]"]
    n2["bob-cli-3f.2: bob ready command [closed]"]
    n3["bob-cli-3f.3: bob-ledger-tools noteReady API [closed]"]
    n4["bob-cli-3f.4: CROWDED chip, bob-ready-notes block, and Tasks heading chip [closed]"]
    n5["bob-cli-3f.5: Vault rollout, docs, and live verification [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n1 -.-> n3
    n2 -.-> n5
    n3 -.-> n4
    n4 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3f.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.1/README.md) | [bob-cli-3f.1](bob-cli-3f.1.md) | 1 |
| [bbugyi200.athena.bob-cli-3f.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.2/README.md) | [bob-cli-3f.2](bob-cli-3f.2.md) | 1 |
| [bbugyi200.athena.bob-cli-3f.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.3/README.md) | [bob-cli-3f.3](bob-cli-3f.3.md) | 1 |
| [bbugyi200.athena.bob-cli-3f.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.4/README.md) | [bob-cli-3f.4](bob-cli-3f.4.md) | 1 |
| [bbugyi200.athena.bob-cli-3f.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.5/README.md) | [bob-cli-3f.5](bob-cli-3f.5.md) | 0 |
| [bbugyi200.athena.bob-cli-3f.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.land/README.md) | [bob-cli-3f](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6e04265`](https://github.com/bobs-org/bob-cli/commit/6e0426524aeed583632995fdc01ceae33f840c17) | feat(note-ready): per-note Ready cap contract, config, and Rust evaluator | [bob-cli-3f.1](bob-cli-3f.1.md) | 2026-10-01 18:17:15 EDT |
| bob-plugins | [`bob-plugins@03fbd18`](https://github.com/bobs-org/bob-plugins/commit/03fbd18367f00fa6b2bdf997131588e0bd866d04) | feat(ledger-tools): per-note Ready cap api.noteReady v1 (1.15.0) | [bob-cli-3f.3](bob-cli-3f.3.md) | 2026-10-01 18:47:49 EDT |
| bob-cli | [`812c1b1`](https://github.com/bobs-org/bob-cli/commit/812c1b19ac8402dd92c6fd451405e6a853341c97) | feat(ready): add bob ready per-note Ready-cap view | [bob-cli-3f.2](bob-cli-3f.2.md) | 2026-10-01 18:48:02 EDT |
| bob-plugins | [`bob-plugins@91b8e40`](https://github.com/bobs-org/bob-plugins/commit/91b8e405adb9bb1a2b76475d90e80748c17963c2) | feat(ledger-tools): CROWDED chip, bob-ready-notes block, and Tasks heading chip (1.16.0) | [bob-cli-3f.4](bob-cli-3f.4.md) | 2026-10-01 19:19:48 EDT |
