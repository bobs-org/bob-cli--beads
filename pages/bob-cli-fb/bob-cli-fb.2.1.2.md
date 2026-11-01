# Bead: bob-cli-fb.2.1.2 — Connect capture planning and the JSON contract

[Bead Pages](../README.md) / [bob-cli-fb.2.1](bob-cli-fb.2.1.md) / bob-cli-fb.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.md) · **Assignee:** `bob-cli-fb.2.1.2` · **Size:** medium
**Created:** 2026-11-01 13:00:27 EST · **Closed:** 2026-11-01 15:34:28 EST
**Plan:** [202611/leaf\_keep\_moving\_rust.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/leaf_keep_moving_rust.md)

## Description

capture: wire both capture close paths, dependency completeness, config, separate JSON arrays, selection and refusal, group folds, task-block roles, and Pomodoro diff reasons; add focused CLI tests.

## Notes

[2026-11-01T20:34:18Z · bob-cli-fb.2.1.2] PROPOSED FOLLOW-UP: Fix pre-existing clippy filter_map_bool_then denial in src/native/capture_pomodoro_agenda.rs:1086 (touched by no phase-2.1.2 edit; just lint fails identically on clean tree)

[2026-11-01T20:34:28Z · bob-cli-fb.2.1.2] Capture phase done: plan.keep_moving wired with KM31 unavailable-safe rows, separate keep_moving arrays on task_complete/pomodoro_close/nested summaries, shared numbering/selection/refusal/counts, keep-moving folds keyed by group, KeepMoving task-block role and pomodoro reason, day_file/continuation for picks; 13 new CLI keep-moving tests pass plus SO/PP/SL and 155 engine + 14 config tests; just lint fails only on pre-existing agenda filter_map_bool_then (untouched file)

## Dependencies

- **Depends on:** [bob-cli-fb.2.1.1](bob-cli-fb.2.1.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fb.2.1.3](bob-cli-fb.2.1.3.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fb.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.2.1.2/README.md) | [bob-cli-fb.2.1.2](bob-cli-fb.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ab32d58`](https://github.com/bobs-org/bob-cli/commit/ab32d58aac5a838edf405eb0a34dfb1955041d1f) | feat(capture): connect keep-moving planning and JSON contract | [bob-cli-fb.2.1.2](bob-cli-fb.2.1.2.md) | 2026-11-01 15:35:44 EST |
