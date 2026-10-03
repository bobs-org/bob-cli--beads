# Bead: bob-cli-3n — Task dependency links: one Depends-On line, a vault-wide Ctrl+Shift+P picker, and live chips

[Bead Pages](../README.md) / bob-cli-3n

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vl.md) · **Assignee:** `bob-cli-3n.land`
**Created:** 2026-10-02 16:54:34 EDT
**Plan:** [202610/task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links.md)

## Description

A task's prerequisites live as plain task dependency links on one managed `⛓️ **DEPENDS ON:**` first-child line. That line is the source of truth, and the `[dependsOn::]` / `[id::]` fields are derived from it. Ctrl+Shift+P adds and removes prerequisites by fuzzy-searching every open task in the vault. bob-ledger-tools draws each link as a live status chip. The vault no longer uses transcluded dependency bullets. The glossary, docs, and decision records describe the new contract.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-3n.1](bob-cli-3n.1.md) | Dependency-line contract doc and conformance vectors | ✓ closed | medium | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.10](bob-cli-3n.10.md) | Migrate the vault to Depends-On lines | ✓ closed | medium | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.11](bob-cli-3n.11.md) | Publish glossary, decision record, and final docs | ✓ closed | small | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.2](bob-cli-3n.2.md) | Rust dependency-line parser, promotion edges, and parser guards | ✓ closed | medium | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.3](bob-cli-3n.3.md) | R1-R10 reconciliation in bob task-status-hooks | ✓ closed | medium | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.4](bob-cli-3n.4.md) | bob-ledger-tools live dependency chips | ✓ closed | medium | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.5](bob-cli-3n.5.md) | task-status-cycler and block-id-prompt compatibility | ✓ closed | medium | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.6](bob-cli-3n.6.md) | Navigation-hotkeys dependency model, single-transaction writer, and api v1 | ✓ closed | medium | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.7](bob-cli-3n.7.md) | Vault-wide Ctrl+Shift+P Depends on stage | ✓ closed | medium | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.8](bob-cli-3n.8.md) | Gesture cleanup, hand-edit mirror, and legacy writer removal | ✓ closed | medium | 2026-10-02 | 1 | 1 |
| [bob-cli-3n.9](bob-cli-3n.9.md) | Install bob and sync plugins on every machine | ✓ closed | small | 2026-10-02 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-3n: Task dependency links: one Depends-On line, a vault-wide Ctrl+Shift+P picker, and live chips [in_progress]"]
    n1["bob-cli-3n.1: Dependency-line contract doc and conformance vectors [closed]"]
    n2["bob-cli-3n.10: Migrate the vault to Depends-On lines [closed]"]
    n3["bob-cli-3n.11: Publish glossary, decision record, and final docs [closed]"]
    n4["bob-cli-3n.2: Rust dependency-line parser, promotion edges, and parser guards [closed]"]
    n5["bob-cli-3n.3: R1-R10 reconciliation in bob task-status-hooks [closed]"]
    n6["bob-cli-3n.4: bob-ledger-tools live dependency chips [closed]"]
    n7["bob-cli-3n.5: task-status-cycler and block-id-prompt compatibility [closed]"]
    n8["bob-cli-3n.6: Navigation-hotkeys dependency model, single-transaction writer, and api v1 [closed]"]
    n9["bob-cli-3n.7: Vault-wide Ctrl+Shift+P Depends on stage [closed]"]
    n10["bob-cli-3n.8: Gesture cleanup, hand-edit mirror, and legacy writer removal [closed]"]
    n11["bob-cli-3n.9: Install bob and sync plugins on every machine [closed]"]
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
    n1 -.-> n4
    n1 -.-> n6
    n1 -.-> n7
    n1 -.-> n8
    n2 -.-> n3
    n4 -.-> n5
    n5 -.-> n11
    n6 -.-> n8
    n6 -.-> n11
    n7 -.-> n8
    n7 -.-> n11
    n8 -.-> n9
    n9 -.-> n10
    n9 -.-> n11
    n10 -.-> n11
    n11 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.1/README.md) | [bob-cli-3n.1](bob-cli-3n.1.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.10/README.md) | [bob-cli-3n.10](bob-cli-3n.10.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.11/README.md) | [bob-cli-3n.11](bob-cli-3n.11.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.2/README.md) | [bob-cli-3n.2](bob-cli-3n.2.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.3/README.md) | [bob-cli-3n.3](bob-cli-3n.3.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.4/README.md) | [bob-cli-3n.4](bob-cli-3n.4.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.5/README.md) | [bob-cli-3n.5](bob-cli-3n.5.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.6/README.md) | [bob-cli-3n.6](bob-cli-3n.6.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.7/README.md) | [bob-cli-3n.7](bob-cli-3n.7.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.8/README.md) | [bob-cli-3n.8](bob-cli-3n.8.md) | 1 |
