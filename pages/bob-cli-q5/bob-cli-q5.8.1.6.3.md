# Bead: bob-cli-q5.8.1.6.3 — Bring the wake HUD and its actions up to the delivery contract

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6](bob-cli-q5.8.1.6.md) / bob-cli-q5.8.1.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.land.md) · **Assignee:** `bob-cli-q5.8.1.6.3` · **Size:** medium
**Created:** 2026-11-26 20:05:50 EST · **Closed:** 2026-11-27 00:21:26 EST
**Plan:** [202611/mac\_snooze\_wake\_notice\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice_repair.md)

## Description

hud-repair: exclude the HUD from capture, render the TODAY link budget and woke time from bob, share task navigation with the record, end the nudge on x/timeout without replays, key HUD state by wake ID, keep hover across updates, and make +15m copy truthful.

## Notes

[2026-11-27T04:54:02Z · bob-cli-q5.8.1.6.3--1] Mac CI Build failure fixed (3 files): AppDelegate agendaEvents now matches .ready/.stale via switch (stale carries String payload); SnoozeNoticeCoordinatorTests stale snapshot now .stale("refresh failed"); SnoozeWakePresenceSource CGDisplayIsAsleep boolean_t converted with != 0. Portable: 2923 tests 0 failures. macOS run 45940646536 showed AppDelegate errors gone, only PresenceSource left (now fixed). Run 45941459240 reached Test step with Build green, but was cancelled by my 540s timeout SIGTERM cleanup; full gate restaged as monitor kj25z8.

[2026-11-27T05:21:09Z · bob-cli-q5.8.1.6.3--1] PROPOSED FOLLOW-UP: testSixtyMinuteBeaconExpiryClears fails on macOS CI because bob-day-authority (phase 6.2, effectiveToday = lastListDate ?? todayProvider) pins the day to fake-bob 2026-11-26 while the test rolls only the local clock; harness cannot simulate a bob-confirmed new day (fake-bob date is a static env var). Natural owner is in-progress bead bob-cli-q5.8.1.6.4 (record lifecycle).

[2026-11-27T05:21:17Z · bob-cli-q5.8.1.6.3--1] macOS gate evidence: Build green on snapshot 750a3ef0 (run 45943032492, includes AppDelegate stale-switch fix, PresenceSource != 0 fix, stale("refresh failed") test fix). Lint green. Test: 1 failing case testSixtyMinuteBeaconExpiryClears (assertions at SnoozeNoticeCoordinatorTests.swift:817-819), recorded as follow-up above; all other suites green. Portable: just portable-check 2923 tests, 0 failures.

[2026-11-27T05:21:26Z · bob-cli-q5.8.1.6.3--1] HUD delivery contract done: capture exclusion, TODAY budget + woke time, shared block-ID navigation, wake-ID-keyed state, truthful +15m copy. Verified: just portable-check 2923 tests 0 failures; macOS run 45943032492 Lint+Build green, all Test suites green except testSixtyMinuteBeaconExpiryClears (bob-day-authority vs local-clock-roll, owned by 6.4, filed as follow-up). No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-q5.8.1.6.2](bob-cli-q5.8.1.6.2.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.8.1.6.4](bob-cli-q5.8.1.6.4.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.3.md) | [bob-cli-q5.8.1.6.3](bob-cli-q5.8.1.6.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.6.3--1][1] | Need full notes and design for remaining fix | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.3.md

<!-- sase:referenced-by:end -->
