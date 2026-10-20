# Bead: bob-cli-a0.7.1.2 — Configuration reference and environment drift guard

[Bead Pages](../README.md) / [bob-cli-a0.7.1](bob-cli-a0.7.1.md) / bob-cli-a0.7.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.md) · **Assignee:** `bob-cli-a0.7.1.2` · **Size:** medium
**Created:** 2026-10-19 23:14:29 EDT · **Closed:** 2026-10-19 23:33:06 EDT
**Plan:** [202610/product\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/product_reference.md)

## Description

configuration-guard: document configuration keys and public environment variables, add a conservative production-source BOB_* inventory with reasoned exceptions to docs lint, and test the guard's detection and exclusions.

## Notes

[2026-10-20T03:33:06Z · bob-cli-a0.7.1.2--1] Added the configuration reference and production BOB_* drift guard with reasoned exceptions and focused fixtures. Verified 60 focused docs tests, full docs-check including 213 passing documentation tests (3 skipped), strict site build, link checks, and no remaining epic symbols.

## Dependencies

- **Blocks:** [bob-cli-a0.7.1.3](bob-cli-a0.7.1.3.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.1.2.md) | [bob-cli-a0.7.1.2](bob-cli-a0.7.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5d3ad7d`](https://github.com/bobs-org/bob-cli/commit/5d3ad7d0adcb32a128839eafe2f3dde10421ab00) | feat(docs): document configuration and guard environment drift | [bob-cli-a0.7.1.2](bob-cli-a0.7.1.2.md) | 2026-10-19 23:34:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.7.1.2--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.1.2.md

<!-- sase:referenced-by:end -->
