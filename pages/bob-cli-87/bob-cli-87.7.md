# Bead: bob-cli-87.7 — Waiting-on and Scheduled lanes for tickler-heavy notes

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.7` · **Size:** medium
**Created:** 2026-10-16 07:13:18 EDT · **Closed:** 2026-10-16 16:29:31 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

scheduled-lane: split the Blocked lane into dependency-blocked 'Waiting on' rows and date-blocked compact 'Scheduled' rows grouped by this week, this month, and later.

## Notes

[2026-10-16T20:29:17Z · bob-cli-87.7--1] PROPOSED FOLLOW-UP: just check flakes under parallel load — lib curl_passes_q_as_first_argument ETXTBSY (already tracked as bob-cli-5l; isolated rerun passed) and completion::bash::bash_readline_inserts_what_bob_returned PTY driver exit after SETUP/EQUALS OK (no dedicated bead; isolated rerun passed in 21s). Neither file is in this phase.

[2026-10-16T20:29:31Z · bob-cli-87.7--1] Verified scheduled-lane split: Blocked [?] rows with open deps, #prj_is_blocked, nested tasks, or no future date stay full Waiting-on rows; date-only future scheduled ticklers become compact Scheduled rows grouped This week / This month / Later with sched/priority/moved chips and {.compact}. Masthead counts N scheduled separately from blocked. Goldens updated (bob-area-ticklers, bob-generated-300, bob-prose-project). cargo test --lib note_snapshot:: 141 passed; prj_is_blocked_and_open_deps_stay_waiting_on and scheduled_rows_group_this_week_this_month_and_later passed. just check failed two pre-existing parallel-load flakes (curl_passes_q ETXTBSY = bob-cli-5l; bash_readline PTY); both passed in isolation. No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-87.11](bob-cli-87.11.md) ◐ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.5](bob-cli-87.5.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.7.md) | [bob-cli-87.7](bob-cli-87.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c7367ee`](https://github.com/bobs-org/bob-cli/commit/c7367ee183e5d9b9bbb3a92b9a1657a8592de10f) | feat(snapshot): split blocked tasks into Waiting on and Scheduled lanes | [bob-cli-87.7](bob-cli-87.7.md) | 2026-10-16 16:30:42 EDT |
