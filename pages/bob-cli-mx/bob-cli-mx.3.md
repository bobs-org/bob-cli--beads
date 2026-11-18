# Bead: bob-cli-mx.3 — Pin the walker footer to the walks conformance vectors

[Bead Pages](../README.md) / [bob-cli-mx](README.md) / bob-cli-mx.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.es.md) · **Assignee:** `bob-cli-mx.3` · **Size:** small
**Created:** 2026-11-17 17:59:53 EST · **Closed:** 2026-11-17 20:43:06 EST
**Plan:** [202611/mac\_walk\_attention\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_walk_attention_marks.md)

## Description

plugin-parity: run the docs/walks.md vectors against bob-ledger-tools' real attention pushes in a JS test, fix any drift in favor of the contract, link the contract from the plugin docs, and sync.

## Notes

[2026-11-18T01:42:37Z · bob-cli-mx.3] PROPOSED FOLLOW-UP: docs-check lint fails on clean base with reference/plugins/bob-ledger-tools.md over word budget (6028/6000, observed before this phase touched docs); this phase kept the source budget-neutral (6000 to 5998 countable words). Related trims tracked by bob-cli-lt.7, bob-cli-lt.8, bob-cli-ls.7

[2026-11-18T01:42:43Z · bob-cli-mx.3] PROPOSED FOLLOW-UP: docs-check fails generated drift on docs/reference/glossary.md on current master with a pristine plugin tree; also seen on bob-cli-my.1 and bob-cli-mj.6

[2026-11-18T01:42:50Z · bob-cli-mx.3] PROPOSED FOLLOW-UP: test-ledger-tools-record-sheet midnight-rollover timer test fails identically on the untouched base tree (flake); four perf-budget tests fail only under full-suite load and pass in isolation

[2026-11-18T01:43:06Z · bob-cli-mx.3] plugin-parity done: new scripts/test-ledger-tools-walk-attention-vectors.cjs runs all 18 docs/walks.md vectors (S1-S5, W1-W8, B1-B4) verbatim through walkerFooterPushReviewAttention, laneWalkQueueFromTasks+walkerFooterPushLaneAttention, and bank snapshots with a stub walkMode v6; 17/17 pass with zero drift so no plugin src changes were needed (contract wins by default). Wired into npm test test:unit; full npm test 7278/7286 with only pre-existing failures (5 fail identically or environmentally, verified on clean base/isolated runs, recorded as follow-ups). Docs: contract linked from bob-ledger-tools.md attention paragraph plus Related entry (source kept at 5998/6000 words), stale [[ s w n ]] fixed to [[ s w n b ]] in nav-hotkeys manifest with docs regen. build:check, docs:inventory:check green; bob plugins sync deployed (1 copied).

## Dependencies

- **Depends on:** [bob-cli-mx.2](bob-cli-mx.2.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mx.3/README.md) | [bob-cli-mx.3](bob-cli-mx.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mx.3][1] | Need phase notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mx.3/README.md

<!-- sase:referenced-by:end -->
