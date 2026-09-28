# Bead: bob-cli-29.3 — =x grammar, atomic capture transaction, and outputs

[Bead Pages](../README.md) / [bob-cli-29](README.md) / bob-cli-29.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2i](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2i.md) · **Assignee:** `bob-cli-29.3` · **Size:** medium
**Created:** 2026-09-28 06:24:49 EDT
**Plan:** [202609/capture\_pomodoro\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_pomodoro_close.md)

## Description

close-capture: recognize whole-item `=x` and the `=x` suffix on solo `@`/`^` links and body-bearing `:` captures, together with their near-miss and conflict errors. Wire the close through CaptureBatchPlanner, including the link-into-running step. Emit the `pomodoro_close` kind and object plus human output, point the start guards at `=x`, and add integration tests.

## Dependencies

- **Depends on:** [bob-cli-29.2](bob-cli-29.2.md) ◐ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-29.4](bob-cli-29.4.md) ◐ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-29.5](bob-cli-29.5.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-29.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-29.3/README.md) | [bob-cli-29.3](bob-cli-29.3.md) | 0 |
