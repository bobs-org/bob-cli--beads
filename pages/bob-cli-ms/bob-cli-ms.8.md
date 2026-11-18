# Bead: bob-cli-ms.8 — Finish the Record Card: the title moves into the sheet, records drop their H1, and real Obsidian proves it

[Bead Pages](../README.md) / [bob-cli-ms](README.md) / bob-cli-ms.8

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ms.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.land.md) · **Assignee:** `bob-cli-ms.8.land`
**Created:** 2026-11-17 22:26:14 EST
**Plan:** [202611/record\_card\_title\_and\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card_title_and_proof.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/record_card_title_and_proof.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card_title_and_proof.md

<!-- sase:links:end -->

## Description

Every record note shows its title at the top of the record sheet instead of an H1. bob writes and keeps record notes without an H1, and the live vault has none. The record-sheet tests pass on any date. A real-Obsidian walkthrough on athena proves the Record Card epic acceptance, including the Properties hide.

## Notes

[2026-11-18T15:51:43Z · bob-cli-n7.land] DISCOVERED ISSUE: bob-cli-n7 landing triage of n7.3 PROPOSED FOLLOW-UP notes #1/#5. Commit 2f80442b (ms.8.2) introduced an unformatted .all closure at tests/cli/albums_create.rs:1149. Independently reproduced cargo fmt --all -- --check exit 1 on clean f0857be8; GitHub master run 44335332552 lint job 134910728869 has the identical diff, ubuntu tests/package pass and macOS is cancelled. No semantic duplicate in task search or all 68 last-week tasks. This is causally owned by ms.8, so no new task. n7 landing closeout tale will apply the one-line rustfmt-only integration repair while preserving the H1-less assertion.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.8.land/README.md) | [bob-cli-ms.8](bob-cli-ms.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-na.1][1] | Check whether the active Record Card epic already tracks the same clean-base rustfmt failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-na.1/README.md

<!-- sase:referenced-by:end -->
