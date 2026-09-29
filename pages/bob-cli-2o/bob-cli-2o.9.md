# Bead: bob-cli-2o.9 — bob-plugins: toggle #now from task lines and Task Links

[Bead Pages](../README.md) / [bob-cli-2o](README.md) / bob-cli-2o.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.9` · **Size:** medium
**Created:** 2026-09-29 18:09:57 EDT · **Closed:** 2026-09-29 19:36:51 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

now-toggle: add a counted "Toggle #now" command (default Alt+N) and a `#now` row in the Ctrl+Shift+P picker. Both work on task lines and Task Link lines, place the tag before the fields, and report the NOW count in the Notice.

## Notes

[2026-09-29T23:36:25Z · bob-cli-2o.9--1] PROPOSED FOLLOW-UP: bob-cli `cargo clippy` (just lint) fails on clean tree at tests/cli/capture/pomodoro_name.rs:808 overly_complex_bool_expr (deny by default) plus unary warning in pomodoro_shift.rs:581; cargo test and cargo fmt pass. Unrelated to now-toggle (bob-cli tree clean, phase touches only bob-plugins).

[2026-09-29T23:36:51Z · bob-cli-2o.9--1] now-toggle done and verified: toggle-now-tag (Alt+N, free chord) + pinned #now picker row in task and link modes; tag placed before trailing fields/^id, whole-token remove, cross-note preimage guards, NOW count Notice via ledger-tools api with over-cap hint. npm test 794/794 pass, npm run validate 6/6, cargo test pass, cargo fmt clean, vault synced at 1.39.0 (main.js identical). bob-cli clippy lint failure at pomodoro_name.rs:808 is pre-existing on clean tree, recorded as follow-up.

## Dependencies

- **Blocks:** [bob-cli-2o.13](bob-cli-2o.13.md) ◐ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.7](bob-cli-2o.7.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.8](bob-cli-2o.8.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2o.9.md) | [bob-cli-2o.9](bob-cli-2o.9.md) | 0 |
