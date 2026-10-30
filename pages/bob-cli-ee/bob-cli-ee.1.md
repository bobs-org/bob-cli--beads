# Bead: bob-cli-ee.1 — bob-cli t:\<type\> grammar, parse spans, and new-task typing

[Bead Pages](../README.md) / [bob-cli-ee](README.md) / bob-cli-ee.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b6.md) · **Assignee:** `bob-cli-ee.1` · **Size:** large
**Created:** 2026-10-30 04:22:33 EDT
**Plan:** [202610/capture\_type\_marker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_marker.md)

## Description

grammar: lex `t:<type>` at line edges with one shared lexer, mask it out of the execution, editor, and completion parse paths without moving byte offsets, emit the `task_type` span, need, and diagnostics, type newly captured tasks (including the named-Pomodoro agreement rule), refuse non-task items with teaching errors, and document the marker.

## Notes

[2026-10-30T08:32:20Z · bob-cli-ee.1] PROPOSED FOLLOW-UP: Skipped type-marker decision memory — the final epic decision memory_record=no forbids creating decisions:type-marker-is-orthogonal; no memory files were edited. The outer land agent can retain this record when triaging the skipped change.

## Dependencies

- **Blocks:** [bob-cli-ee.2](bob-cli-ee.2.md) ◐ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-ee.3](bob-cli-ee.3.md) ◐ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-ee.4](bob-cli-ee.4.md) ◐ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ee.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.md) | [bob-cli-ee.1](bob-cli-ee.1.md) | 0 |
