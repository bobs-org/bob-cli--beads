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

[2026-11-27T05:45:38Z · bob-cli-q5.8.1.6.3--2] macOS gate rerun 45945499688 (snapshot 54883c671f2ec25d7fb7ff3f57e7b5d94c6d7f8f): Lint green, Build green, Test red with the single known testSixtyMinuteBeaconExpiryClears failure (SnoozeNoticeCoordinatorTests.swift:817-819). Same bob-day-authority mechanism as run 45943032492: effectiveToday stays pinned to fake-bob 2026-11-26 via lastListDate, so rolling clock.today to 2026-11-27 triggers no purge. Out of scope for hud-repair; owned by in-progress bob-cli-q5.8.1.6.4 (record lifecycle). No code changed this turn; bead stays closed.

## Dependencies

- **Depends on:** [bob-cli-q5.8.1.6.2](bob-cli-q5.8.1.6.2.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.8.1.6.4](bob-cli-q5.8.1.6.4.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.3.md) | [bob-cli-q5.8.1.6.3](bob-cli-q5.8.1.6.3.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@6f959f2`](https://github.com/bobs-org/bob-mac-capture/commit/6f959f2d7a3447a69f72c2b7616561404d8fa32c) | fix(snooze): bring wake HUD up to delivery contract | [bob-cli-q5.8.1.6.3](bob-cli-q5.8.1.6.3.md) | 2026-11-26 23:20:17 EST |
| bob-mac-capture | [`bob-mac-capture@d302e01`](https://github.com/bobs-org/bob-mac-capture/commit/d302e01fdd4b36e414bebc0f52da5122048e7b9b) | fix(snooze): repair macOS CI build for wake HUD delivery | [bob-cli-q5.8.1.6.3](bob-cli-q5.8.1.6.3.md) | 2026-11-27 00:22:08 EST |
| bob-mac-capture | [`bob-mac-capture@586d9cc`](https://github.com/bobs-org/bob-mac-capture/commit/586d9ccbe16353ef6cdd16dadf5dbc7d9817eaf6) | fix(snooze): clear beacon on bob-confirmed day boundary in test | [bob-cli-q5.8.1.6.3](bob-cli-q5.8.1.6.3.md) | 2026-11-27 00:50:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.6.3--1][1] | Need full notes and design for remaining fix | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.3.md

<!-- sase:referenced-by:end -->
