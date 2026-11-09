# Bead: bob-cli-j5.2.1.2 — Plan archive changes from captured inputs

[Bead Pages](../README.md) / [bob-cli-j5.2.1](bob-cli-j5.2.1.md) / bob-cli-j5.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-j5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.2.md) · **Assignee:** `bob-cli-j5.2.1.2` · **Size:** medium
**Created:** 2026-11-09 12:19:09 EST · **Closed:** 2026-11-09 14:15:51 EST
**Plan:** [202611/guarded\_archive\_writer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/guarded_archive_writer.md)

## Description

archive-snapshot: capture every archive-planning input once, detect exact block replays, regroup changed sources, and validate final postimages before constructing the guarded WritePlan.

## Notes

[2026-11-09T19:15:51Z · bob-cli-j5.2.1.2] archive-snapshot landed: captured input set (source/repair walkers, absent archive dests, Tasks settings via snapshot) drives all planning with no disk fallbacks; structured moved-root records with source line/root id/raw bytes/contained+final ids; byte-exact replay (nested/CRLF, mixed replay+new, threshold-gated, second-run no-op); same-write grouping with structural quiet-period flags and empty-Done-group removal; plan-wide refusal on identity multiplicity/resolution and open #task in done postimages; WritePlan outputs archive-first with original snapshots. Verified: 17 new tests in collect_done/tests/snapshot.rs (replay/collision/mixed/threshold/CRLF/grouping+idempotence/grandfathered/bare-dup/refusal/5x stale-plan rejection via apply_plan), all 6057 lib + 3416 cli workspace tests pass, just lint and cargo fmt clean. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-j5.2.1.1](bob-cli-j5.2.1.1.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j5.2.1.3](bob-cli-j5.2.1.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.2.1.2/README.md) | [bob-cli-j5.2.1.2](bob-cli-j5.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`37df0e5`](https://github.com/bobs-org/bob-cli/commit/37df0e52cf364c82bf5017ea8ee74d9443f66801) | feat(collect-done): snapshot inputs with exact replay and plan-wide refusal | [bob-cli-j5.2.1.2](bob-cli-j5.2.1.2.md) | 2026-11-09 14:18:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j5.2.1.2][1] | check prior notes and remaining work | 2 |
| read-by | [agent:bob-cli-j5.2.1.3][2] | Check predecessor notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.2.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.2.1.3/README.md

<!-- sase:referenced-by:end -->
