# Bead: bob-cli-32.1 — Close planner writes Work Log details under typed entries and reports them

[Bead Pages](../README.md) / [bob-cli-32](README.md) / bob-cli-32.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0uj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0uj.md) · **Assignee:** `bob-cli-32.1` · **Size:** small
**Created:** 2026-09-30 21:31:27 EDT · **Closed:** 2026-09-30 21:49:47 EDT
**Plan:** [202609/close\_work\_log\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_work_log_bullets.md)

## Description

engine: give each typed close Work Log entry a `details` list. The planner
inserts the details one level under the entry line, so the unchanged close
nests them under the dated entry in the task's Work Log. Report the details in
`pomodoro_close.log[].details` and `tasks[].typed_work_log_details`, and print
them in human output. Out-of-range errors stop suggesting the retired `\N`
escape.

## Notes

[2026-10-01T01:49:35Z · bob-cli-32.1] PROPOSED FOLLOW-UP: 5 linked_task_tests fail identically on clean base (freshness [fresh:: date] stamp drift from f103979/3cd4d44: close_plan_preserves_crlf, day_file_can_also_be_a_task_note, worked_example_updates_tasks, selection_in_progress_and_complete, typed_entry_lands_as_typed_subset); needs a freshness-bead expectation update

[2026-10-01T01:49:47Z · bob-cli-32.1] Engine done: CloseLogEntry.details model; planner inserts detail lines one level under entries (tab/2-space/4-space-8-child, CRLF, no-final-newline) tagged InsertedDetail so inserted_lines stays entry lines; LogOutOfRange reworded to quote '- N' with no \N advice; write_logs reports aligned typed_work_log_details; JSON adds log[].details + tasks[].typed_work_log_details (both omitted when empty, schema v1 additive); human output prints details 2 spaces under typed entries; format_pomodoro_close shows (+N detail(s)); docs/capture.md field notes updated. Verified: cargo fmt clean, clippy clean, 11 new tests green (selection x3, linked x3, output x4, format x1), updated CLI out-of-range assertion green, full suite 2091 passed with only the 5 pre-existing base freshness-stamp failures (recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Blocks:** [bob-cli-32.2](bob-cli-32.2.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-32.3](bob-cli-32.3.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-32.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-32.1/README.md) | [bob-cli-32.1](bob-cli-32.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`15c6341`](https://github.com/bobs-org/bob-cli/commit/15c63418ddc0558b968694cc53f88f083190db7a) | feat(capture): close planner writes Work Log details under typed entries and reports them | [bob-cli-32.1](bob-cli-32.1.md) | 2026-09-30 21:51:25 EDT |
