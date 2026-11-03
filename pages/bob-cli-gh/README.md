# Bead: bob-cli-gh — Period notes that add up: a whole-ISO-week Week → Quarter → Year → All-time tree with stats strips, parts tables, and reviews Bryan closes

[Bead Pages](../README.md) / bob-cli-gh

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.34.linker.w0` · **Assignee:** `bob-cli-gh.land`
**Created:** 2026-11-03 10:55:43 EST
**Plan:** [202611/period\_notes\_and\_stats\_strips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_notes_and_stats_strips.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/period_notes_and_stats_strips.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_notes_and_stats_strips.md

<!-- sase:links:end -->

## Description

Every daily note's parent is its ISO week note, and the tree climbs week → quarter → year → all_time → org with no dangling links. bob creates each period note ahead of time from a deterministic scaffold and never edits a note it did not just create. Every week, quarter, year, and all-time note opens with a live stats strip — the Day strip's family: the same five facts as period totals, a typical line, root and type lanes, and a parts row of its child periods — and a live parts table that summarizes each child automatically, with or without an agent. Each note carries complete, versioned agent instructions, so "Update 2026/2026-W45.md" is a whole prompt: agents take every number from `bob periods brief` and save only through `bob periods draft`, which never overwrites Bryan's edits. gtd_daily.md runs a Monday weekly review plus calendar-anchored quarterly and yearly reviews, and the glossary and decision records name the new pieces.

## Notes

[2026-11-03T16:48:31Z · bob-cli-gf.land] DISCOVERED ISSUE: bob-cli-gf.land reproduced generated docs drift on bob-cli e9deb7f8 via bob-plugins npm run docs:check (46b25c6): docs/reference/glossary.md is out of date. gh.1 commits 2a9640a6 and 4ce79094 add/reword Period Note, Stats Strip, and Day Strip but do not regenerate that published glossary; the new terms are absent there. Please regenerate via just docs-gen and verify just docs-check during gh integration. No gf source change causes this; attaching to this active epic rather than making a duplicate task. gg.2 note #3 independently reported glossary drift.

[2026-11-03T17:21:35Z · bob-cli-gg.land] DISCOVERED ISSUE: bob-cli-gg landing corroborates gh.1 generated glossary drift, proposed independently by bob-cli-gg.2 note #3 and bob-cli-gg.3 note #2. On bob-cli a5e1c519 and clean bob-plugins 84ea548, npm run docs:check passes lint and plugin inventory then fails: out of date: docs/reference/glossary.md (run just docs-gen). gh.1 commits 2a9640a6/4ce79094 changed Period Note, Stats Strip, and Day Strip without regenerating the published glossary. Same causal issue as gh note #1; please regenerate and run both docs gates during gh integration. No gg source causes it; no duplicate task created.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-gh.1](bob-cli-gh.1.md) | Glossary strands and decision records | ✓ closed | small | 2026-11-03 | 2 | 2 |
| [bob-cli-gh.2](bob-cli-gh.2.md) | Period calendar, scaffolds, note parser, and bob periods ensure/list | ✓ closed | medium | 2026-11-03 | 1 | 1 |
| [bob-cli-gh.3](bob-cli-gh.3.md) | Period report — bob periods show and period stats ranges | ✓ closed | medium | 2026-11-03 | 1 | 1 |
| [bob-cli-gh.4](bob-cli-gh.4.md) | Vault adoption — bob periods migrate, problems report, nightly check | ✓ closed | medium | 2026-11-03 | 1 | 1 |
| [bob-cli-gh.5](bob-cli-gh.5.md) | Agent reviews — bob periods brief, draft, and instruction refresh | ✓ closed | medium | 2026-11-03 | 1 | 1 |
| [bob-cli-gh.6](bob-cli-gh.6.md) | Period-note creation hook, open-week command, and agent callout style | ✓ closed | small | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.7](bob-cli-gh.7.md) | The period stats strip in bob-ledger-tools, week member first | ✓ closed | medium | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.8](bob-cli-gh.8.md) | Quarter, year, and all-time strips plus the bob-period-parts table | ✓ closed | medium | 2026-11-03 | 1 | 0 |
| [bob-cli-gh.9](bob-cli-gh.9.md) | Vault rollout, review rituals, and live verification | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-gh: Period notes that add up: a whole-ISO-week Week → Quarter → Year → All-time tree with stats strips, parts tables, and reviews Bryan closes [in_progress]"]
    n1["bob-cli-gh.1: Glossary strands and decision records [closed]"]
    n2["bob-cli-gh.2: Period calendar, scaffolds, note parser, and bob periods ensure/list [closed]"]
    n3["bob-cli-gh.3: Period report — bob periods show and period stats ranges [closed]"]
    n4["bob-cli-gh.4: Vault adoption — bob periods migrate, problems report, nightly check [closed]"]
    n5["bob-cli-gh.5: Agent reviews — bob periods brief, draft, and instruction refresh [closed]"]
    n6["bob-cli-gh.6: Period-note creation hook, open-week command, and agent callout style [closed]"]
    n7["bob-cli-gh.7: The period stats strip in bob-ledger-tools, week member first [closed]"]
    n8["bob-cli-gh.8: Quarter, year, and all-time strips plus the bob-period-parts table [closed]"]
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
| [bbugyi200.athena.bob-cli-gh.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gh.1.md) | [bob-cli-gh.1](bob-cli-gh.1.md) | 1 |
| [bbugyi200.athena.bob-cli-gh.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.2/README.md) | [bob-cli-gh.2](bob-cli-gh.2.md) | 1 |
| [bbugyi200.athena.bob-cli-gh.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gh.3.md) | [bob-cli-gh.3](bob-cli-gh.3.md) | 1 |
| [bbugyi200.athena.bob-cli-gh.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.4/README.md) | [bob-cli-gh.4](bob-cli-gh.4.md) | 1 |
| [bbugyi200.athena.bob-cli-gh.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.5/README.md) | [bob-cli-gh.5](bob-cli-gh.5.md) | 1 |
| [bbugyi200.athena.bob-cli-gh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.6/README.md) | [bob-cli-gh.6](bob-cli-gh.6.md) | 0 |
| [bbugyi200.athena.bob-cli-gh.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.7/README.md) | [bob-cli-gh.7](bob-cli-gh.7.md) | 0 |
| [bbugyi200.athena.bob-cli-gh.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.8/README.md) | [bob-cli-gh.8](bob-cli-gh.8.md) | 0 |
| [bbugyi200.athena.bob-cli-gh.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.9/README.md) | [bob-cli-gh.9](bob-cli-gh.9.md) | 0 |
| [bbugyi200.athena.bob-cli-gh.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.land/README.md) | [bob-cli-gh](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2a9640a`](https://github.com/bobs-org/bob-cli/commit/2a9640a6b20c4bcb42e5e0a7cfe3eb347b5d1b44) | docs(memory): add Stats Strip and Period Note glossary strands | [bob-cli-gh.1](bob-cli-gh.1.md) | 2026-11-03 11:09:56 EST |
| bob-cli | [`4ce7909`](https://github.com/bobs-org/bob-cli/commit/4ce79094aaf3cf8753bb438a17cd3d9b40afa02a) | docs(memory): add Period Note and Stats Strip glossary terms | [bob-cli-gh.1](bob-cli-gh.1.md) | 2026-11-03 11:31:20 EST |
| bob-cli | [`020a1f6`](https://github.com/bobs-org/bob-cli/commit/020a1f6da021513bc60abdcbda7a4d9ab606fb90) | feat(periods): add ISO period calendar, scaffolds, parser, ensure/list | [bob-cli-gh.2](bob-cli-gh.2.md) | 2026-11-03 11:59:22 EST |
| bob-cli | [`5a1ccf5`](https://github.com/bobs-org/bob-cli/commit/5a1ccf593bb743a9f08c003af550a4b473504540) | feat(periods): adopt the period-note tree (migrate, list -p, nightly) | [bob-cli-gh.4](bob-cli-gh.4.md) | 2026-11-03 13:00:24 EST |
| bob-cli | [`9f88a86`](https://github.com/bobs-org/bob-cli/commit/9f88a861ffa3444058c449b5bdd7218a184e8142) | feat(periods): add period reports and stats ranges | [bob-cli-gh.3](bob-cli-gh.3.md) | 2026-11-03 13:37:09 EST |
| bob-cli | [`13fb39d`](https://github.com/bobs-org/bob-cli/commit/13fb39d0d40c35ee361400a552a29b08ce1bfcaf) | feat(periods): add agent reviews — brief, draft, and instruction refresh | [bob-cli-gh.5](bob-cli-gh.5.md) | 2026-11-03 15:01:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gh.2][1] | Need epic scope and plan linkage | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.2/README.md

<!-- sase:referenced-by:end -->
