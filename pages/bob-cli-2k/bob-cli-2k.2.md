# Bead: bob-cli-2k.2 — =x\<N\>!\<M\> grammar, capture-parse contract, and editor states

[Bead Pages](../README.md) / [bob-cli-2k](README.md) / bob-cli-2k.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.34](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.34.md) · **Assignee:** `bob-cli-2k.2` · **Size:** medium
**Created:** 2026-09-29 13:45:03 EDT
**Plan:** [202609/close\_task\_selection.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_task_selection.md)

## Description

selection-grammar: lex `=x[<N>][!<M>]` once and share the lexer between the
whole-item close and the `@`/`^`/body-bearing `=x` suffix, in both the execution
and editor parsers. Report the additive `in_progress`/`complete` spec, new span
kinds, precise `invalid_pomodoro_close` diagnostics, and an incomplete
`pomodoro_close_task` need for a dangling `,`/`!`. Update capture-complete,
capture-rewrite, and capture-parse help. The executor refuses a selection-bearing
close until selection-capture wires it in.

## Dependencies

- **Blocks:** [bob-cli-2k.3](bob-cli-2k.3.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2k.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2k.2/README.md) | [bob-cli-2k.2](bob-cli-2k.2.md) | 0 |
