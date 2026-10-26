# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5 — Coalesce relation-index publishes and memoize the task memo

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5` · **Size:** medium
**Created:** 2026-10-26 12:58:46 EDT · **Closed:** 2026-10-26 13:30:29 EDT
**Plan:** [202610/backlog\_batch14\_ledger\_integrity\_mac\_ci\_and\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md)

## Description

relation-index-coalesce: resolve bob-cli-a5 by collapsing event-driven relation-index publishes to one per turn and reusing the task memo within it, with storm regression coverage and a sync deploy.

## Notes

[2026-10-26T17:30:17Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5] BASELINE: every vault/metadata/overlay/scan event called publishRelationIndex(), which copied the records Map, rebuilt relationIndexTaskMemo() over every Tasks task, and walked all edges.

FIX: event-driven publishes now schedule one microtask rebuild via scheduleRelationIndexPublish(); api.relationIndex v1 reads (generation, ready, outgoing, incoming, labelSuggestions) and relationLabels.rows flush a pending publish so v1 never serves a stale snapshot; the Tasks task memo is reused until that turn ends.

TESTS: npm test 3777 pass; npm run validate pass. New coverage in scripts/test-ledger-tools-relation-index.cjs: 40 metadata events produce one publish, one memo build, and one onChange; a v1 read after an event flushes the pending rebuild without waiting for the microtask.

COST: synthetic 40-file index — uncoalesced apply+flush 27.6ms, coalesced event-stack 0.58ms + turn 1.43ms. Vault copy (6725 md, 3223 prefiltered, 250 synthetic relations) — uncoalesced storm 196.96ms vs coalesced 140.79ms (40 parses of a 293KB daily plus one publish).

DEPLOY: rebased onto origin/master 5790364, rebuilt, bob plugins sync --no-pull -p bob-ledger-tools from this checkout; copied main.js.

LIMITATIONS: bob-cli-a5 left open for the lander. Distinct async turns (scan chunks, target-read promises) still publish separately. Live Obsidian renderer cost was not measured in-app.

DECISIONS: theme_field_strip and legacy_key do not apply to this phase.

[2026-10-26T17:30:29Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5] Coalesced event-driven relation-index publishes to one microtask rebuild with same-turn task-memo reuse; v1 reads flush pending state. Verified: npm test 3777 pass, npm run validate pass, storm test (40 events → 1 publish + 1 memo), read-after-event freshness, vault storm 196.96ms → 140.79ms, deployed bob-ledger-tools via bob plugins sync after rebase onto origin/master 5790364. Left bob-cli-a5 open for the lander. No --epic-symbol leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5][1] | Confirm the phase bead stayed closed after final submit | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.5/README.md

<!-- sase:referenced-by:end -->
