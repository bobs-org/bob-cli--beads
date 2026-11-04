# Bead: bob-cli-h0.2 — Lexer arm, parsers, capture-parse spans, continuation key, grammar bump

[Bead Pages](../README.md) / [bob-cli-h0](README.md) / bob-cli-h0.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.37.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.37.linker.w0.md) · **Assignee:** `bob-cli-h0.2` · **Size:** medium
**Created:** 2026-11-04 08:50:23 EST · **Closed:** 2026-11-04 10:19:11 EST
**Plan:** [202611/move\_choice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/move_choice.md)

## Description

cli-grammar: claim `- ^^` in the shared move lexer with its teaching errors, report it from capture-parse, advertise `^` as a continuation key on the lone `- ^` picker, bump the grammar, and refuse `^^` in bob capture until cli-report.

## Notes

[2026-11-04T15:18:39Z · bob-cli-h0.2] PROPOSED FOLLOW-UP: just docs-gen and just docs-check fail on generated drift for sase/memory/glossary/task-merge.md missing front matter; reproduced on clean base and already owned by bob-cli-go.13 (see bob-cli-h0.1 note #1); this phase leaves memory untouched.

[2026-11-04T15:19:11Z · bob-cli-h0.2] cli-grammar done: lexer Choice arm with teaching errors, parsers with draft-wide duplicate, capture-parse spans/JSON/human (grammar 11), continuation key on lone - ^, interim move_choice_unavailable. Verified cargo fmt, clippy, lib 4947 passed, cli 3074 passed (incl 5 new unit + 3 new integration). docs lint passes; docs-gen drift pre-existing task-merge front matter owned by go.13. epic-symbols none.

## Dependencies

- **Depends on:** [bob-cli-h0.1](bob-cli-h0.1.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h0.4](bob-cli-h0.4.md) ◐ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h0.6](bob-cli-h0.6.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-h0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.2/README.md) | [bob-cli-h0.2](bob-cli-h0.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bfbf482`](https://github.com/bobs-org/bob-cli/commit/bfbf482fd696fbb406fb33a0fb4231a8112dd83d) | feat(capture)!: claim - ^^ move-choice marker with teaching errors | [bob-cli-h0.2](bob-cli-h0.2.md) | 2026-11-04 10:21:20 EST |
