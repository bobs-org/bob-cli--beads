# Bead: bob-cli-ji.7.1.4 — Mode entry points, capture preservation, and event picker

[Bead Pages](../README.md) / [bob-cli-ji.7.1](bob-cli-ji.7.1.md) / bob-cli-ji.7.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) · **Assignee:** `bob-cli-ji.7.1.4` · **Size:** medium
**Created:** 2026-11-10 10:29:45 EST · **Closed:** 2026-11-10 15:07:13 EST
**Plan:** [202611/mac\_event\_note\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_event_note_mode.md)

## Description

picker: wire Command-E, Event Note status menu, and Calendar-row URL entry into a surface inside the capture panel with a grouped keyboard picker. Keep the actual capture editor and its undo manager alive; route focus, sizing, Escape, capability, and panel switches without capture writes. Cover the entry and restoration paths in hosted tests. Read Picker and entry.

## Notes

[2026-11-10T19:37:45Z · bob-cli-ji.7.1.4--6] PROPOSED FOLLOW-UP: Pre-existing CaptureAliasTipPanelTests waitUntil timeouts (testFilteringKeepsTheShownTipAnchoredToTheSigil, testOptionTypedHashOpensTheHashTip, testTypingQueryBeforeTheRouteListOpensKeepsTheTip) failed identically on exact-SHA run 42883209970 and base aafed83/6b6052c (runs 42826766066, 42838952067); same class as flake bead bob-cli-jk / bob-cli-ji.7.1.2 follow-up — picker Command-E assertion is the only introduced Test failure

[2026-11-10T20:06:57Z · bob-cli-ji.7.1.4--7] PROPOSED FOLLOW-UP: CaptureAliasTipPanelTests.testEditBeforeTheReplyDropsTheTip also flakes on exact-SHA run 42888193431 (nil vs Optional(1) at line 299) identically to base 6b6052c run 42838952067; passed on aafed83 run 42826766066 and picker snapshot 42883209970 — same class as flake bead bob-cli-jk / existing 7.1.4 note #1

[2026-11-10T20:07:13Z · bob-cli-ji.7.1.4--7] Event Note picker overlay: Command-E/status-menu/Calendar-row entry, capture editor retained, GcalNotePickerTests all passed on exact-SHA run 42888193431 (snapshot e6203cecdb8fca9b86a9fd25cac5cabda74627cd); Athena portable-check 2454 tests 0 failures; Command-E line-motion assertion passed; remaining CaptureAliasTipPanelTests failures (testEditBeforeTheReplyDropsTheTip plus the three waitUntil timeouts) reproduce on base 6b6052c/aafed83 (bob-cli-jk); no leftover --epic-symbol entries

## Dependencies

- **Depends on:** [bob-cli-ji.7.1.2](bob-cli-ji.7.1.2.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.7.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.4.md) | [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.7.1.4--4][1] | Need the full phase description, DECISIONS, notes, and design file after failed macOS CI | 2 |
| read-by | [agent:bob-cli-ji.7.1.4--5][1] | Need phase scope, notes, and current status after Test hang | 1 |
| read-by | [agent:bob-cli-ji.7.1.4--6][1] | Need phase scope, notes, and design after macOS Test failures | 2 |
| read-by | [agent:bob-cli-ji.7.1.5--1][2] | Need how picker phase recorded alias-tip CI failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.4.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.5.md

<!-- sase:referenced-by:end -->
