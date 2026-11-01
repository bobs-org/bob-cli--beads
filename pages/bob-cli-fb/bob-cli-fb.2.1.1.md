# Bead: bob-cli-fb.2.1.1 — Implement the keep-moving successor engine

[Bead Pages](../README.md) / [bob-cli-fb.2.1](bob-cli-fb.2.1.md) / bob-cli-fb.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.md) · **Assignee:** `bob-cli-fb.2.1.1` · **Size:** medium
**Created:** 2026-11-01 13:00:27 EST · **Closed:** 2026-11-01 13:40:57 EST
**Plan:** [202611/leaf\_keep\_moving\_rust.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/leaf_keep_moving_rust.md)

## Description

engine: implement leaf detection, cost gates, K1-K8, candidate classification, stable ordering, picks, and separate keep-moving rows in the shared Rust engine, with LP and pure KM tests.

## Notes

[2026-11-01T18:40:57Z · bob-cli-fb.2.1.1] Implemented keep-moving engine in keep_moving.rs: HomeResolver leaf detection, G1-G3 no-I/O pre-gate, K1-K8 classification, separate keep_moving rows/folds, Pending-Next-Ready lane order, unpicked no-write, KM31 incomplete snapshot. LP1-LP12 and KM engine vectors pass; existing successor/pull-in tests pass (151 task_complete); clippy -D unused clean; no --epic-symbol leftovers. Capture callers still pass keep_moving: false.

## Dependencies

- **Blocks:** [bob-cli-fb.2.1.2](bob-cli-fb.2.1.2.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fb.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.1.1.md) | [bob-cli-fb.2.1.1](bob-cli-fb.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f6d3084`](https://github.com/bobs-org/bob-cli/commit/f6d3084bb7796b56292f820f62b0cea5bedab472) | feat(task-complete): add leaf-project keep-moving successor engine | [bob-cli-fb.2.1.1](bob-cli-fb.2.1.1.md) | 2026-11-01 14:31:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fb.2.1.1--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.1.1.md

<!-- sase:referenced-by:end -->
