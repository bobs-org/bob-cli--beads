# Bead: bob-cli-2o.3 — bob-cli: plan budget in task-status-hooks and the tmux segment

[Bead Pages](../README.md) / [bob-cli-2o](README.md) / bob-cli-2o.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.3` · **Size:** small
**Created:** 2026-09-29 18:09:56 EDT · **Closed:** 2026-09-29 19:17:38 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

hooks-tmux: add a read-only `plan_budget` to task-status-hooks JSON and human output, make the multiple-open-timed error name the entries and suggest `=x`, and append the budget meter (reversed when over the cap) to `bob tmux-pomodoro`.

## Notes

[2026-09-29T23:00:18Z · bob-cli-2o.3] PROPOSED FOLLOW-UP: pre-existing clippy deny (overly_complex_bool_expr, `|| true`) at tests/cli/capture/pomodoro_name.rs:808 reproduces on clean base; makes `cargo clippy --all-targets` fail for unrelated phases

[2026-09-29T23:17:38Z · bob-cli-2o.3] hooks-tmux done and verified: plan_budget in task-status-hooks JSON+human (null on invalid config/missing section, single stderr warning), multi-timed error names entries with line/range and =x hint, tmux meter with reverse-video over-cap, script fallback budget-less. Verified: cargo build ok, cargo fmt --check ok, full cargo test green (1217 lib + 558 cli incl. 4 tmux and 36 hooks tests), docs+README updated. One pre-existing clippy deny at tests/cli/capture/pomodoro_name.rs:808 fails identically on clean base (recorded as PROPOSED FOLLOW-UP); no epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-2o.1](bob-cli-2o.1.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.13](bob-cli-2o.13.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.3/README.md) | [bob-cli-2o.3](bob-cli-2o.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f481c7a`](https://github.com/bobs-org/bob-cli/commit/f481c7a065f99806018167f6e712de543e5251ad) | feat(hooks-tmux): plan budget in task-status-hooks and the tmux segment | [bob-cli-2o.3](bob-cli-2o.3.md) | 2026-09-29 19:19:10 EDT |
