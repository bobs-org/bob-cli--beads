# Bead: bob-cli-bp.2 — Stats fetch service fixes for the Stats page and the strip

[Bead Pages](../README.md) / [bob-cli-bp](README.md) / bob-cli-bp.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2f.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2f.linker.w1.md) · **Assignee:** `bob-cli-bp.2` · **Size:** medium
**Created:** 2026-10-24 16:30:44 EDT · **Closed:** 2026-10-24 16:56:22 EDT
**Plan:** [202610/daily\_note\_day\_strip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_note_day_strip.md)

## Description

fetch-service: in bob-plugins' bob-ledger-tools, give each key its own in-flight promise behind a FIFO queue so no waiter is lost, track change generations and fetch ages so cache hits spawn only when dirty, add a cache-update listener API, a synchronous peek, and `group`. Also gate Stats page revalidation on visibility and add spawn counters.

## Notes

[2026-10-24T20:55:53Z · bob-cli-bp.2] PROPOSED FOLLOW-UP: Skipped memory decision decision_record=no — add decisions:day-strip-shows-the-days-facts-facts placement/facts-not-targets record (applies to bob-ledger-tools and bob-cli) once the strip ships

[2026-10-24T20:56:02Z · bob-cli-bp.2] PROPOSED FOLLOW-UP: Skipped memory decision glossary_term=no — add Day Strip glossary term (aliases: day stats), distinguished from the Morning GTD Review Footer, once the strip ships

[2026-10-24T20:56:08Z · bob-cli-bp.2] PROPOSED FOLLOW-UP: Load-sensitive perf budget test-navigation-dependencies-stage-entry-and-view stage-ranker 16ms budget fails under full-suite parallel load (24-44ms) but passes solo (11ms, 23/23); untouched navigation file, unrelated to fetch-service — consider raising budget or isolating the perf test

[2026-10-24T20:56:22Z · bob-cli-bp.2] fetch-service done in bob-ledger-tools: per-key in-flight FIFO queue (no lost waiters, cap 8 with cancelled drop), change-generation + 10min-age dirty gating (warm remount spawns nothing), statsPeek/statsOnCacheUpdate/group, visibility-gated Stats revalidation with needsRevalidate flush, spawn counters. Verified: npm run build + build:check clean, stats-data + stats-block suites 46/46 green, npm run validate 7/7 valid, bob plugins sync deployed to vault (VAULT IN SYNC) and bob stats show -a -f json resolves on apollo. Full npm test 3598/3599 with one unrelated load-flaky 16ms perf budget (passes solo 11ms), recorded as follow-up. Fragments 829/400/901 lines, no new test files, main.js via build only.

## Dependencies

- **Blocks:** [bob-cli-bp.3](bob-cli-bp.3.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bp.4](bob-cli-bp.4.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bp.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.2/README.md) | [bob-cli-bp.2](bob-cli-bp.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6ce2e17`](https://github.com/bobs-org/bob-plugins/commit/6ce2e17b63f645295a5f5c0e20d47bbff2418d85) | feat(ledger-tools): per-key FIFO fetch queue with stats cache, peek and grouping | [bob-cli-bp.2](bob-cli-bp.2.md) | 2026-10-24 16:57:37 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bp.2][1] | full read | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.2/README.md

<!-- sase:referenced-by:end -->
