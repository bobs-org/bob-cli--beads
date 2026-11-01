# Bead: bob-cli-f6.7 — bob-mac-capture: Calendar band in the idle agenda

[Bead Pages](../README.md) / [bob-cli-f6](README.md) / bob-cli-f6.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bv](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bv.md) · **Assignee:** `bob-cli-f6.7` · **Size:** medium
**Created:** 2026-11-01 11:24:14 EST · **Closed:** 2026-11-01 15:11:27 EST
**Plan:** [202611/untracked\_calendar\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/untracked_calendar_events.md)

## Description

mac-calendar-band: decode the events block and add the folding Calendar band, rows, header, chips, and Command-J join.

## Notes

[2026-11-01T20:11:27Z · bob-cli-f6.7] Calendar band landed in bob-mac-capture: models decode the events block (events, item event, entry tracked, untracked_count) with .other fallbacks; presentation builds the calendar unit (header, all-day, rail slot, gap, conflict, event rows, earlier/+N chips, oneRow merge, clear row) with MEET time chips; planner splices the band after Now groups with full->compact->oneRow ladder and no hide state; views render all 8 new row kinds with join buttons; Command-J joins the focus event from an empty draft (verified free); store schedules .eventBoundary refresh at refresh_at; docs updated. Verified: portable swift test 1915 pass incl 20 new calendar tests (athena), macOS build + typecheck-tests exit 0, docs-check pass, check-scripts OK (42 tests). macOS XCTest run itself is CI's; lint parity unavailable (bundled formatter v600 reports 2134 warnings on pristine HEAD).

## Dependencies

- **Depends on:** [bob-cli-f6.5](bob-cli-f6.5.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f6.8](bob-cli-f6.8.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f6.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.7/README.md) | [bob-cli-f6.7](bob-cli-f6.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@28293b2`](https://github.com/bobs-org/bob-mac-capture/commit/28293b25350e7a20bdb03604a6c931851692434d) | feat(mac-capture): add the Calendar band to the idle agenda | [bob-cli-f6.7](bob-cli-f6.7.md) | 2026-11-01 15:12:45 EST |
