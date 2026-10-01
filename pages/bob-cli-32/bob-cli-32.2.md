# Bead: bob-cli-32.2 — Parse Work Log bullets under =x, retire the inline tail, and document it

[Bead Pages](../README.md) / [bob-cli-32](README.md) / bob-cli-32.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0uj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0uj.md) · **Assignee:** `bob-cli-32.2` · **Size:** medium
**Created:** 2026-09-30 21:31:28 EDT
**Plan:** [202609/close\_work\_log\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_work_log_bullets.md)

## Description

grammar: replace the inline tail lexer with one shared Work Log bullet lexer
used by `bob capture` and `capture-parse`. It produces index spans, the
dangling-bullet editing state, and diagnostics. Retire the tail with a message
that shows the bullet to write. Revert the tail-only chain splitting, and attach
a chain line's bullets to its `=x`. Silence marker and block-link completion on
bullet lines, then update help, docs/capture.md, and tests.

## Dependencies

- **Depends on:** [bob-cli-32.1](bob-cli-32.1.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-32.3](bob-cli-32.3.md) ◐ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-32.4](bob-cli-32.4.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-32.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-32.2/README.md) | [bob-cli-32.2](bob-cli-32.2.md) | 0 |
