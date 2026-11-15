# Bead: bob-cli-lr.3 — Freeze rows from calendars that left the config

[Bead Pages](../README.md) / [bob-cli-lr](README.md) / bob-cli-lr.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4q.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4q.linker.w1.md) · **Assignee:** `bob-cli-lr.3` · **Size:** small
**Created:** 2026-11-15 12:24:27 EST · **Closed:** 2026-11-15 14:25:45 EST
**Plan:** [202611/gcal\_calendar\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_calendar_marks.md)

## Description

deconfigured-freeze: journaled rows whose calendar is no longer configured are left alone, reported once, and never looked up, which removes the false Moved and Deleted verdicts; re-adding the calendar resumes the same identities.

## Notes

[2026-11-15T18:45:34Z · bob-cli-lr.3] PROPOSED FOLLOW-UP: docs-check fails on docs/reference/configuration.md word budget (6009/6000) on the clean tree; this phase did not edit that file.

[2026-11-15T19:25:45Z · bob-cli-lr.3--1] Verified: deconfigured calendars freeze journaled rows (LeftAlone calendar no longer synced, no gog lookup). Test deconfigured_calendar_rows_freeze_without_lookup covers timed + day-2 all-day freeze, once-only notice, resume without duplicates. just check / sase tool run check 282aa1044426e67f914dc116b736660e succeeded. No leftover --epic-symbol entries. PROPOSED FOLLOW-UP already recorded for docs-check configuration.md word budget on the clean tree.

## Dependencies

- **Depends on:** [bob-cli-lr.1](bob-cli-lr.1.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-lr.5](bob-cli-lr.5.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lr.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lr.3.md) | [bob-cli-lr.3](bob-cli-lr.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ee6d650`](https://github.com/bobs-org/bob-cli/commit/ee6d650376d0fb413e789d704f22e915e608f89d) | feat(gcal): freeze rows from calendars that left the config | [bob-cli-lr.3](bob-cli-lr.3.md) | 2026-11-15 14:46:22 EST |
