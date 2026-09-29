# Bead: bob-cli-2o.4 — bob-cli: capture plan-budget warnings, strict mode, and implicit destination

[Bead Pages](../README.md) / [bob-cli-2o](README.md) / bob-cli-2o.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.4` · **Size:** medium
**Created:** 2026-09-29 18:09:56 EDT · **Closed:** 2026-09-29 19:29:09 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

capture-budget: `bob capture` reports before/after `plan_budget` when a batch changes today's ledger, warns only when it grows past a cap, refuses new non-start themes past the cap in strict mode, reports where a Task Link lands (`role`: current/next_up/named/created), and marks capture-complete create rows with the resulting theme count.

## Notes

[2026-09-29T23:28:59Z · bob-cli-2o.4] PROPOSED FOLLOW-UP: clippy deny(clippy::overly_complex_bool_expr) fails in tests/cli/capture/pomodoro_name.rs:808 on the clean base tree (verified via git stash); unrelated to capture-budget, blocks just lint

[2026-09-29T23:29:09Z · bob-cli-2o.4] capture-budget done: plan_budget before/after reporting with cap warnings, strict-mode atomic refusal (code plan_theme_cap_exceeded, starts never refused), destination roles on all endpoints, pomodoro_task destination/name/creates reporting, capture-complete plan_themes_after/cap rows; docs+help updated. Verified: cargo fmt clean, cargo test all green (1219 lib + 565 cli incl. 12 new plan_budget tests), no epic-symbol leftovers; one pre-existing clippy error on clean base recorded as follow-up

## Dependencies

- **Depends on:** [bob-cli-2o.1](bob-cli-2o.1.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.11](bob-cli-2o.11.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.5](bob-cli-2o.5.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.4/README.md) | [bob-cli-2o.4](bob-cli-2o.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`35b96b3`](https://github.com/bobs-org/bob-cli/commit/35b96b3d734e1d21b42905312233e54afbcfc482) | feat(capture): plan-budget warnings, strict mode, and destination roles | [bob-cli-2o.4](bob-cli-2o.4.md) | 2026-09-29 19:33:21 EDT |
