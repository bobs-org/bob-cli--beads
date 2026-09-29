# Bead: bob-cli-2k.2 — =x\<N\>!\<M\> grammar, capture-parse contract, and editor states

[Bead Pages](../README.md) / [bob-cli-2k](README.md) / bob-cli-2k.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.34](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.34.md) · **Assignee:** `bob-cli-2k.2` · **Size:** medium
**Created:** 2026-09-29 13:45:03 EDT · **Closed:** 2026-09-29 14:13:41 EDT
**Plan:** [202609/close\_task\_selection.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_task_selection.md)

## Description

selection-grammar: lex `=x[<N>][!<M>]` once and share the lexer between the
whole-item close and the `@`/`^`/body-bearing `=x` suffix, in both the execution
and editor parsers. Report the additive `in_progress`/`complete` spec, new span
kinds, precise `invalid_pomodoro_close` diagnostics, and an incomplete
`pomodoro_close_task` need for a dangling `,`/`!`. Update capture-complete,
capture-rewrite, and capture-parse help. The executor refuses a selection-bearing
close until selection-capture wires it in.

## Notes

[2026-09-29T18:13:20Z · bob-cli-2k.2] PROPOSED FOLLOW-UP: cargo clippy --all-targets --all-features fails identically on the clean base tree (23 pre-existing warnings, e.g. needless returns in tokens.rs and a boolean-logic bug in tests/cli/capture/pomodoro_name.rs:808); no new warnings from selection-grammar

[2026-09-29T18:13:41Z · bob-cli-2k.2] selection-grammar done: shared lex_close_selection in capture_language/close_selection.rs drives whole-item =x and @/^ suffixes in execution + editor; PomodoroCloseSpec carries sorted in_progress/complete (plain =x: null/[]); new pomodoro_close_in_progress/complete spans and pomodoro_close_task need; precise invalid_pomodoro_close ranges for every lexical row; dangling ,/! reports incomplete with partial spec + placeholder; executor refuses selection-bearing closes; capture-parse/complete/rewrite help updated. Verified: cargo fmt clean, full cargo test green (1147 lib + 523 cli incl. new selection protocol/unit tests), clippy shows zero new warnings vs base (base fails identically; filed as PROPOSED FOLLOW-UP). epic-symbols: none.

## Dependencies

- **Blocks:** [bob-cli-2k.3](bob-cli-2k.3.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2k.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2k.2/README.md) | [bob-cli-2k.2](bob-cli-2k.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1838779`](https://github.com/bobs-org/bob-cli/commit/1838779284b63937735b988a4f09e57d7ae50325) | feat(capture): add pomodoro close selection grammar | [bob-cli-2k.2](bob-cli-2k.2.md) | 2026-09-29 14:15:59 EDT |
