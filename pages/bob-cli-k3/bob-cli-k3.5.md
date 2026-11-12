# Bead: bob-cli-k3.5 — The generated records index inside each album, rebuilt with every record write

[Bead Pages](../README.md) / [bob-cli-k3](README.md) / bob-cli-k3.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.43.linker.w0` · **Assignee:** `bob-cli-k3.5` · **Size:** large
**Created:** 2026-11-11 04:56:44 EST · **Closed:** 2026-11-11 18:17:45 EST
**Plan:** [202611/album\_and\_record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md)

## Description

album-index: render the bob-owned `[!records]` index (tally title, groups in declared status order, sub-groups by `index_by`, faceted rows), rebuild it in the same transaction as every capture or `bob records` write from the album slice alone, and add `bob albums sync` plus its nightly step.

## Notes

[2026-11-11T23:18:30Z · bob-cli-k3.5.1.land] Child epic bob-cli-k3.5.1 closed with landing repairs verified: renderer (byte-exact grouped index, inert tally, current/missing/stale/damaged states), atomic record writes (capture batch and records new/update stage one final album edit with preimage guards, damaged refuses, net-zero guards, unified dry-run diffs), sync plus nightly (guarded transaction, scoped commit, no-op second sync, continue-after-failure). No epic symbols. Plan 202611/album_records_index.md marked done. Extension point for owner-catalog phase bob-cli-k3.6: albums::sync::plan_indexes / IndexSyncPlan. Epic bob-cli-k3 and phase bob-cli-k3.6 left to existing workers.

## Dependencies

- **Depends on:** [bob-cli-k3.3](bob-cli-k3.3.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-k3.4](bob-cli-k3.4.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k3.6](bob-cli-k3.6.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.5.md) | [bob-cli-k3.5](bob-cli-k3.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.47.mus][1] | Need records index details for bank album research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.mus/README.md

<!-- sase:referenced-by:end -->
