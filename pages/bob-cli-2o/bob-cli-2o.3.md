# Bead: bob-cli-2o.3 — bob-cli: plan budget in task-status-hooks and the tmux segment

[Bead Pages](../README.md) / [bob-cli-2o](README.md) / bob-cli-2o.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.3` · **Size:** small
**Created:** 2026-09-29 18:09:56 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

hooks-tmux: add a read-only `plan_budget` to task-status-hooks JSON and human output, make the multiple-open-timed error name the entries and suggest `=x`, and append the budget meter (reversed when over the cap) to `bob tmux-pomodoro`.

## Notes

[2026-09-29T23:00:18Z · bob-cli-2o.3] PROPOSED FOLLOW-UP: pre-existing clippy deny (overly_complex_bool_expr, `|| true`) at tests/cli/capture/pomodoro_name.rs:808 reproduces on clean base; makes `cargo clippy --all-targets` fail for unrelated phases

## Dependencies

- **Depends on:** [bob-cli-2o.1](bob-cli-2o.1.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.13](bob-cli-2o.13.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.3/README.md) | [bob-cli-2o.3](bob-cli-2o.3.md) | 0 |
