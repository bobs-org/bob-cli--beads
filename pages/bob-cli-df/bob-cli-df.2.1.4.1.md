# Bead: bob-cli-df.2.1.4.1 — Repair Rust collision ordering across history and duplicate roots

[Bead Pages](../README.md) / [bob-cli-df.2.1.4](bob-cli-df.2.1.4.md) / bob-cli-df.2.1.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.land.md) · **Assignee:** `bob-cli-df.2.1.4.1` · **Size:** medium
**Created:** 2026-10-28 02:07:52 EDT · **Closed:** 2026-10-28 03:19:10 EDT
**Plan:** [202610/artifact\_link\_quarantine\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_quarantine_landing_repairs.md)

## Description

ordering-policy: preserve earliest evidence, compare actual instants, and respect ancestry across the complete group.

## Notes

[2026-10-28T07:19:03Z · bob-cli-df.2.1.4.1--5] PROPOSED FOLLOW-UP: Recheck and resolve the 27 existing Clippy errors tracked by bob-cli-dh; the governed check emitted identical diagnostics on this phase tree and clean base 83b010dd. The focused artifact_link and artifact_link_collision_bindings_round_trip suites passed.

[2026-10-28T07:19:10Z · bob-cli-df.2.1.4.1--5] Implemented complete-group collision ordering by actual instants and ancestry, retaining earliest evidence across duplicate roots. Verified with just test -p sase_core artifact_link and just test -p sase_core_py artifact_link_collision_bindings_round_trip; both passed. sase tool run check remains red on 27 Clippy diagnostics identical to clean base 83b010dd and tracked by bob-cli-dh. epic-symbols had no leftovers.

## Dependencies

- **Blocks:** [bob-cli-df.2.1.4.2](bob-cli-df.2.1.4.2.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.4.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.1.md) | [bob-cli-df.2.1.4.1](bob-cli-df.2.1.4.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.4.1--5][1] | Need the phase scope, notes, and design file before finishing the assigned work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.1.md

<!-- sase:referenced-by:end -->
