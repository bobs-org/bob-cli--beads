# Bead: bob-cli-kd — Bank — acknowledge every transaction daily, prove it weekly

[Bead Pages](../README.md) / bob-cli-kd

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1be.md) · **Assignee:** `bob-cli-kd.land`
**Created:** 2026-11-11 11:24:16 EST
**Plan:** [202611/bank\_daily\_acknowledgment.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_daily_acknowledgment.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 8 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md

<!-- sase:links:end -->

## Description

Bryan restarts his daily bank habit right away. Every posted transaction and deposit becomes one checkbox row in a monthly bank note under a new `bank` sub-area of `cash`. Typing a row acknowledges it. A weekly `bob bank import` of a Wells Fargo QFX file writes, unchecked, only the rows he missed, and a balance proof shows that nothing was skipped. Every total is computed when it is drawn (terminal, month card, queue card, daily chip) and never written into notes. A missed week costs one sitting to catch up, not a retyping spiral.

## Notes

[2026-11-11T20:42:22Z · research.49.cld] DISCOVERED ISSUE: bob bank ensure (month::plan_insert_day → day_end_line, src/native/bank/month.rs:300) inserts a new day heading right after the previous day's last row block (row + indented children), not at the end of that day's section. Any trailing non-row line of the earlier day — free prose, a plain checklist line, or an empty '- [x] $' stub — is silently moved under the new day; bob bank check reports nothing, and ensure's next-row line then points at the moved line. Repro (synthetic, installed bob 0.5.0 @ 2026-11-11): BOB_NOW=2026-11-12T08:00:00; bob bank ensure -b SB -D 2026-11-11; append '- [x] $13.71 Smashburger', '  - split with Kelly', 'Kelly paid the tip in cash.', '- [ ] call the bank about the fee' under ## Wed Nov 11; bob bank ensure -b SB -D 2026-11-12 → '## Thu Nov 12' lands after the child bullet and the prose + checklist lines now sit under Thu. Contract (docs/bank.md 'Writers insert a missing day heading in date order') implies the day's whole section stays intact. Impact: Bank: open today, the daily-chip ensure, and any import path that reuses plan_insert_day can re-date Bryan's notes. Suggested fix: anchor the insert before the next day heading / at the end of the earlier day's section (trimming trailing blanks), plus a golden test with trailing prose, a plain checklist line, and a stub.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-kd.1](bob-cli-kd.1.md) | Restart the habit in the vault with no code | ✓ closed | small | 2026-11-11 | 1 | 0 |
| [bob-cli-kd.2](bob-cli-kd.2.md) | The bank module, row grammar, and bob bank check | ✓ closed | medium | 2026-11-11 | 1 | 1 |
| [bob-cli-kd.3](bob-cli-kd.3.md) | Read the bank — list, report, ensure, and ack | ✓ closed | medium | 2026-11-11 | 1 | 1 |
| [bob-cli-kd.4](bob-cli-kd.4.md) | Weekly QFX import that writes only what you missed | ◐ in_progress | large | 2026-11-11 | 1 | 0 |
| [bob-cli-kd.5](bob-cli-kd.5.md) | Prove every transaction — coverage, presence, balance | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |
| [bob-cli-kd.6](bob-cli-kd.6.md) | Obsidian bank cards, styled rows, and the daily chip | ◐ in_progress | large | 2026-11-11 | 1 | 0 |
| [bob-cli-kd.7](bob-cli-kd.7.md) | End-to-end proof, the guide, docs audit, memory, and follow-ups | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-kd: Bank — acknowledge every transaction daily, prove it weekly [in_progress]"]
    n1["bob-cli-kd.1: Restart the habit in the vault with no code [closed]"]
    n2["bob-cli-kd.2: The bank module, row grammar, and bob bank check [closed]"]
    n3["bob-cli-kd.3: Read the bank — list, report, ensure, and ack [closed]"]
    n4["bob-cli-kd.4: Weekly QFX import that writes only what you missed [in_progress]"]
    n5["bob-cli-kd.4.1: Weekly bank import with deterministic matching and one guarded commit [in_progress]"]
    n6["bob-cli-kd.4.1.1: Parse bank exports and establish the shared journal [closed]"]
    n7["bob-cli-kd.4.1.2: Plan only missing rows and preserve existing writing [closed]"]
    n8["bob-cli-kd.4.1.3: Ship the guarded import command and recovery tests [closed]"]
    n9["bob-cli-kd.4.1.4: Document the import and install the Monday ritual [in_progress]"]
    n10["bob-cli-kd.5: Prove every transaction — coverage, presence, balance [in_progress]"]
    n11["bob-cli-kd.6: Obsidian bank cards, styled rows, and the daily chip [in_progress]"]
    n12["bob-cli-kd.6.1: Bank views and safe editing in Obsidian [in_progress]"]
    n13["bob-cli-kd.6.1.1: Bank JSON data service and shared presentation models [closed]"]
    n14["bob-cli-kd.6.1.2: Safe bank gestures, commands, and typing helpers [closed]"]
    n15["bob-cli-kd.6.1.3: Month and queue cards with the daily bank chip [in_progress]"]
    n16["bob-cli-kd.6.1.4: Bank row and day-heading rendering in both Obsidian views [in_progress]"]
    n17["bob-cli-kd.6.1.5: Fixture walkthrough, documentation, and deployment proof [in_progress]"]
    n18["bob-cli-kd.7: End-to-end proof, the guide, docs audit, memory, and follow-ups [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n4 --> n5
    n5 --> n6
    n5 --> n7
    n5 --> n8
    n5 --> n9
    n0 --> n10
    n0 --> n11
    n11 --> n12
    n12 --> n13
    n12 --> n14
    n12 --> n15
    n12 --> n16
    n12 --> n17
    n0 --> n18
    n1 -.-> n18
    n2 -.-> n3
    n3 -.-> n4
    n3 -.-> n11
    n4 -.-> n10
    n6 -.-> n7
    n7 -.-> n8
    n8 -.-> n9
    n10 -.-> n18
    n11 -.-> n18
    n13 -.-> n14
    n14 -.-> n15
    n15 -.-> n16
    n16 -.-> n17
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.1/README.md) | [bob-cli-kd.1](bob-cli-kd.1.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.2.md) | [bob-cli-kd.2](bob-cli-kd.2.md) | 1 |
| [bbugyi200.athena.bob-cli-kd.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.3/README.md) | [bob-cli-kd.3](bob-cli-kd.3.md) | 1 |
| [bbugyi200.athena.bob-cli-kd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.md) | [bob-cli-kd.4](bob-cli-kd.4.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.1/README.md) | [bob-cli-kd.4.1.1](bob-cli-kd.4.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-kd.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.2/README.md) | [bob-cli-kd.4.1.2](bob-cli-kd.4.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-kd.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.1.3.md) | [bob-cli-kd.4.1.3](bob-cli-kd.4.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-kd.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.4/README.md) | [bob-cli-kd.4.1.4](bob-cli-kd.4.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.land/README.md) | [bob-cli-kd.4.1](bob-cli-kd.4.1.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.5/README.md) | [bob-cli-kd.5](bob-cli-kd.5.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.md) | [bob-cli-kd.6](bob-cli-kd.6.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.1/README.md) | [bob-cli-kd.6.1.1](bob-cli-kd.6.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.2/README.md) | [bob-cli-kd.6.1.2](bob-cli-kd.6.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.1.3.md) | [bob-cli-kd.6.1.3](bob-cli-kd.6.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.4/README.md) | [bob-cli-kd.6.1.4](bob-cli-kd.6.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.6.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.5/README.md) | [bob-cli-kd.6.1.5](bob-cli-kd.6.1.5.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.land/README.md) | [bob-cli-kd.6.1](bob-cli-kd.6.1.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.7/README.md) | [bob-cli-kd.7](bob-cli-kd.7.md) | 0 |
| [bbugyi200.athena.bob-cli-kd.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.land/README.md) | [bob-cli-kd](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`07f1c74`](https://github.com/bobs-org/bob-cli/commit/07f1c7442bb24d50658167856fb5816312199423) | feat(bank): add bank grammar, month notes, and read-only bob bank check | [bob-cli-kd.2](bob-cli-kd.2.md) | 2026-11-11 12:58:45 EST |
| bob-cli | [`49218b3`](https://github.com/bobs-org/bob-cli/commit/49218b38ebf3372b44274fa94869ad7ccc58311c) | feat(bank): add list, report, ensure, and ack to bob bank | [bob-cli-kd.3](bob-cli-kd.3.md) | 2026-11-11 13:58:05 EST |
| bob-cli | [`bffbf36`](https://github.com/bobs-org/bob-cli/commit/bffbf36bd58d79868e4bf2b2db042bcab50f4635) | feat(bank): parse OFX/CSV exports and fold the bank journal | [bob-cli-kd.4.1.1](bob-cli-kd.4.1.1.md) | 2026-11-11 15:06:39 EST |
| bob-cli | [`ee2d2cb`](https://github.com/bobs-org/bob-cli/commit/ee2d2cbf0a837c5b735d26d462fbce60e34d269c) | feat(bank): add import planner and payee naming for match-name plan | [bob-cli-kd.4.1.2](bob-cli-kd.4.1.2.md) | 2026-11-11 16:39:22 EST |
| bob-cli | [`d9f0539`](https://github.com/bobs-org/bob-cli/commit/d9f0539f61830be7296f311f086496c1fd491cbb) | feat(bank): add guarded import command and recovery | [bob-cli-kd.4.1.3](bob-cli-kd.4.1.3.md) | 2026-11-11 19:20:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.3][1] | Need epic scope and decisions | 1 |
| read-by | [agent:bob-cli-kf.land][2] | Check whether the active bank epic owns bank ensure line/append work that overlaps bob-cli-kf.4 integration | 1 |
| read-by | [agent:research.49.cdx][3] | Research first bank acknowledgement and end-to-end epic verification | 1 |
| read-by | [agent:research.49.cld][4] | research: write user guide for first-time bank transaction acknowledgment and e2e test of the epic | 2 |
| read-by | [agent:research.49.final][5] | Confirm current epic phase state for the consolidated first-ack + e2e guide | 1 |
| read-by | [agent:research.49.gem][6] | Research epic details and requirements for first-time bank transaction ack and e2e testing | 1 |
| read-by | [agent:research.49.grk][7] | Need the epic scope, phases, and e2e wrap-up so the first-run bank-ack guide matches the live bead | 1 |
| read-by | [agent:research.49.mus][8] | researching user guide for first bank transaction acknowledge and e2e test of kd epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kf.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cdx/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cld/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.final/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.gem/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.grk/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.mus/README.md

<!-- sase:referenced-by:end -->
