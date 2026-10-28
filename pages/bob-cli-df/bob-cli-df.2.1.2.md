# Bead: bob-cli-df.2.1.2 — Read colliding stores safely and expose quarantine in doctor

[Bead Pages](../README.md) / [bob-cli-df.2.1](bob-cli-df.2.1.md) / bob-cli-df.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.md) · **Assignee:** `bob-cli-df.2.1.2` · **Size:** medium
**Created:** 2026-10-27 21:43:19 EDT · **Closed:** 2026-10-27 23:34:36 EDT
**Plan:** [202610/artifact\_link\_collision\_quarantine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_collision_quarantine.md)

## Description

store-quarantine: add historical durability evidence, accepted-event snapshots, quarantine persistence helpers, and doctor reporting in sase.

## Notes

[2026-10-28T03:34:21Z · bob-cli-df.2.1.2] PROPOSED FOLLOW-UP: sase tool run check lint(symvision) fails on stale --epic-symbol rows for closed sase-1p1.2/.3/.5/.6 — Justfile unmodified vs HEAD so it reproduces on the clean base tree; check run b96fffccdd41d915a77251d6fed10fe9 verdict new_failures (4 NEW, 5 KNOWN, witness 87f71b1a9c84ff31284c1917af31d713); same class as bob-cli-df.4.1.2 and bob-cli-df.4.1.3

[2026-10-28T03:34:36Z · bob-cli-df.2.1.2] store-quarantine landed in sase: pinned sase-core-revision.txt to 6613c9bb (collision partition + quarantine contracts); Python gathers evidence/IO and partitions before reducing in store/canonical/project/reconcile; historical git ancestor + local admission sequence; persist/load quarantine records at link-events/quarantine/v1/<op>/<digest>.json; doctor reports Link event quarantine as unhealthy without blocking store writability; 6 new core-rs bindings required. Focused tests 47 passed (store quarantine/history/admission, quarantine IO, health, doctor, validate/bindings). sase tool run check green through fmt/ruff/mypy; lint(symvision) fails identically on clean-HEAD stale sase-1p1.2/.3/.5/.6 epic-symbols (recorded as follow-up citing bob-cli-df.4.1.2/.3). epic-symbols for this phase: none.

## Dependencies

- **Depends on:** [bob-cli-df.2.1.1](bob-cli-df.2.1.1.md) ✓ · ⧖ 2026-10-27
- **Blocks:** [bob-cli-df.2.1.3](bob-cli-df.2.1.3.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.2/README.md) | [bob-cli-df.2.1.2](bob-cli-df.2.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.2][1] | Need the phase scope and design file | 7 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.2/README.md

<!-- sase:referenced-by:end -->
