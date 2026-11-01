# Bead: bob-cli-f6.1 — bob-cli: untracked ledger rows and Event Task event helpers

[Bead Pages](../README.md) / [bob-cli-f6](README.md) / bob-cli-f6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bv](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bv.md) · **Assignee:** `bob-cli-f6.1` · **Size:** medium
**Created:** 2026-11-01 11:24:13 EST · **Closed:** 2026-11-01 12:47:01 EST
**Plan:** [202611/untracked\_calendar\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/untracked_calendar_events.md)

## Description

untracked-ledger: make a timed row without [t::] untracked in every reader and writer, and add the shared Event Task helpers.

## Notes

[2026-11-01T17:19:23Z · bob-cli-f6.1] Verified session_tracking, untracked close/adjust/shift, homes untracked:true + 0-minute parts, stats exclude from minutes/counts with health.homes.untracked_sessions, Event Task helpers, glossary:event-task, just lint, no leftover --epic-symbol entries. just check still pending via prepared monitor.

[2026-11-01T17:47:01Z · bob-cli-f6.1--1] Timed rows without [t::] are untracked in every reader and writer: session_tracking, stats minutes/counts plus health.homes.untracked_sessions, homes untracked:true with 0-minute parts, completed_summary, and bob pomodoro --worked (day_with_worked_pomodoros is 50m tracked-only; GTD/LATE NIGHT span fallback retired). Adjust/shift/close keep untracked rows untracked. Event Task helpers parse #untracked, events_in_note, first_event_start_crossed, and cluster_by_trackedness. glossary:event-task and CLI --worked help/docs match. No leftover --epic-symbol entries. Targeted cli pomodoro --worked test passed; full just check via prepared monitor.

## Dependencies

- **Blocks:** [bob-cli-f6.2](bob-cli-f6.2.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f6.3](bob-cli-f6.3.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f6.5](bob-cli-f6.5.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-f6.1.md) | [bob-cli-f6.1](bob-cli-f6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6d39305`](https://github.com/bobs-org/bob-cli/commit/6d39305a8cc4d39b2c2213c8b9e702cfacb648b4) | feat(pomodoro)!: omit untracked sessions from clocks and counts | [bob-cli-f6.1](bob-cli-f6.1.md) | 2026-11-01 13:19:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f6.1--2][1] | Need the phase scope, design file, notes, and DECISIONS | 1 |
| read-by | [agent:bob-cli-f6.2][2] | Need prior phase implementation for dependency | 1 |
| read-by | [agent:bob-cli-f6.3][3] | see what the predecessor phase landed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-f6.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.3/README.md

<!-- sase:referenced-by:end -->
