# Bead: bob-cli-h0.6 — Typing \`- ^^\` in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-h0](README.md) / bob-cli-h0.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.37.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.37.linker.w0.md) · **Assignee:** `bob-cli-h0.6` · **Size:** small
**Created:** 2026-11-04 08:50:24 EST · **Closed:** 2026-11-04 10:38:58 EST
**Plan:** [202611/move\_choice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/move_choice.md)

## Description

mac-draft: honor Bob's `action_continuation_keys` in the Move picker so a second `^` leaves `- ^^`, show the footer hint, and colour the choice marker span.

## Notes

[2026-11-04T15:38:58Z · bob-cli-h0.6] Implemented Mac Capture handling for Bob's action_continuation_keys in the Move picker: typing the second ^ inserts - ^^, the footer explains the choice, and the choice-marker span uses the route color. Verified with an athena portable build and a scratch Mac bundle plus typecheck-tests; no epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-h0.2](bob-cli-h0.2.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h0.8](bob-cli-h0.8.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-h0.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.6/README.md) | [bob-cli-h0.6](bob-cli-h0.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@0df42dc`](https://github.com/bobs-org/bob-mac-capture/commit/0df42dc667c7dad009ec0e58b925b0f07f637fe7) | feat(capture): support move-choice continuation in Mac Capture | [bob-cli-h0.6](bob-cli-h0.6.md) | 2026-11-04 10:40:21 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h0.6][1] | Need the phase notes to check prior work before continuing | 2 |
| read-by | [agent:bob-cli-h0.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.6/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-h0.land.md

<!-- sase:referenced-by:end -->
