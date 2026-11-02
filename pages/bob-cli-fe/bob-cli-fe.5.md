# Bead: bob-cli-fe.5 — x narrows the closed name and sheds the carried name (bob-cli)

[Bead Pages](../README.md) / [bob-cli-fe](README.md) / bob-cli-fe.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c4.md) · **Assignee:** `bob-cli-fe.5` · **Size:** medium
**Created:** 2026-11-01 16:00:43 EST · **Closed:** 2026-11-01 19:14:35 EST
**Plan:** [202611/merged\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merged_pomodoros.md)

## Description

capture-close-names: apply R6 in the shared close planner using pre-close task types; split the closed-name and continuation-name roles; add the closed_name and shed output.

## Notes

[2026-11-02T00:14:28Z · bob-cli-fe.5] PROPOSED FOLLOW-UP: five CLI tests fail on the clean master tree (reproduced with my changes stashed) — tests/cli capture::pomodoro_link::capture_named_pomodoro_updates_both_notes_and_skips_current, ::capture_named_pomodoro_dry_run_and_failures_leave_notes_untouched, capture::project_note::capture_project_note_task_links_write_the_worked_example, capture::project_note_offer::offer_named_pomodoro_is_created_only_when_a_pick_lands_there, capture::task_theme_writes::named_capture_writes_a_type_without_a_shown_suggestion; they still expect a named link to retype the task ([type::] written) after routing-core made land default to merge — likely owned by bob-cli-fe.2 capture-link-merge

[2026-11-02T00:14:35Z · bob-cli-fe.5] R6 applied in the shared close planner: pure close_names (names.rs) feeds merged::narrow_closed/shed from pre-close link types + outcomes; closed entry line renamed, created placeholder uses shed name; ClosingContext.closed_name split (capture locates closed entry by narrowed closed_name, successors name/reuse continuation via continuation_name); JSON adds pomodoro_close.closed_name and next_pomodoro.shed [ThemeRef]; human output adds 'from X' and 'shed T'; docs/capture.md updated (new 'Close names follow the work', JSON and parity text). Verified: just check fmt+clippy clean; all tests pass incl. new names/ledger/CLI/km11 tests except 5 pre-existing named-link retype CLI failures reproduced on clean base (recorded as PROPOSED FOLLOW-UP). just docs-check passes. No epic-symbols remain.

## Dependencies

- **Depends on:** [bob-cli-fe.1](bob-cli-fe.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.10](bob-cli-fe.10.md) ◐ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.8](bob-cli-fe.8.md) ◐ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.9](bob-cli-fe.9.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fe.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.5/README.md) | [bob-cli-fe.5](bob-cli-fe.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3e21e99`](https://github.com/bobs-org/bob-cli/commit/3e21e990d7c1bd73f14db46f13367b339f5d179b) | feat(capture): narrow the closed Pomodoro name and shed the carried one on x | [bob-cli-fe.5](bob-cli-fe.5.md) | 2026-11-01 19:15:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fb.2.1.land--1][1] | Need fe.5 follow-up for 5 named-link failures | 1 |
| read-by | [agent:bob-cli-fe.5][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.5/README.md

<!-- sase:referenced-by:end -->
