# Bead: bob-cli-lr.1 — Calendar marks in config, a resolved calendar set, and per-calendar fake gog

[Bead Pages](../README.md) / [bob-cli-lr](README.md) / bob-cli-lr.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4q.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4q.linker.w1.md) · **Assignee:** `bob-cli-lr.1` · **Size:** medium
**Created:** 2026-11-15 12:24:27 EST · **Closed:** 2026-11-15 13:20:03 EST
**Plan:** [202611/gcal\_calendar\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_calendar_marks.md)

## Description

calendar-config: add the required, validated `mark` key to `gcal.calendars`, check the calendar set against the account's calendar list before any fetch (missing calendars, primary/email aliases, unmarked non-primary), carry a resolved calendar identity on every snapshot event, and teach the test fake gog to serve events and lookups per calendar.

## Notes

[2026-11-15T18:19:37Z · bob-cli-lr.1] PROPOSED FOLLOW-UP: just check --test cli complete_themes shell tests flake under suite load (configured_shell_describes_never_used_and_unconfigured_create, theme_recent_shell_description_and_quoted_replacement); pass isolated; already tracked by bob-cli-g8

[2026-11-15T18:20:03Z · bob-cli-lr.1] Required unique mark on non-primary gcal.calendars; FetchContext/note resolve the Google set before any events fetch (calendar_not_found, calendar_duplicate, unmarked non-primary); SnapshotEvent carries SyncedCalendar; fake gog serves per-calendar events/lookups. Verified: cargo fmt, clippy gates, config unit tests, gcal_sync/list/note_cli integration tests including missing/duplicate/unmarked/second-fetch-fail/shared-id; just check otherwise green. Two cli complete_themes shell tests failed under suite load and passed isolated (bob-cli-g8).

## Dependencies

- **Blocks:** [bob-cli-lr.2](bob-cli-lr.2.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-lr.3](bob-cli-lr.3.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lr.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lr.1/README.md) | [bob-cli-lr.1](bob-cli-lr.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2759a4e`](https://github.com/bobs-org/bob-cli/commit/2759a4e7c687ce36c859ceb20f790b682204494b) | feat(gcal)!: require unique marks on non-primary calendars | [bob-cli-lr.1](bob-cli-lr.1.md) | 2026-11-15 13:22:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lr.1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lr.1/README.md

<!-- sase:referenced-by:end -->
