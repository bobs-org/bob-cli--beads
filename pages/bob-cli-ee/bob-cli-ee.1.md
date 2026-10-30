# Bead: bob-cli-ee.1 — bob-cli t:\<type\> grammar, parse spans, and new-task typing

[Bead Pages](../README.md) / [bob-cli-ee](README.md) / bob-cli-ee.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b6.md) · **Assignee:** `bob-cli-ee.1` · **Size:** large
**Created:** 2026-10-30 04:22:33 EDT · **Closed:** 2026-10-30 09:37:51 EDT
**Plan:** [202610/capture\_type\_marker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_marker.md)

## Previously Closed

> ↺ Closed 2026-10-30T13:35:45Z · done
>
> delegated work landed
>
> Reopened 2026-10-30T13:37:28Z by `sase bead open`

## Description

grammar: lex `t:<type>` at line edges with one shared lexer, mask it out of the execution, editor, and completion parse paths without moving byte offsets, emit the `task_type` span, need, and diagnostics, type newly captured tasks (including the named-Pomodoro agreement rule), refuse non-task items with teaching errors, and document the marker.

## Notes

[2026-10-30T08:32:20Z · bob-cli-ee.1] PROPOSED FOLLOW-UP: Skipped type-marker decision memory — the final epic decision memory_record=no forbids creating decisions:type-marker-is-orthogonal; no memory files were edited. The outer land agent can retain this record when triaging the skipped change.

[2026-10-30T13:37:51Z · bob-cli-ee.1.1.land--1] Verified the grammar phase end to end: shared masking and original spans, marker-only continuation handling, final-subject checks after global/forced routing, close-gesture refusal, typed error codes, staged destination inheritance, resolved Pomodoro agreement and rollback, and kept output. Regression coverage includes editor/execution parity, Unicode/CRLF, URLs, inbox/root/reading defaults, explicit IDs, templates, -R, placement, and multi-item rollback. All three descendant phases and bob-cli-ee.1.1 are closed; plan 202610/capture_type_grammar.md is marked done. just all passed (exit 0); just docs-check passed (447 passed, 1 skipped for absent font dependencies); git diff --check is clean. Follow-ups: clone_on_copy was fixed by a0a6b497, so no task or corroboration; bob-cli-dh is a different repository; memory_record=no remains final, with no memory edit or task. No just symvision recipe is available. Outer epic bob-cli-ee remains open.

## Dependencies

- **Blocks:** [bob-cli-ee.2](bob-cli-ee.2.md) ✓ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-ee.3](bob-cli-ee.3.md) ✓ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-ee.4](bob-cli-ee.4.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ee.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.md) | [bob-cli-ee.1](bob-cli-ee.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ee.1.1.3][1] | grandparent phase decisions | 1 |
| read-by | [agent:bob-cli-ee.1.1.land--1][2] | Inspect the parent phase status after the child epic close command | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.1.land.md

<!-- sase:referenced-by:end -->
