# Bead: bob-cli-q5.7.1.2 — Render and fold Later today with woken accents

[Bead Pages](../README.md) / [bob-cli-q5.7.1](bob-cli-q5.7.1.md) / bob-cli-q5.7.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.md) · **Assignee:** `bob-cli-q5.7.1.2` · **Size:** medium
**Created:** 2026-11-26 07:49:18 EST · **Closed:** 2026-11-26 09:26:41 EST
**Plan:** [202611/mac\_snoozed\_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snoozed_agenda.md)

## Description

later-today-band: implement the separate presentation, persistent summary and first-to-fold behavior, measured Mac views, separate budget count, and sixty-minute woken accents. Cover empty-ledger, compact, and legacy cases and document the shipped idle agenda behavior.

## Notes

[2026-11-26T13:49:49Z · bob-cli-q5.7.1.2] PROPOSED FOLLOW-UP: CapturePlaceMenuPresentationTests.testEmptyQueryOpensWithOnThisTaskAndRecentGroupsAndNothingSelected expects "3 weeks ago" but gets "4 weeks ago" on 2026-11-26; reproduces identically on clean base tree (c4a30591), so date-dependent pre-existing failure unrelated to Later-today band.

[2026-11-26T14:26:28Z · bob-cli-q5.7.1.2--1] macOS CI 45833533092 (snapshot 359a4b7e82a98f4cf0d1f9fb328f04d87942f01f, base e387187f) red: testPlansMatchRenderedHeight (186 vs 176, 127 vs 117 for agenda-snoozed.json at both widths), testAsleepCountdownAging (in 7h30m vs 3h30m, in 4h01m vs now), plus pre-existing place-menu 4-vs-3-weeks. URL https://github.com/bobs-org/bob-mac-capture/actions/runs/45833533092

[2026-11-26T14:26:32Z · bob-cli-q5.7.1.2--1] Fixed owned failures: FitPlanner render added groupSpacing gaps before the snoozed block, so group+snoozed missed 10pt (planner 176 vs view 186); moved gap accounting after snoozed append. Countdown test mixed absolute wake_at with TimeZone.current now (fails under UTC); now uses isoAt 12:00-04:00/15:29-04:00. Portable swift test: 2823 tests, only pre-existing place-menu failure; SnoozedTests 23/23 pass in EST and UTC.

[2026-11-26T14:26:41Z · bob-cli-q5.7.1.2--1] Fixed 2 owned macOS CI failures (planner 10pt snoozed gap, UTC countdown); portable 2823 tests with only pre-existing place-menu 4-vs-3-weeks failure; macOS height fix needs next CI run but logic matches view blocks

## Dependencies

- **Depends on:** [bob-cli-q5.7.1.1](bob-cli-q5.7.1.1.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.7.1.3](bob-cli-q5.7.1.3.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.1.2.md) | [bob-cli-q5.7.1.2](bob-cli-q5.7.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.7.1.2--1][1] | Need phase scope and design for Later-today band CI failure triage | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.1.2.md

<!-- sase:referenced-by:end -->
