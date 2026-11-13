# Bead: bob-cli-kx — Gmail archive on task close

[Bead Pages](../README.md) / bob-cli-kx

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bt](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bt.md) · **Assignee:** `bob-cli-kx.land`
**Created:** 2026-11-12 11:11:53 EST
**Plan:** [202611/gmail\_archive\_on\_task\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_on_task_close.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_archive_on_task_close.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_on_task_close.md

<!-- sase:links:end -->

## Description

bob gmail sync archives a bob-labelled thread's saved messages exactly once when every linking Obsidian task is closed, visibly, undoably, and opt-in; Bryan is opted in and a gated live run on the Mac writer verifies the expected threads were archived.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-kx.1](bob-cli-kx.1.md) | Mutation-path spike | ✓ closed | small | 2026-11-12 | 1 | 0 |
| [bob-cli-kx.2](bob-cli-kx.2.md) | Archive-on-close machinery in bob-cli | ◐ in_progress | large | 2026-11-12 | 1 | 0 |
| [bob-cli-kx.3](bob-cli-kx.3.md) | Undo command and receipt surfaces | ◐ in_progress | large | 2026-11-12 | 1 | 0 |
| [bob-cli-kx.4](bob-cli-kx.4.md) | Close-time notice polish | ◐ in_progress | small | 2026-11-12 | 1 | 0 |
| [bob-cli-kx.5](bob-cli-kx.5.md) | Gated live enable and verification | ◐ in_progress | medium | 2026-11-12 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-kx: Gmail archive on task close [in_progress]"]
    n1["bob-cli-kx.1: Mutation-path spike [closed]"]
    n2["bob-cli-kx.2: Archive-on-close machinery in bob-cli [in_progress]"]
    n3["bob-cli-kx.2.1: Gmail archive-on-close core [in_progress]"]
    n4["bob-cli-kx.2.1.1: Archive configuration and modify grant [closed]"]
    n5["bob-cli-kx.2.1.2: Positive closed-task and saved-message evidence [closed]"]
    n6["bob-cli-kx.2.1.3: One-shot archive journal and enable baseline [closed]"]
    n7["bob-cli-kx.2.1.4: Constrained label mutations and fake transport [closed]"]
    n8["bob-cli-kx.2.1.5: Archive eligibility and digest-confirmed batch planning [closed]"]
    n9["bob-cli-kx.2.1.6: Archive apply, let-go, and crash reconciliation [closed]"]
    n10["bob-cli-kx.2.1.7: Reports, doctor, documentation, and conformance audit [in_progress]"]
    n11["bob-cli-kx.3: Undo command and receipt surfaces [in_progress]"]
    n12["bob-cli-kx.4: Close-time notice polish [in_progress]"]
    n13["bob-cli-kx.5: Gated live enable and verification [in_progress]"]
    n0 --> n1
    n0 --> n2
    n2 --> n3
    n3 --> n4
    n3 --> n5
    n3 --> n6
    n3 --> n7
    n3 --> n8
    n3 --> n9
    n3 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n1 -.-> n2
    n2 -.-> n11
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
    n7 -.-> n8
    n8 -.-> n9
    n9 -.-> n10
    n11 -.-> n12
    n12 -.-> n13
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.1/README.md) | [bob-cli-kx.1](bob-cli-kx.1.md) | 0 |
| [bbugyi200.athena.bob-cli-kx.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.md) | [bob-cli-kx.2](bob-cli-kx.2.md) | 0 |
| [bbugyi200.athena.bob-cli-kx.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.1/README.md) | [bob-cli-kx.2.1.1](bob-cli-kx.2.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-kx.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.2/README.md) | [bob-cli-kx.2.1.2](bob-cli-kx.2.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-kx.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.1.3.md) | [bob-cli-kx.2.1.3](bob-cli-kx.2.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-kx.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.4/README.md) | [bob-cli-kx.2.1.4](bob-cli-kx.2.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-kx.2.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.5/README.md) | [bob-cli-kx.2.1.5](bob-cli-kx.2.1.5.md) | 1 |
| [bbugyi200.athena.bob-cli-kx.2.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.6/README.md) | [bob-cli-kx.2.1.6](bob-cli-kx.2.1.6.md) | 1 |
| [bbugyi200.athena.bob-cli-kx.2.1.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.7/README.md) | [bob-cli-kx.2.1.7](bob-cli-kx.2.1.7.md) | 0 |
| [bbugyi200.athena.bob-cli-kx.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.land/README.md) | [bob-cli-kx.2.1](bob-cli-kx.2.1.md) | 0 |
| [bbugyi200.athena.bob-cli-kx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3/README.md) | [bob-cli-kx.3](bob-cli-kx.3.md) | 0 |
| [bbugyi200.athena.bob-cli-kx.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.4/README.md) | [bob-cli-kx.4](bob-cli-kx.4.md) | 0 |
| [bbugyi200.athena.bob-cli-kx.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.5/README.md) | [bob-cli-kx.5](bob-cli-kx.5.md) | 0 |
| [bbugyi200.athena.bob-cli-kx.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.land/README.md) | [bob-cli-kx](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`677e740`](https://github.com/bobs-org/bob-cli/commit/677e7407a7dc4b9b65c680784d3d9d8433b0523c) | feat(gmail): add archive config and modify login scope | [bob-cli-kx.2.1.1](bob-cli-kx.2.1.1.md) | 2026-11-12 12:36:22 EST |
| bob-cli | [`92b52e4`](https://github.com/bobs-org/bob-cli/commit/92b52e4f66d619109f9b49c37ecf24931361d972) | feat(gmail)!: add strict archive evidence scan | [bob-cli-kx.2.1.2](bob-cli-kx.2.1.2.md) | 2026-11-12 13:58:04 EST |
| bob-cli | [`4c2cb87`](https://github.com/bobs-org/bob-cli/commit/4c2cb87885f88df245f72243f72a484969fa30dc) | feat(gmail): add archive state journal | [bob-cli-kx.2.1.3](bob-cli-kx.2.1.3.md) | 2026-11-12 15:48:06 EST |
| bob-cli | [`8e78584`](https://github.com/bobs-org/bob-cli/commit/8e78584d5b93b7a978017096adef8bad3587b381) | feat(gmail)!: add constrained archive label transport | [bob-cli-kx.2.1.4](bob-cli-kx.2.1.4.md) | 2026-11-12 16:47:51 EST |
| bob-cli | [`0b806ae`](https://github.com/bobs-org/bob-cli/commit/0b806ae83fc4285c60eee2e631ee5678c757b732) | feat(gmail)!: add digest-confirmed archive batch planning preview | [bob-cli-kx.2.1.5](bob-cli-kx.2.1.5.md) | 2026-11-12 19:45:47 EST |
| bob-cli | [`62ad26d`](https://github.com/bobs-org/bob-cli/commit/62ad26d7472c4ee98153a9ac8a86d661faa5b4f4) | feat(gmail)!: add archive apply, let-go and crash reconciliation | [bob-cli-kx.2.1.6](bob-cli-kx.2.1.6.md) | 2026-11-12 21:21:27 EST |
