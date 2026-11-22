# Bead: bob-cli-on.8.1.2 — Requirement verdict resolution and refusal rules

[Bead Pages](../README.md) / [bob-cli-on.8.1](bob-cli-on.8.1.md) / bob-cli-on.8.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.md) · **Assignee:** `bob-cli-on.8.1.2` · **Size:** medium
**Created:** 2026-11-22 07:22:30 EST · **Closed:** 2026-11-22 08:41:40 EST
**Plan:** [202611/requirement\_close\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/requirement_close_engine.md)

## Description

choices: implement the pure Met, Drop, Carry, and Carry-Pulled selection model, shared card numbering, overlap and snapshot validation, and requirement-aware mark-all exclusion with RV selection vectors.

## Notes

[2026-11-22T13:41:40Z · bob-cli-on.8.1.2] Implemented the pure Met/Drop/Carry/Carry-Pulled selection model, requirement-first shared numbering, mark-all exclusion, overlap and exact-preimage validation, stale-card recovery data, and RV12-RV19 selection vectors. Verified cargo test native::task_complete::tests (227 passed), cargo test req_verdict_tests (7 passed), cargo fmt --all -- --check, git diff --check, and no remaining epic symbols.

## Dependencies

- **Depends on:** [bob-cli-on.8.1.1](bob-cli-on.8.1.1.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.8.1.3](bob-cli-on.8.1.3.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.2/README.md) | [bob-cli-on.8.1.2](bob-cli-on.8.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.8.1.2][1] | Need the phase scope, design file, and prior notes before implementation | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.2/README.md

<!-- sase:referenced-by:end -->
