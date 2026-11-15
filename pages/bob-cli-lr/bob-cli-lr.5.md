# Bead: bob-cli-lr.5 — Decision record, setup guide, and the Birthdays config row

[Bead Pages](../README.md) / [bob-cli-lr](README.md) / bob-cli-lr.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4q.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4q.linker.w1.md) · **Assignee:** `bob-cli-lr.5` · **Size:** small
**Created:** 2026-11-15 12:24:27 EST · **Closed:** 2026-11-15 15:06:07 EST
**Plan:** [202611/gcal\_calendar\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_calendar_marks.md)

## Description

enable-birthdays: write the calendar-mark decision record, add the add-another-calendar step to the setup guide, enable the Birthdays calendar by id with its mark in the chezmoi bob config, and record follow-ups.

## Notes

[2026-11-15T20:04:03Z · bob-cli-lr.5] PROPOSED FOLLOW-UP: Cross-calendar iCalUID dedupe — research and implement deduplication where the same event appears in more than one configured calendar.

[2026-11-15T20:04:21Z · bob-cli-lr.5] PROPOSED FOLLOW-UP: Contacts-birthday layer — consider an opt-in that treats eventType: birthday as context rows.

[2026-11-15T20:04:43Z · bob-cli-lr.5] PROPOSED FOLLOW-UP: Calendar stamp legend — revisit when stamp parsers support trailing segments.

[2026-11-15T20:05:01Z · bob-cli-lr.5] PROPOSED FOLLOW-UP: Per-calendar row policy — define policy before enabling timed-event calendars such as Time Blocks.

[2026-11-15T20:05:16Z · bob-cli-lr.5] PROPOSED FOLLOW-UP: docs-check baseline — docs/reference/configuration.md exceeds its reference word budget by 9 words; this file is unchanged in this phase.

[2026-11-15T20:06:07Z · bob-cli-lr.5] Updated the Google Calendar setup guide with the by-ID unique-mark Birthdays example and dry-run step; enabled the Birthdays ID with 🎂 in the managed Bob config. Recorded four planned follow-ups plus the unchanged docs reference word-budget failure. git diff --check passed in both repos; just docs-check is blocked only by docs/reference/configuration.md being 9 words over budget. Reviewer decision mark_decision_record=no honored; epic-symbols had no leftovers.

## Dependencies

- **Depends on:** [bob-cli-lr.3](bob-cli-lr.3.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-lr.4](bob-cli-lr.4.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-lr.6](bob-cli-lr.6.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lr.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lr.5/README.md) | [bob-cli-lr.5](bob-cli-lr.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d794e0b`](https://github.com/bobs-org/bob-cli/commit/d794e0ba262d32da6b8503f88ad8bcbc2ebc79a5) | docs(gcal): document marked calendar setup | [bob-cli-lr.5](bob-cli-lr.5.md) | 2026-11-15 15:09:05 EST |
| chezmoi | [`chezmoi@88bbec9`](https://github.com/bbugyi200/dotfiles/commit/88bbec95181c09fd4dbe9ce9c9eac5a20b0094ca) | feat(config): enable Birthdays calendar mark | [bob-cli-lr.5](bob-cli-lr.5.md) | 2026-11-15 15:10:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lr.5][1] | Confirm follow-up notes are recorded and the phase is ready to close | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lr.5/README.md

<!-- sase:referenced-by:end -->