| [bbugyi200.athena.bob-cli-3n.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.9/README.md) | [bob-cli-3n.9](bob-cli-3n.9.md) | 0 |
| [bbugyi200.athena.bob-cli-3n.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.land/README.md) | [bob-cli-3n](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f4b0d12`](https://github.com/bobs-org/bob-cli/commit/f4b0d12b447f43bdceb6844ed1229fda6e4fd20a) | docs(tasks): document task dependency contract with DK vector coverage | [bob-cli-3n.1](bob-cli-3n.1.md) | 2026-10-02 17:35:53 EDT |
| bob-plugins | [`bob-plugins@1831db4`](https://github.com/bobs-org/bob-plugins/commit/1831db4b9d56eb71bc7b7a02d62799696e350170) | feat(bob-ledger-tools): live dependency chips 1.17.0 -\> 1.18.0 | [bob-cli-3n.4](bob-cli-3n.4.md) | 2026-10-02 19:06:53 EDT |
| bob-plugins | [`bob-plugins@e7baeb5`](https://github.com/bobs-org/bob-plugins/commit/e7baeb5eb1da203941633a51ccf360bcfb74d9a5) | feat(deps): task-status-cycler and block-id-prompt Depends-On compatibility | [bob-cli-3n.5](bob-cli-3n.5.md) | 2026-10-02 19:16:07 EDT |
| bob-cli | [`2d4d508`](https://github.com/bobs-org/bob-cli/commit/2d4d50835ef449d971920c911903436fe78b0907) | feat(hooks): Rust dependency-line parser, promotion edges, and parser guards | [bob-cli-3n.2](bob-cli-3n.2.md) | 2026-10-02 19:27:39 EDT |
| bob-plugins | [`bob-plugins@5194bc8`](https://github.com/bobs-org/bob-plugins/commit/5194bc80ac71f2d964a82311735f25cdb38fd0c1) | feat(nav): task dependency contract grammar, planner, and single-transaction writer | [bob-cli-3n.6](bob-cli-3n.6.md) | 2026-10-02 20:17:29 EDT |
| bob-cli | [`043d9c5`](https://github.com/bobs-org/bob-cli/commit/043d9c54022b4146d66b29f36b73ee0adf41e635) | feat(hooks): R1-R10 Depends-On reconciliation in bob task-status-hooks | [bob-cli-3n.3](bob-cli-3n.3.md) | 2026-10-02 20:19:21 EDT |
| bob-plugins | [`bob-plugins@08d1560`](https://github.com/bobs-org/bob-plugins/commit/08d15603d22aa11fc2df3f916bd71de4c461baf8) | feat(nav): vault-wide Ctrl+Shift+P Depends on stage (1.54.0) | [bob-cli-3n.7](bob-cli-3n.7.md) | 2026-10-02 20:57:49 EDT |
| bob-plugins | [`bob-plugins@82aec34`](https://github.com/bobs-org/bob-plugins/commit/82aec3481a9a29fce57ba68fdda40a003fb195d8) | feat(nav): gesture cleanup, hand-edit mirror, and legacy writer removal (1.55.0) | [bob-cli-3n.8](bob-cli-3n.8.md) | 2026-10-02 21:36:20 EDT |
| bob-plugins | [`bob-plugins@46ddd1e`](https://github.com/bobs-org/bob-plugins/commit/46ddd1eb52fccb516a2deb4b509590c3a9a37a48) | feat(nav): dry-run-first Depends-On line migration script | [bob-cli-3n.10](bob-cli-3n.10.md) | 2026-10-02 22:20:12 EDT |
| bob-cli | [`f21e856`](https://github.com/bobs-org/bob-cli/commit/f21e856cae4893f482a9a8baeb0417b5ea1501d0) | docs(memory): publish task-deps-are-depends-on-links decision and glossary | [bob-cli-3n.11](bob-cli-3n.11.md) | 2026-10-02 22:35:21 EDT |
