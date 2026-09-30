# Bead: bob-cli-2y — Retire #now: sticky Next/Pending lanes and a ledger-derived Today

[Bead Pages](../README.md) / bob-cli-2y

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.land`
**Created:** 2026-09-30 16:41:59 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

Linking a task makes it Next, working it makes it Pending, and no unlink path (hooks, keymap, capture drop, hand deletion) ever lowers it; only an explicit one-key release returns it to Ready. Today is read from the ledger when the dash renders, the dash shows mutually exclusive TODAY / PENDING / NEXT / READY sections with soft caps, and #now is gone from bob-cli, bob-plugins, Bob Mac Capture, the vault, and memory.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-2y.1](bob-cli-2y.1.md) | Pause the MacBook's hooks cron before the first 2026-10-01 pass | ✓ closed | small | 2026-09-30 | 1 | 0 |
| [bob-cli-2y.10](bob-cli-2y.10.md) | Mutually exclusive dash sections, GTD chores, and lane caps config | ◐ in_progress | small | 2026-09-30 | 1 | 0 |
| [bob-cli-2y.11](bob-cli-2y.11.md) | Bob Mac Capture drops #now and presents the link-presence toggle | ◐ in_progress | medium | 2026-09-30 | 1 | 0 |
| [bob-cli-2y.12](bob-cli-2y.12.md) | Install, deploy, end-to-end check, and Bryan's checklist | ◐ in_progress | small | 2026-09-30 | 1 | 0 |
| [bob-cli-2y.2](bob-cli-2y.2.md) | Sticky lanes in bob task-status-hooks, docs, and superseding decision records | ✓ closed | medium | 2026-09-30 | 1 | 1 |
| [bob-cli-2y.3](bob-cli-2y.3.md) | Install sticky hooks on the MacBook and restore the cron | ✓ closed | small | 2026-09-30 | 1 | 0 |
| [bob-cli-2y.4](bob-cli-2y.4.md) | No bob capture path lowers a lane | ✓ closed | medium | 2026-09-30 | 1 | 1 |
| [bob-cli-2y.5](bob-cli-2y.5.md) | Define Today once; NEXT/PENDING lanes replace NOW in bob plan and the hooks | ✓ closed | medium | 2026-09-30 | 1 | 0 |
| [bob-cli-2y.6](bob-cli-2y.6.md) | Remove | ◐ in_progress | medium | 2026-09-30 | 1 | 0 |
| [bob-cli-2y.7](bob-cli-2y.7.md) | bob-ledger-tools api v2 with a synchronous Today, lane budgets, and query refresh | ◐ in_progress | medium | 2026-09-30 | 1 | 0 |
| [bob-cli-2y.8](bob-cli-2y.8.md) | Ctrl+Shift+Enter toggles on link presence and never changes the lane | ✓ closed | medium | 2026-09-30 | 1 | 1 |
| [bob-cli-2y.9](bob-cli-2y.9.md) | Alt+N commits or releases a lane; #now leaves Bob Navigation Hotkeys | ◐ in_progress | medium | 2026-09-30 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-2y: Retire #now: sticky Next/Pending lanes and a ledger-derived Today [in_progress]"]
    n1["bob-cli-2y.1: Pause the MacBook's hooks cron before the first 2026-10-01 pass [closed]"]
    n2["bob-cli-2y.10: Mutually exclusive dash sections, GTD chores, and lane caps config [in_progress]"]
    n3["bob-cli-2y.11: Bob Mac Capture drops #now and presents the link-presence toggle [in_progress]"]
    n4["bob-cli-2y.12: Install, deploy, end-to-end check, and Bryan's checklist [in_progress]"]
    n5["bob-cli-2y.2: Sticky lanes in bob task-status-hooks, docs, and superseding decision records [closed]"]
    n6["bob-cli-2y.3: Install sticky hooks on the MacBook and restore the cron [closed]"]
    n7["bob-cli-2y.4: No bob capture path lowers a lane [closed]"]
    n8["bob-cli-2y.5: Define Today once; NEXT/PENDING lanes replace NOW in bob plan and the hooks [closed]"]
    n9["bob-cli-2y.6: Remove [in_progress]"]
    n10["bob-cli-2y.7: bob-ledger-tools api v2 with a synchronous Today, lane budgets, and query refresh [in_progress]"]
    n11["bob-cli-2y.8: Ctrl+Shift+Enter toggles on link presence and never changes the lane [closed]"]
    n12["bob-cli-2y.9: Alt+N commits or releases a lane; #now leaves Bob Navigation Hotkeys [in_progress]"]
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
    n1 -.-> n6
    n2 -.-> n4
    n3 -.-> n4
    n5 -.-> n6
    n5 -.-> n7
    n5 -.-> n8
    n5 -.-> n11
    n6 -.-> n4
    n7 -.-> n3
    n7 -.-> n9
    n8 -.-> n9
    n8 -.-> n10
    n9 -.-> n3
    n9 -.-> n4
    n10 -.-> n2
    n10 -.-> n12
    n11 -.-> n2
    n11 -.-> n12
    n12 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.1/README.md) | [bob-cli-2y.1](bob-cli-2y.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-2y.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.10/README.md) | [bob-cli-2y.10](bob-cli-2y.10.md) | 0 |
| [bbugyi200.apollo.bob-cli-2y.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.11/README.md) | [bob-cli-2y.11](bob-cli-2y.11.md) | 0 |
| [bbugyi200.apollo.bob-cli-2y.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.12/README.md) | [bob-cli-2y.12](bob-cli-2y.12.md) | 0 |
| [bbugyi200.apollo.bob-cli-2y.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.2/README.md) | [bob-cli-2y.2](bob-cli-2y.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-2y.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.3/README.md) | [bob-cli-2y.3](bob-cli-2y.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-2y.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.4/README.md) | [bob-cli-2y.4](bob-cli-2y.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-2y.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.5/README.md) | [bob-cli-2y.5](bob-cli-2y.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-2y.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.6/README.md) | [bob-cli-2y.6](bob-cli-2y.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-2y.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.7/README.md) | [bob-cli-2y.7](bob-cli-2y.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-2y.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.8/README.md) | [bob-cli-2y.8](bob-cli-2y.8.md) | 1 |
| [bbugyi200.apollo.bob-cli-2y.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.9/README.md) | [bob-cli-2y.9](bob-cli-2y.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-2y.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.land/README.md) | [bob-cli-2y](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`33d5622`](https://github.com/bobs-org/bob-cli/commit/33d5622a466b72a0254f7b7866b3ebd6243fa11a) | feat(hooks): make Next/In-Progress lanes sticky outside daily notes | [bob-cli-2y.2](bob-cli-2y.2.md) | 2026-09-30 17:11:06 EDT |
| bob-cli | [`63305f0`](https://github.com/bobs-org/bob-cli/commit/63305f02b7d437e7830f89d6ba919a43a9a15a6e) | feat(capture): make @route+id! a link-presence toggle that never lowers a lane | [bob-cli-2y.4](bob-cli-2y.4.md) | 2026-09-30 17:31:39 EDT |
| bob-cli | [`85f7901`](https://github.com/bobs-org/bob-cli/commit/85f79018ab2e47075c9123c3a03c8ef2f9805f85) | docs(memory): unlinking an In Progress task keeps its lane in the Work Log strand | [bob-cli-2y.8](bob-cli-2y.8.md) | 2026-09-30 17:32:20 EDT |
