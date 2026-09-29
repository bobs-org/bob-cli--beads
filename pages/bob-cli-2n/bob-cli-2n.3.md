# Bead: bob-cli-2n.3 — Render named project tasks and write their Task Links

[Bead Pages](../README.md) / [bob-cli-2n](README.md) / bob-cli-2n.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.35](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.35.md) · **Assignee:** `bob-cli-2n.3` · **Size:** medium
**Created:** 2026-09-29 15:35:25 EDT · **Closed:** 2026-09-29 17:11:55 EDT
**Plan:** [202609/project\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/project_task_links.md)

## Description

task-id-execution: render `^id` onto named tasks (`[*]` for `:` tasks), write one Task Link per `:` task into the selected Pomodoro atomically with the new note, and report `project_note.task_links` in JSON and human output.

## Notes

[2026-09-29T21:11:40Z · bob-cli-2n.3] PROPOSED FOLLOW-UP: clippy overly_complex_bool_expr error at tests/cli/capture/pomodoro_name.rs:808 (pre-existing trailing `|| true` in untouched file, identical on clean base) keeps `cargo clippy --all-targets --all-features` red; simplify that assertion so the gate goes green

[2026-09-29T21:11:55Z · bob-cli-2n.3] task-id-execution done: renderer appends ^id last with [*]/[?] for : tasks and named_tasks; planner writes one Task Link per : task atomically with the note (implicit current/next or named, single create) and reports project_note.task_links always plus day_file/pomodoro_link_placement/pomodoro_name/creates_pomodoro; human output prints linked/under/links lines. Verified: cargo fmt --check clean, full cargo test green (1187 lib + 543 cli incl. 5 new renderer + 4 new CLI tests), epic-symbols empty. Known pre-existing: clippy overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 (recorded as PROPOSED FOLLOW-UP, identical on clean base).

## Dependencies

- **Depends on:** [bob-cli-2n.2](bob-cli-2n.2.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2n.5](bob-cli-2n.5.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2n.6](bob-cli-2n.6.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2n.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2n.3/README.md) | [bob-cli-2n.3](bob-cli-2n.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5f6c761`](https://github.com/bobs-org/bob-cli/commit/5f6c761208a36eea54c6327185e3f419ea105a71) | feat(capture): render named project tasks and write their Task Links | [bob-cli-2n.3](bob-cli-2n.3.md) | 2026-09-29 17:13:21 EDT |
