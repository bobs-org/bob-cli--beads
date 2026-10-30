# Bead: bob-cli-ee.1.1.1 — Shared type-marker lexer and execution grammar

[Bead Pages](../README.md) / [bob-cli-ee.1.1](bob-cli-ee.1.1.md) / bob-cli-ee.1.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ee.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.md) · **Assignee:** `bob-cli-ee.1.1.1` · **Size:** medium
**Created:** 2026-10-30 04:33:10 EDT · **Closed:** 2026-10-30 05:14:10 EDT
**Plan:** [202610/capture\_type\_grammar.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_grammar.md)

## Description

language: implement the shared t: lexer, offset-preserving item views, original-draft boundary handling, execution metadata and teaching errors, and template integration. Preserve unmarked grammar and fail closed at the planner until the writes phase enables new-task typing. Add grammar and boundary vectors.

## Notes

[2026-10-30T09:13:55Z · bob-cli-ee.1.1.1] PROPOSED FOLLOW-UP: Reconcile the clean-base Clippy failure with bob-cli-ea #4: current clean base 3b0ffa0a reports clone_on_copy at src/native/gcal/classify.rs:75, reproducing identically with this phase stashed.

[2026-10-30T09:14:10Z · bob-cli-ee.1.1.1] Implemented shared type-marker scanning and execution parsing with byte-stable masking and type metadata; planner rejects typed task writes until the later write phase. Verified 362 capture-language tests pass, 12 focused type-marker/planner tests pass, and git diff --check is clean. just check still fails only on the clean-base clone_on_copy at src/native/gcal/classify.rs:75, reproduced with this phase stashed and recorded as a PROPOSED FOLLOW-UP. epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-ee.1.1.2](bob-cli-ee.1.1.2.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ee.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.1/README.md) | [bob-cli-ee.1.1.1](bob-cli-ee.1.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`59d5a09`](https://github.com/bobs-org/bob-cli/commit/59d5a09380248882dc8ebba850af671ac6b7e0b1) | feat(capture): parse task type markers | [bob-cli-ee.1.1.1](bob-cli-ee.1.1.1.md) | 2026-10-30 05:15:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ee.1.1.1][1] | Need the phase scope, notes, design file, and epic decisions before implementing this reserved phase | 3 |
| read-by | [agent:bob-cli-ee.1.1.2][2] | Check language phase output for shared seam | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.2/README.md

<!-- sase:referenced-by:end -->
