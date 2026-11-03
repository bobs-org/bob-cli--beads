# Bead: bob-cli-gh — Period notes that add up: a whole-ISO-week Week → Quarter → Year → All-time tree with stats strips, parts tables, and reviews Bryan closes

[Bead Pages](../README.md) / bob-cli-gh

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.34.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.34.linker.w0.md) · **Assignee:** `bob-cli-gh.land`
**Created:** 2026-11-03 10:55:43 EST
**Plan:** [202611/period\_notes\_and\_stats\_strips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_notes_and_stats_strips.md)

## Description

Every daily note's parent is its ISO week note, and the tree climbs week → quarter → year → all_time → org with no dangling links. bob creates each period note ahead of time from a deterministic scaffold and never edits a note it did not just create. Every week, quarter, year, and all-time note opens with a live stats strip — the Day strip's family: the same five facts as period totals, a typical line, root and type lanes, and a parts row of its child periods — and a live parts table that summarizes each child automatically, with or without an agent. Each note carries complete, versioned agent instructions, so "Update 2026/2026-W45.md" is a whole prompt: agents take every number from `bob periods brief` and save only through `bob periods draft`, which never overwrites Bryan's edits. gtd_daily.md runs a Monday weekly review plus calendar-anchored quarterly and yearly reviews, and the glossary and decision records name the new pieces.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-gh.1](bob-cli-gh.1.md) | Glossary strands and decision records | ✓ closed | small | 2026-11-03 | 2 | 2 |
| [bob-cli-gh.2](bob-cli-gh.2.md) | Period calendar, scaffolds, note parser, and bob periods ensure/list | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.3](bob-cli-gh.3.md) | Period report — bob periods show and period stats ranges | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.4](bob-cli-gh.4.md) | Vault adoption — bob periods migrate, problems report, nightly check | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.5](bob-cli-gh.5.md) | Agent reviews — bob periods brief, draft, and instruction refresh | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.6](bob-cli-gh.6.md) | Period-note creation hook, open-week command, and agent callout style | ◐ in_progress | small | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.7](bob-cli-gh.7.md) | The period stats strip in bob-ledger-tools, week member first | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.8](bob-cli-gh.8.md) | Quarter, year, and all-time strips plus the bob-period-parts table | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.9](bob-cli-gh.9.md) | Vault rollout, review rituals, and live verification | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-gh: Period notes that add up: a whole-ISO-week Week → Quarter → Year → All-time tree with stats strips, parts tables, and reviews Bryan closes [in_progress]"]
    n1["bob-cli-gh.1: Glossary strands and decision records [closed]"]
    n2["bob-cli-gh.2: Period calendar, scaffolds, note parser, and bob periods ensure/list [in_progress]"]
    n3["bob-cli-gh.3: Period report — bob periods show and period stats ranges [in_progress]"]
    n4["bob-cli-gh.4: Vault adoption — bob periods migrate, problems report, nightly check [in_progress]"]
    n5["bob-cli-gh.5: Agent reviews — bob periods brief, draft, and instruction refresh [in_progress]"]
    n6["bob-cli-gh.6: Period-note creation hook, open-week command, and agent callout style [in_progress]"]
    n7["bob-cli-gh.7: The period stats strip in bob-ledger-tools, week member first [in_progress]"]
    n8["bob-cli-gh.8: Quarter, year, and all-time strips plus the bob-period-parts table [in_progress]"]
    n9["bob-cli-gh.9: Vault rollout, review rituals, and live verification [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n1 -.-> n9
    n2 -.-> n3
    n2 -.-> n4
    n2 -.-> n6
    n3 -.-> n5
    n3 -.-> n7
    n4 -.-> n9
    n5 -.-> n9
    n6 -.-> n9
    n7 -.-> n8
    n8 -.-> n9
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gh.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gh.1.md) | [bob-cli-gh.1](bob-cli-gh.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-gh.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gh.2/README.md) | [bob-cli-gh.2](bob-cli-gh.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-gh.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gh.3/README.md) | [bob-cli-gh.3](bob-cli-gh.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-gh.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gh.4/README.md) | [bob-cli-gh.4](bob-cli-gh.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-gh.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gh.5/README.md) | [bob-cli-gh.5](bob-cli-gh.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-gh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gh.6/README.md) | [bob-cli-gh.6](bob-cli-gh.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-gh.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gh.7/README.md) | [bob-cli-gh.7](bob-cli-gh.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-gh.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gh.8/README.md) | [bob-cli-gh.8](bob-cli-gh.8.md) | 0 |
| [bbugyi200.apollo.bob-cli-gh.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gh.9/README.md) | [bob-cli-gh.9](bob-cli-gh.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-gh.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gh.land/README.md) | [bob-cli-gh](README.md) | 0 |
| [bbugyi200.athena.bob-cli-gh.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gh.1.md) | [bob-cli-gh.1](bob-cli-gh.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2a9640a`](https://github.com/bobs-org/bob-cli/commit/2a9640a6b20c4bcb42e5e0a7cfe3eb347b5d1b44) | docs(memory): add Stats Strip and Period Note glossary strands | [bob-cli-gh.1](bob-cli-gh.1.md) | 2026-11-03 11:09:56 EST |
| bob-cli | [`4ce7909`](https://github.com/bobs-org/bob-cli/commit/4ce79094aaf3cf8753bb438a17cd3d9b40afa02a) | docs(memory): add Period Note and Stats Strip glossary terms | [bob-cli-gh.1](bob-cli-gh.1.md) | 2026-11-03 11:31:20 EST |
