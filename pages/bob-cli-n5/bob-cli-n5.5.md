# Bead: bob-cli-n5.5 — Stabilize the dependency-stage ranker performance gate

[Bead Pages](../README.md) / [bob-cli-n5](README.md) / bob-cli-n5.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-my.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-my.land.md) · **Assignee:** `bob-cli-n5.5` · **Size:** medium
**Created:** 2026-11-17 22:21:55 EST · **Closed:** 2026-11-18 01:21:29 EST
**Plan:** [202611/backlog\_triage\_t3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t3.md)

## Description

ranker-measurement: resolve bob-cli-3w with meaningful load-independent regression measurement.

## Notes

[2026-11-18T06:21:12Z · bob-cli-n5.5] PROPOSED FOLLOW-UP: full npm test wall-clock miss in test-ledger-tools-keep-moving-marks-surface.cjs:486 (200-link Live Preview build took 1072.6 ms vs 250 ms budget, performance.now wall clock) while the same file passed 14/14 standalone; untouched by n5.5, same parallel-load signature as 3w — triage against bob-cli-lp family

[2026-11-18T06:21:16Z · bob-cli-n5.5] PROPOSED FOLLOW-UP: full npm test wall-clock miss in test-navigation-dependencies-stage-performance.cjs:64 (400-task sync build 268.1 ms vs 250 ms budget) while the file passed 9/9 standalone; untouched by n5.5, matches excluded m1 stage-opening growth-ratio node — leave for its owning work

[2026-11-18T06:21:29Z · bob-cli-n5.5] CPU-work gate landed in scripts/test-navigation-dependencies-stage-entry-and-view.cjs (test-only, no version bump). The 1000-task/16ms gate now asserts on min CPU over 7 warmed runs via process.cpuUsage/threadCpuUsage convention shared with task-wikilink-index-perf-support.cjs, keeping wall samples plus clock source and host load as diagnostics; budget and workload unchanged, all correctness assertions retained. New seam test proves a 50ms parked sleep charges ~0 CPU (budget survives) while a real CPU spin past budget fails the same predicate. Evidence: file standalone 27/27 pass x3; full npm test 7301/7305 with both ranker tests passing under loadavg ~27-37 (2 unrelated wall-clock misses in untouched files recorded as PROPOSED FOLLOW-UPs). bob plugins sync run: no built bundles changed by this edit; 2 plugin overwrites refused to protect running workspaces 10/11 — no -F per AGENTS.md. 3w left open for lander verification.

## Dependencies

- **Depends on:** [bob-cli-n5.4](bob-cli-n5.4.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-n5.5/README.md) | [bob-cli-n5.5](bob-cli-n5.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@87c7b72`](https://github.com/bobs-org/bob-plugins/commit/87c7b721ca38ae2380b8c1b446b060bf7e2ff729) | test(nav): gate stage-ranker budget on CPU work, not wall time | [bob-cli-n5.5](bob-cli-n5.5.md) | 2026-11-18 01:22:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-n5.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-n5.5/README.md

<!-- sase:referenced-by:end -->
