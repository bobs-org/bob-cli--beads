# Bead: bob-cli-4i.1 — Extract a shared task-completion engine (no new syntax)

[Bead Pages](../README.md) / [bob-cli-4i](README.md) / bob-cli-4i.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5a](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5a.md) · **Assignee:** `bob-cli-4i.1` · **Size:** medium
**Created:** 2026-10-05 15:13:24 EDT · **Closed:** 2026-10-05 15:34:34 EDT
**Plan:** [202610/bang\_task\_complete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete.md)

## Description

engine: in bob-cli, add `src/native/task_complete/`. Extract the =x embedded tree close into a reusable `complete_task_tree`, keeping =x byte-identical. Expose a scoped completed-reference retirement built on reconcile's structural planner, with an opt-in dedupe that avoids the bob-cli-2l duplicate. Add an immediate Blocked-dependent recovery matching Ctrl+Enter, built on reconcile's dependency-state definition. Unit tests only; no user-visible change.

## Notes

[2026-10-05T19:34:12Z · bob-cli-4i.1] PROPOSED FOLLOW-UP: Rust structural planner dedupe path exists behind the opt-in dedupe_into_destination flag (retirement passes true, reconcile passes false); enabling it for reconcile together with the bob-plugins JS fix belongs to bob-cli-2l

[2026-10-05T19:34:16Z · bob-cli-4i.1] PROPOSED FOLLOW-UP: lib test completion::kinds::tests::every_value_arg_has_a_decision fails on missing kinds decision for "highlights create:audio"; reproduces identically on the clean base tree (verified via stash), unrelated to this phase

[2026-10-05T19:34:21Z · bob-cli-4i.1] PROPOSED FOLLOW-UP: just lint is red on clippy deny overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 (|| true); file untouched by this phase, predates it

[2026-10-05T19:34:34Z · bob-cli-4i.1] Engine done: task_complete module (complete_task_tree with CloseLink/Explicit, retire_completed_links with dedupe flag, recover_blocked_dependents, is_recurring_task_line) plus 19 unit tests, all passing; close rewired through engine gate with CloseLink and all existing close tests unchanged; just fmt pass; cargo test green except pre-existing completion kinds failure verified identical on clean base; just lint red only on pre-existing pomodoro_name clippy deny (both recorded as follow-ups)

## Dependencies

- **Blocks:** [bob-cli-4i.4](bob-cli-4i.4.md) ✓ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4i.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4i.1/README.md) | [bob-cli-4i.1](bob-cli-4i.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7c8d854`](https://github.com/bobs-org/bob-cli/commit/7c8d854ec408a5afe9e8c6dd29d8e754fb754a06) | feat(task-complete): extract shared task-completion engine | [bob-cli-4i.1](bob-cli-4i.1.md) | 2026-10-05 15:35:46 EDT |
