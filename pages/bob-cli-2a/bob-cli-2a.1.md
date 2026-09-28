# Bead: bob-cli-2a.1 — Parse and atomically apply Pomodoro session shifts

[Bead Pages](../README.md) / [bob-cli-2a](README.md) / bob-cli-2a.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2k.md) · **Assignee:** `bob-cli-2a.1` · **Size:** medium
**Created:** 2026-09-28 10:35:57 EDT · **Closed:** 2026-09-28 10:57:23 EDT
**Plan:** [202609/pomodoro\_shift\_operators.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_shift_operators.md)

## Description

shift_core: add the unified whole-item session-operator lexer (one sign resizes, two signs shift, count defaults to 1), the PomodoroShift capture kind, a staged planner that translates the running session's start and end like `N\o`/`N\O`, additive `pomodoro_shift` capture JSON plus human output, and CLI integration tests.

## Notes

[2026-09-28T14:57:10Z · bob-cli-2a.1] PROPOSED FOLLOW-UP: Fix pre-existing clippy deny (overly_complex_bool_expr at tests/cli.rs:31456, reproduces identically on clean base tree) so just lint goes green

[2026-09-28T14:57:23Z · bob-cli-2a.1] shift_core done: session-operator lexer (one sign resizes, two shift, count defaults 1), PomodoroShift kind + staged shift planner (both endpoints mod 1440, duration unchanged, atomic batches, dry-run), pomodoro_shift JSON + shifted/would-shift human output, bare +,-,++,-- verified, midnight wrap both ways verified, metadata/CRLF/children + stopwatch/range fallbacks verified, 5 new cli shift tests + updated 2 bare-sign tests pass, full cargo test green (967 lib + 503 cli), cargo fmt clean, clippy shows only the pre-existing base-tree deny recorded as follow-up

## Dependencies

- **Blocks:** [bob-cli-2a.2](bob-cli-2a.2.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2a.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2a.1/README.md) | [bob-cli-2a.1](bob-cli-2a.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fe2c0b8`](https://github.com/bobs-org/bob-cli/commit/fe2c0b81d29eb38ef92d8a3824980ae65738733b) | feat(capture): add pomodoro shift operator with staged planner | [bob-cli-2a.1](bob-cli-2a.1.md) | 2026-09-28 11:00:22 EDT |
