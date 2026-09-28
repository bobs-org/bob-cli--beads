# Bead: bob-cli-2c.1 — Parse and atomically apply whole-item Pomodoro starts

[Bead Pages](../README.md) / [bob-cli-2c](README.md) / bob-cli-2c.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2s.md) · **Assignee:** `bob-cli-2c.1` · **Size:** medium
**Created:** 2026-09-28 12:19:13 EDT · **Closed:** 2026-09-28 12:40:31 EDT
**Plan:** [202609/pomodoro\_start\_next\_operator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_start_next_operator.md)

## Description

start_core: add the shared `=`-family lexer, CaptureKind::PomodoroStart, the staged next-future-Pomodoro planner with its guards and error copy, JSON/human output, the shared selection helper, the "start it with `=`" hints, and CLI tests.

## Notes

[2026-09-28T16:40:11Z · bob-cli-2c.1] PROPOSED FOLLOW-UP: capture_pomodoros missing-note test flakes under parallel runs (with_env BOB_DAY_FILE race); quarantine or serialize env-mutating tests

[2026-09-28T16:40:31Z · bob-cli-2c.1] start_core done: =-family lexer + PomodoroStart kind/planner/guards/hints/output; full cargo test green (1029 lib + 511 cli), clippy has only pre-existing warnings, fmt clean

## Dependencies

- **Blocks:** [bob-cli-2c.2](bob-cli-2c.2.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2c.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2c.1/README.md) | [bob-cli-2c.1](bob-cli-2c.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`47a4b59`](https://github.com/bobs-org/bob-cli/commit/47a4b59489a072cebcd3e73c6454063245dbc6df) | feat(capture): parse and atomically apply whole-item Pomodoro starts | [bob-cli-2c.1](bob-cli-2c.1.md) | 2026-09-28 12:41:45 EDT |
