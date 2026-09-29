# Bead: bob-cli-2k.3 — Wire the selection into all close forms, JSON, and human output

[Bead Pages](../README.md) / [bob-cli-2k](README.md) / bob-cli-2k.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.34](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.34.md) · **Assignee:** `bob-cli-2k.3` · **Size:** medium
**Created:** 2026-09-29 13:45:03 EDT
**Plan:** [202609/close\_task\_selection.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_task_selection.md)

## Description

selection-capture: pass the parsed selection into the planner for whole-item,
link, and new-task closes, and remove the temporary refusal. Emit
`in_progress`, `complete`, `task_links`, and `tasks[].index` in the
`pomodoro_close` JSON. Print a numbered index column in human output, and fix the
`carries 1 links` plural. Pin all of it with CLI integration tests on the worked
example, including batches, link forms, dry-run parity, and every diagnostic.

## Dependencies

- **Depends on:** [bob-cli-2k.1](bob-cli-2k.1.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2k.2](bob-cli-2k.2.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2k.4](bob-cli-2k.4.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2k.5](bob-cli-2k.5.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2k.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2k.3/README.md) | [bob-cli-2k.3](bob-cli-2k.3.md) | 0 |
