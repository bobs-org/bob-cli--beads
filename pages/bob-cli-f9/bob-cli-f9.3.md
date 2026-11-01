# Bead: bob-cli-f9.3 — bob plan reports and prints Today roots

[Bead Pages](../README.md) / [bob-cli-f9](README.md) / bob-cli-f9.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.by](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.by.md) · **Assignee:** `bob-cli-f9.3` · **Size:** medium
**Created:** 2026-11-01 12:12:36 EST · **Closed:** 2026-11-01 14:31:19 EST
**Plan:** [202611/retire\_type\_cap\_today\_roots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/retire_type_cap_today_roots.md)

## Description

cli-today-roots: write the Today roots contract in docs/plan.md, compute today_roots in Rust from today_tasks via the Pomodoro home resolver, print the ROOTS line, and add shared today_roots conformance vectors.

## Notes

[2026-11-01T19:31:19Z · bob-cli-f9.3] Added docs/plan.md ## Today roots contract (+Surfaces, bob plan JSON/human sample, TODAY badge paragraph no longer mentions type red, pomodoro-homes R7 cross-link and vector table, json-outputs, task-status-hooks sample). New src/native/plan_budget/roots.rs: today_roots() groups today_tasks via HomeResolver::home_for_link (honors [root::]), orders count desc / first-task / @unfiled last, hue = resolve_note(root).hue (area) per root_ring_hue=area; PlanReport.today_roots always serialized; ROOTS line under PLAN with root_counts=counts; bob task reconcile plan_budget carries same roots. 12 shared today_roots vectors in tests/fixtures/pomodoro_homes/vectors.json (existing cases byte-identical; hand-computed expectations pass in Rust), CLI integration tests, partition invariant asserted. Verified: just all (fmt, lint, test) and just docs-check pass after just docs-gen and just docs-media (plan.svg re-captured); live bob plan against ~/bob printed ROOTS 3+2+1+1 = TODAY 7. Left for f9.5: copy vectors.json byte-for-byte and mirror the contract in JS.

## Dependencies

- **Depends on:** [bob-cli-f9.2](bob-cli-f9.2.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f9.5](bob-cli-f9.5.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f9.3/README.md) | [bob-cli-f9.3](bob-cli-f9.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f9.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f9.3/README.md

<!-- sase:referenced-by:end -->
