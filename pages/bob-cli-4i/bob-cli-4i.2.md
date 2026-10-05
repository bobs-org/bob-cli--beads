# Bead: bob-cli-4i.2 — Lex, claim, and parse whole-item \`!note:block-id\`

[Bead Pages](../README.md) / [bob-cli-4i](README.md) / bob-cli-4i.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5a](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5a.md) · **Assignee:** `bob-cli-4i.2` · **Size:** medium
**Created:** 2026-10-05 15:13:24 EDT
**Plan:** [202610/bang\_task\_complete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete.md)

## Description

grammar: in bob-cli, generalize the `&` note-locator lexer and `replacement_for` over a sigil. Claim whole-item `!` tokens in execution and editor parsing. Add `CaptureKind::TaskComplete`, capture-parse mode/need `task_complete`, `task_complete_*` spans, the per-item `task_complete` object, the `invalid_task_complete` diagnostic, and teaching refusals for queries and padded items. Execution of a complete token returns a temporary refusal until `execute` lands. Grammar docs.

## Dependencies

- **Blocks:** [bob-cli-4i.3](bob-cli-4i.3.md) ◐ · ⧖ 2026-10-05
- **Blocks:** [bob-cli-4i.4](bob-cli-4i.4.md) ◐ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4i.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4i.2/README.md) | [bob-cli-4i.2](bob-cli-4i.2.md) | 0 |
