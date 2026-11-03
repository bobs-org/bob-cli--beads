# Bead: bob-cli-gl.2 — Move-bullet lexer, parsers, and capture-parse

[Bead Pages](../README.md) / [bob-cli-gl](README.md) / bob-cli-gl.2

**Status:** ○ open · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.35.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.35.linker.w0.md) · **Assignee:** `bob-cli-gl.2` · **Size:** medium
**Created:** 2026-11-03 13:39:31 EST
**Plan:** [202611/capture\_move\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_bullets.md)

## Description

cli-grammar: Add the shared `move_bullet` lexer. Wire it into the execution parser (`item.rs`) and the editor parser (`editor_parse.rs`). Report the new spans, the `project_task_move` need, `sub_bullet_moves`, and every lexical diagnostic, and apply the grammar-revision decision. Execution refuses move bullets until `cli-execution` lands.

## Dependencies

- **Depends on:** [bob-cli-gl.1](bob-cli-gl.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.4](bob-cli-gl.4.md) ◐ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.5](bob-cli-gl.5.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.2/README.md) | [bob-cli-gl.2](bob-cli-gl.2.md) | 0 |
