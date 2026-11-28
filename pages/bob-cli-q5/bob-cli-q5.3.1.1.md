# Bead: bob-cli-q5.3.1.1 — Parse snooze intents and expose editor spans

[Bead Pages](../README.md) / [bob-cli-q5.3.1](bob-cli-q5.3.1.md) / bob-cli-q5.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.3.md) · **Assignee:** `bob-cli-q5.3.1.1` · **Size:** medium
**Created:** 2026-11-25 19:34:27 EST · **Closed:** 2026-11-25 22:22:46 EST
**Plan:** [202611/capture\_snooze\_token.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_snooze_token.md)

## Description

grammar: add the shared terminal z:<when> intent, existing-task exception and snooze-drop spelling, editor spans and diagnostics, and parser tests; guard execution until the mutation phase consumes the intent.

## Notes

[2026-11-26T03:22:09Z · bob-cli-q5.3.1.1] PROPOSED FOLLOW-UP: clippy gate fails on clean base at tests/cli/capture/complete_block_id.rs:292 (manual_contains: ids.iter().any(|id| *id == "dup")); untouched by this phase, reproduces identically on the untouched tree

[2026-11-26T03:22:17Z · bob-cli-q5.3.1.1] PROPOSED FOLLOW-UP: 15 capture CLI tests fail identically on the clean base tree (inbox_route x2, note_pull x3, project_note x3, project_note_offer x6, task_theme_writes x1); verified via stash + full capture:: suite on untouched HEAD

[2026-11-26T03:22:22Z · bob-cli-q5.3.1.1] PROPOSED FOLLOW-UP: lib test wispr_summary_renders_one_or_two_pages_with_stable_words fails identically on the clean base tree; september_shaped_vault_finishes_fast is a load-sensitive timing test that passes in isolation with this phase applied

[2026-11-26T03:22:46Z · bob-cli-q5.3.1.1] Grammar phase done and verified. New module capture_language/snooze.rs: lowercase terminal z:<when> lexing (SnoozeIntent { raw, span, drop }), narrow @route:id! drop claim before target validation, shared conflict/teaching messages. TerminalMarkers.snooze and ParsedCaptureText.snooze ride extraction (markers.rs, target_runs crossing-runs incl. Schedule/Priority/Snooze masking, AggregateMarkers with duplicate refusal); multi-target runs refuse; SpanKind::Snooze spans plus incomplete_snooze/invalid_snooze diagnostics keep strict/editor messages byte-identical (bare z, s:/priority/start/close/session/drop conflicts, existing-children, unsupported kinds, drop-vs-toggle). Drop pre-pass (strict item.rs + editor masked view) yields PomodoroLink+drop; caret ^route:id alias shares the exception. Guard at top of plan_capture_item (capture/plan.rs) refuses every recognized intent with snooze_not_yet_executable_error; nothing writes. GRAMMAR_REVISION 31->32 with test assertions updated (docs prose still says 31; completion_docs owns docs-gen/check). FOR MUTATION: consume ParsedCaptureText.snooze — existing-add = PomodoroLink + body empty + snooze.add (route/block set); drop = PomodoroLink + body empty + snooze.drop; new-task = Task/TaskWithBlockId/bare-Pomodoro + body + snooze.add; remove the plan.rs guard only when every accepted intent reaches a planner branch. Verified: 939 lib capture_language tests incl. 8 new snooze tests + snooze.rs unit tests; 5 new CLI tests/cli/capture/parse_snooze.rs; 2066 capture:: CLI pass with only the 15 pre-existing base failures; fmt clean; clippy gate clean for touched files (one pre-existing failure in untouched complete_block_id.rs). Pre-existing failures recorded as PROPOSED FOLLOW-UP bead notes.

## Dependencies

- **Blocks:** [bob-cli-q5.3.1.2](bob-cli-q5.3.1.2.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.1/README.md) | [bob-cli-q5.3.1.1](bob-cli-q5.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1b38663`](https://github.com/bobs-org/bob-cli/commit/1b386638ff031506bb1058853af17b9cab398281) | feat(capture): add snooze z:\<when\> grammar with drop claims | [bob-cli-q5.3.1.1](bob-cli-q5.3.1.1.md) | 2026-11-25 22:59:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.3.1.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-q5.3.1.2][2] | Need grammar intent fields and execution guard handoff | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.2/README.md

<!-- sase:referenced-by:end -->
