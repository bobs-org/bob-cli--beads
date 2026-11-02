# Bead: bob-cli-fs — Starts-after relations offer the next task when one is parked or done

[Bead Pages](../README.md) / bob-cli-fs

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5m.linker.w0.md) · **Assignee:** `bob-cli-fs.land`
**Created:** 2026-11-02 05:57:11 EST
**Plan:** [202611/starts\_after\_relation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/starts_after_relation.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/starts_after_relation.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/starts_after_relation.md

<!-- sase:links:end -->

## Description

A task linked "S starts after T" is offered as a successor (never auto-linked, never blocked) when T is parked (left Pending with no live Task Link today) or done, on every surface, and every surface says plainly which relation and which event fired.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-fs.1](bob-cli-fs.1.md) | Contract, shared vectors, inverse pair, and glossary | ✓ closed | medium | 2026-11-02 | 1 | 1 |
| [bob-cli-fs.10](bob-cli-fs.10.md) | Bob Mac Capture generic group copy and relation presentation | ◐ in_progress | large | 2026-11-02 | 1 | 0 |
| [bob-cli-fs.11](bob-cli-fs.11.md) | Enable starts after in chezmoi and smoke it | ◐ in_progress | small | 2026-11-02 | 1 | 0 |
| [bob-cli-fs.2](bob-cli-fs.2.md) | Rust policy and relation-successor engine | ◐ in_progress | large | 2026-11-02 | 1 | 0 |
| [bob-cli-fs.3](bob-cli-fs.3.md) | Rust authoring indications and relations list | ◐ in_progress | medium | 2026-11-02 | 1 | 0 |
| [bob-cli-fs.4](bob-cli-fs.4.md) | Capture events, snapshot, reporting, and bob-authored group copy | ◐ in_progress | large | 2026-11-02 | 1 | 0 |
| [bob-cli-fs.5](bob-cli-fs.5.md) | Capture unlink hand-offs (v1.1) | ◐ in_progress | medium | 2026-11-02 | 1 | 0 |
| [bob-cli-fs.6](bob-cli-fs.6.md) | Obsidian picker v3 and notice v3 presentation | ✓ closed | medium | 2026-11-02 | 1 | 1 |
| [bob-cli-fs.7](bob-cli-fs.7.md) | Obsidian inverse pair and relation-stage indications | ✓ closed | medium | 2026-11-02 | 1 | 1 |
| [bob-cli-fs.8](bob-cli-fs.8.md) | Obsidian cycler relation-successor engine (Done path) | ◐ in_progress | large | 2026-11-02 | 1 | 0 |
| [bob-cli-fs.9](bob-cli-fs.9.md) | Obsidian unlink hand-offs (v1.1) | ◐ in_progress | medium | 2026-11-02 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-fs: Starts-after relations offer the next task when one is parked or done [in_progress]"]
    n1["bob-cli-fs.1: Contract, shared vectors, inverse pair, and glossary [closed]"]
    n2["bob-cli-fs.10: Bob Mac Capture generic group copy and relation presentation [in_progress]"]
    n3["bob-cli-fs.11: Enable starts after in chezmoi and smoke it [in_progress]"]
    n4["bob-cli-fs.2: Rust policy and relation-successor engine [in_progress]"]
    n5["bob-cli-fs.2.1: Rust relation-successor policy and planner for bob-cli-fs.2 [in_progress]"]
    n6["bob-cli-fs.2.1.1: Successor-label policy and shared copy [closed]"]
    n7["bob-cli-fs.2.1.2: Pure relation extraction and classification [closed]"]
    n8["bob-cli-fs.2.1.3: Merge relation offers into successor planning [in_progress]"]
    n9["bob-cli-fs.3: Rust authoring indications and relations list [in_progress]"]
    n10["bob-cli-fs.4: Capture events, snapshot, reporting, and bob-authored group copy [in_progress]"]
    n11["bob-cli-fs.5: Capture unlink hand-offs (v1.1) [in_progress]"]
    n12["bob-cli-fs.6: Obsidian picker v3 and notice v3 presentation [closed]"]
    n13["bob-cli-fs.7: Obsidian inverse pair and relation-stage indications [closed]"]
    n14["bob-cli-fs.8: Obsidian cycler relation-successor engine (Done path) [in_progress]"]
    n15["bob-cli-fs.8.1: Obsidian cycler relation successors on managed Done [in_progress]"]
    n16["bob-cli-fs.8.1.1: Relation policy, pure rule, and shared copy [closed]"]
    n17["bob-cli-fs.8.1.2: Integrate relation offers with recovery and selection [closed]"]
    n18["bob-cli-fs.8.1.3: Wire managed Done with fresh relation reads and receipts [closed]"]
    n19["bob-cli-fs.8.1.4: Document, validate, and deploy the cycler [in_progress]"]
    n20["bob-cli-fs.9: Obsidian unlink hand-offs (v1.1) [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n4 --> n5
    n5 --> n6
    n5 --> n7
    n5 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n0 --> n14
    n14 --> n15
    n15 --> n16
    n15 --> n17
    n15 --> n18
    n15 --> n19
    n0 --> n20
    n1 -.-> n4
    n1 -.-> n12
    n1 -.-> n13
    n1 -.-> n14
    n2 -.-> n3
    n4 -.-> n9
    n4 -.-> n10
    n6 -.-> n7
    n7 -.-> n8
    n9 -.-> n2
    n9 -.-> n3
    n10 -.-> n2
    n10 -.-> n3
    n10 -.-> n11
    n11 -.-> n2
    n12 -.-> n14
    n13 -.-> n3
    n14 -.-> n3
    n14 -.-> n20
    n16 -.-> n17
    n17 -.-> n18
    n18 -.-> n19
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.1.md) | [bob-cli-fs.1](bob-cli-fs.1.md) | 1 |
| [bbugyi200.athena.bob-cli-fs.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.10/README.md) | [bob-cli-fs.10](bob-cli-fs.10.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.11/README.md) | [bob-cli-fs.11](bob-cli-fs.11.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.2.md) | [bob-cli-fs.2](bob-cli-fs.2.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.1/README.md) | [bob-cli-fs.2.1.1](bob-cli-fs.2.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-fs.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.2/README.md) | [bob-cli-fs.2.1.2](bob-cli-fs.2.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-fs.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.3/README.md) | [bob-cli-fs.2.1.3](bob-cli-fs.2.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.land/README.md) | [bob-cli-fs.2.1](bob-cli-fs.2.1.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.3/README.md) | [bob-cli-fs.3](bob-cli-fs.3.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.4/README.md) | [bob-cli-fs.4](bob-cli-fs.4.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.5/README.md) | [bob-cli-fs.5](bob-cli-fs.5.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.6/README.md) | [bob-cli-fs.6](bob-cli-fs.6.md) | 1 |
| [bbugyi200.athena.bob-cli-fs.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.7/README.md) | [bob-cli-fs.7](bob-cli-fs.7.md) | 1 |
| [bbugyi200.athena.bob-cli-fs.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.8.md) | [bob-cli-fs.8](bob-cli-fs.8.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.8.1.1/README.md) | [bob-cli-fs.8.1.1](bob-cli-fs.8.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-fs.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.8.1.2/README.md) | [bob-cli-fs.8.1.2](bob-cli-fs.8.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-fs.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.8.1.3.md) | [bob-cli-fs.8.1.3](bob-cli-fs.8.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-fs.8.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.8.1.4/README.md) | [bob-cli-fs.8.1.4](bob-cli-fs.8.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.8.1.land/README.md) | [bob-cli-fs.8.1](bob-cli-fs.8.1.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.9/README.md) | [bob-cli-fs.9](bob-cli-fs.9.md) | 0 |
| [bbugyi200.athena.bob-cli-fs.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.land/README.md) | [bob-cli-fs](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0095426`](https://github.com/bobs-org/bob-cli/commit/0095426daa386bd9ff3c1006f228e8a33548bf4e) | feat(task-relations): document successor offer contract | [bob-cli-fs.1](bob-cli-fs.1.md) | 2026-11-02 06:20:05 EST |
| bob-plugins | [`bob-plugins@a3e3462`](https://github.com/bobs-org/bob-plugins/commit/a3e346201fdb0acb0660dd4d263e74f7a080efd6) | feat(nav): show starts-after successor indications in relation stages | [bob-cli-fs.7](bob-cli-fs.7.md) | 2026-11-02 06:47:47 EST |
| bob-plugins | [`bob-plugins@7cc1735`](https://github.com/bobs-org/bob-plugins/commit/7cc17352985be3cb11cf1b6b81bc6cbf74fbb466) | feat(nav-hotkeys): present relation successor picker and notice v3 | [bob-cli-fs.6](bob-cli-fs.6.md) | 2026-11-02 06:55:11 EST |
| bob-cli | [`c3a2e62`](https://github.com/bobs-org/bob-cli/commit/c3a2e62acdec4ca22dc740038862ce5648156461) | feat(task-relations): add successor-label policy and shared copy | [bob-cli-fs.2.1.1](bob-cli-fs.2.1.1.md) | 2026-11-02 07:00:54 EST |
| bob-plugins | [`bob-plugins@4447723`](https://github.com/bobs-org/bob-plugins/commit/4447723dd13eeb09eab9f14f316c306780cafe4d) | feat(task-status-cycler): add relation successor policy, planner, and copy | [bob-cli-fs.8.1.1](bob-cli-fs.8.1.1.md) | 2026-11-02 07:34:01 EST |
| bob-cli | [`ace86f8`](https://github.com/bobs-org/bob-cli/commit/ace86f8e5d7fc9c2103e7513953548b119b6629c) | feat(task-relations): add pure relation-successor classifier | [bob-cli-fs.2.1.2](bob-cli-fs.2.1.2.md) | 2026-11-02 07:39:55 EST |
| bob-plugins | [`bob-plugins@65d25d9`](https://github.com/bobs-org/bob-plugins/commit/65d25d97660160059c4ec746bea9623938a36159) | feat(task-status-cycler): merge relation offers into successor pipeline | [bob-cli-fs.8.1.2](bob-cli-fs.8.1.2.md) | 2026-11-02 08:17:02 EST |
| bob-plugins | [`bob-plugins@f4550e2`](https://github.com/bobs-org/bob-plugins/commit/f4550e297077687c27c441ce8bafed878df3e921) | feat(task-status-cycler): wire relation successors on Done gestures | [bob-cli-fs.8.1.3](bob-cli-fs.8.1.3.md) | 2026-11-02 08:46:59 EST |
