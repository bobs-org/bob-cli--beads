# Bead: bob-cli-4i.2 — Lex, claim, and parse whole-item \`!note:block-id\`

[Bead Pages](../README.md) / [bob-cli-4i](README.md) / bob-cli-4i.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5a](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5a.md) · **Assignee:** `bob-cli-4i.2` · **Size:** medium
**Created:** 2026-10-05 15:13:24 EDT · **Closed:** 2026-10-05 15:36:49 EDT
**Plan:** [202610/bang\_task\_complete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete.md)

## Description

grammar: in bob-cli, generalize the `&` note-locator lexer and `replacement_for` over a sigil. Claim whole-item `!` tokens in execution and editor parsing. Add `CaptureKind::TaskComplete`, capture-parse mode/need `task_complete`, `task_complete_*` spans, the per-item `task_complete` object, the `invalid_task_complete` diagnostic, and teaching refusals for queries and padded items. Execution of a complete token returns a temporary refusal until `execute` lands. Grammar docs.

## Notes

[2026-10-05T19:36:20Z · bob-cli-4i.2] PROPOSED FOLLOW-UP: just test failure native::completion::kinds::tests::every_value_arg_has_a_decision (highlights create:audio lacks a kinds decision) reproduces identically on the clean base tree; needs its own bead

[2026-10-05T19:36:26Z · bob-cli-4i.2] PROPOSED FOLLOW-UP: just lint deny clippy::overly_complex_bool_expr in tests/cli/capture/pomodoro_name.rs:808 (tautological || true); file untouched by this phase, pre-existing

[2026-10-05T19:36:49Z · bob-cli-4i.2] Grammar done and verified: shared !/& sigil lexer (scan_bang_token), claim_bang_item predicate, CaptureKind::TaskComplete, execution claim with picker/invalid teaching refusals (exit 2, no inbox), temporary planner refusal, EditorMode/Need/SpanKind task_complete trio, per-item task_complete JSON object, docs/capture.md section. Verified: just fmt clean, 270 capture_language lib tests + 464 capture CLI tests (incl. 7 new task_complete_parse) green, & suite unchanged. just test/lint failures are pre-existing on clean base (recorded as PROPOSED FOLLOW-UP). No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-4i.3](bob-cli-4i.3.md) ✓ · ⧖ 2026-10-05
- **Blocks:** [bob-cli-4i.4](bob-cli-4i.4.md) ✓ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4i.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4i.2/README.md) | [bob-cli-4i.2](bob-cli-4i.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1b6f8bc`](https://github.com/bobs-org/bob-cli/commit/1b6f8bc4396c283e0bf66d95fc504e871bc52d3f) | feat(capture): implement whole-item !note:block-id grammar | [bob-cli-4i.2](bob-cli-4i.2.md) | 2026-10-05 15:38:40 EDT |
