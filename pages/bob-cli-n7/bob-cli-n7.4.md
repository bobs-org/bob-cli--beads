# Bead: bob-cli-n7.4 — Gate the 200-link Live Preview budgets on CPU work

[Bead Pages](../README.md) / [bob-cli-n7](README.md) / bob-cli-n7.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-n5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n5.land.md) · **Assignee:** `bob-cli-n7.4` · **Size:** medium
**Created:** 2026-11-18 01:55:52 EST · **Closed:** 2026-11-18 10:43:54 EST
**Plan:** [202611/backlog\_triage\_t4.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t4.md)

## Description

cpu-gates: Resolve bob-cli-ju (off-clock link chips, 35 ms) and bob-cli-ki (keep-moving marks surface, 250 ms) by measuring CPU work with the convention bob-cli-3w established, with unchanged budgets and workloads.

## Notes

[2026-11-18T15:43:26Z · bob-cli-n7.4--1] PROPOSED FOLLOW-UP: Full npm test monitor babjt7h3chky exposed two unrelated timing misses: frees-marks synthetic build 93 ms vs 25 ms (existing tracker bob-cli-io) and dependency-stage 1000-task build 2180.6 ms vs 1000 ms (existing tracker bob-cli-m1). Both failures occurred under host loadavg 53.4/38.1/36.4 on 64 CPUs; the assigned CPU gates passed. No new bead created.

[2026-11-18T15:43:54Z · bob-cli-n7.4--1] CPU-work gates verified in focused and full npm test runs; both assigned task beads closed with CPU/wall samples, load, and seam evidence. Full suite had two unrelated timing misses recorded as proposed follow-ups and matched to bob-cli-io and bob-cli-m1. Plugin sync completed without force after landing c7e6d3e.

## Dependencies

- **Depends on:** [bob-cli-n7.3](bob-cli-n7.3.md) ✓ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n7.4.md) | [bob-cli-n7.4](bob-cli-n7.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b2a6d2b`](https://github.com/bobs-org/bob-plugins/commit/b2a6d2bf56963702af02d45da362db0141c1295b) | test(perf): measure Live Preview budgets with CPU time | [bob-cli-n7.4](bob-cli-n7.4.md) | 2026-11-18 10:45:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-n7.4--1][1] | Need the assigned phase scope, notes, and design file before recording suite results | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n7.4.md

<!-- sase:referenced-by:end -->
