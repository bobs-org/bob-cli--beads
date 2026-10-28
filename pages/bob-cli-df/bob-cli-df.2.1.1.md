# Bead: bob-cli-df.2.1.1 — Add the Rust collision partition and quarantine contracts

[Bead Pages](../README.md) / [bob-cli-df.2.1](bob-cli-df.2.1.md) / bob-cli-df.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.md) · **Assignee:** `bob-cli-df.2.1.1` · **Size:** medium
**Created:** 2026-10-27 21:43:19 EDT · **Closed:** 2026-10-27 22:25:25 EDT
**Plan:** [202610/artifact\_link\_collision\_quarantine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_collision_quarantine.md)

## Description

collision-policy: add canonical selection from durability evidence, typed quarantine results, and Python binding coverage in sase-core.

## Notes

[2026-10-28T02:25:15Z · bob-cli-df.2.1.1] PROPOSED FOLLOW-UP: sase-core `sase tool run check` fails identically (27 clippy errors) on the clean base 83b010dd and with this change — pre-existing lints in agent_hold, bead/cli/tests, bead/touch_index, macro_catalog/tests, artifact_ref_commit_budget, gateway/push, macro_lsp tests; needs a separate cleanup bead, not this phase.

[2026-10-28T02:25:25Z · bob-cli-df.2.1.1] collision-policy landed in sase-core: new artifact_link::collision partition + quarantine record wires, facade/lib/prelude exports, 6 registered PyO3 bindings with round-trip test; 14 core tests cover retries, distinct ops, durable-beats-pending/incoming, ancestor/commit-time/history/sequence/tie-break selection, permutations/duplicate roots, 3-payload groups, rejected alias/put/remove/observation exclusion, invalid-event errors, quarantine validate/path, strict reducer still rejects; just fast clean, targeted core (43) + py binding tests pass; full check fails identically (27 pre-existing clippy errors) on clean base 83b010dd, recorded as follow-up

## Dependencies

- **Blocks:** [bob-cli-df.2.1.2](bob-cli-df.2.1.2.md) ◐ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.1/README.md) | [bob-cli-df.2.1.1](bob-cli-df.2.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.1][1] | Need phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.1/README.md

<!-- sase:referenced-by:end -->
