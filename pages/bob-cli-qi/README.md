# Bead: bob-cli-qi — Demote bank.md to a single-owner bank hub, then finish the card epics

[Bead Pages](../README.md) / bob-cli-qi

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gn.md) · **Assignee:** `bob-cli-qi.land`
**Created:** 2026-11-26 10:06:12 EST
**Plan:** [202611/bank\_hub\_demotion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_hub_demotion.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_hub_demotion.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_hub_demotion.md

<!-- sase:links:end -->

## Description

~/bob/bank.md is an untyped, path-canonical bank hub under cash. It has exactly one card (the Bank Card, gated on props_v1), no area semantics in any repo, and no tasks. Every piece of logic that supported the bank/area hybrid is gone. On top of that single-owner model, the unfinished work of the canceled bob-cli-pl and bob-cli-q6 epics is completed: acceptance, polish, cleanup, docs, and deployment.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-qi.1](bob-cli-qi.1.md) | Reparent the subscriptions album and untype bank.md in the vault | ✓ closed | small | 2026-11-26 | 1 | 0 |
| [bob-cli-qi.2](bob-cli-qi.2.md) | Remove the bank area contract from bob and guard the no-tasks hub | ◐ in_progress | medium | 2026-11-26 | 1 | 0 |
| [bob-cli-qi.3](bob-cli-qi.3.md) | Delete the bank/area arbitration and restore the single-owner Bank Card | ◐ in_progress | medium | 2026-11-26 | 1 | 1 |
| [bob-cli-qi.4](bob-cli-qi.4.md) | Real-Obsidian takeover acceptance and family screenshot review | ◐ in_progress | medium | 2026-11-26 | 1 | 0 |
| [bob-cli-qi.5](bob-cli-qi.5.md) | Re-run the retired project-count cleanup in the vault | ◐ in_progress | small | 2026-11-26 | 1 | 0 |
| [bob-cli-qi.6](bob-cli-qi.6.md) | Passive-rendering proof, docs sweep, approved memory, and clean deploy | ◐ in_progress | medium | 2026-11-26 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-qi: Demote bank.md to a single-owner bank hub, then finish the card epics [in_progress]"]
    n1["bob-cli-qi.1: Reparent the subscriptions album and untype bank.md in the vault [closed]"]
    n2["bob-cli-qi.2: Remove the bank area contract from bob and guard the no-tasks hub [in_progress]"]
    n3["bob-cli-qi.3: Delete the bank/area arbitration and restore the single-owner Bank Card [in_progress]"]
    n4["bob-cli-qi.4: Real-Obsidian takeover acceptance and family screenshot review [in_progress]"]
    n5["bob-cli-qi.5: Re-run the retired project-count cleanup in the vault [in_progress]"]
    n6["bob-cli-qi.6: Passive-rendering proof, docs sweep, approved memory, and clean deploy [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n4
    n1 -.-> n5
    n2 -.-> n4
    n2 -.-> n5
    n3 -.-> n4
    n3 -.-> n5
    n4 -.-> n6
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qi.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qi.1/README.md) | [bob-cli-qi.1](bob-cli-qi.1.md) | 0 |
| [bbugyi200.athena.bob-cli-qi.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qi.2/README.md) | [bob-cli-qi.2](bob-cli-qi.2.md) | 0 |
| [bbugyi200.athena.bob-cli-qi.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qi.3.md) | [bob-cli-qi.3](bob-cli-qi.3.md) | 1 |
| [bbugyi200.athena.bob-cli-qi.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qi.4/README.md) | [bob-cli-qi.4](bob-cli-qi.4.md) | 0 |
| [bbugyi200.athena.bob-cli-qi.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qi.5/README.md) | [bob-cli-qi.5](bob-cli-qi.5.md) | 0 |
| [bbugyi200.athena.bob-cli-qi.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qi.6/README.md) | [bob-cli-qi.6](bob-cli-qi.6.md) | 0 |
| [bbugyi200.athena.bob-cli-qi.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qi.land/README.md) | [bob-cli-qi](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8e6a5a6`](https://github.com/bobs-org/bob-plugins/commit/8e6a5a61908bb5eac13584536fa6f564b7464617) | refactor(plugins): restore single-owner Bank Card | [bob-cli-qi.3](bob-cli-qi.3.md) | 2026-11-26 10:40:24 EST |
