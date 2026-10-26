# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1 — Give the capture\_related synthetic-vault lib perf gates a paired baseline

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1` · **Size:** small
**Created:** 2026-10-26 08:32:07 EDT
**Plan:** [202610/backlog\_batch12\_perf\_baseline\_fakenode\_daystrip\_blocks\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch12_perf_baseline_fakenode_daystrip_blocks_notice.md)

## Description

capture-related-perf-baseline: resolve bob-cli-ca by moving both src/native/capture_related synthetic-vault wall-clock gates onto the warmed, paired-baseline pattern from 0e75ca56, proving they still catch a real slowdown and no longer fail under parallel just check load.

## Notes

[2026-10-26T12:47:25Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1] Baseline: both lib gates in src/native/capture_related/tests.rs (synthetic_vault_query_is_under_250ms, synthetic_vault_draft_contract_is_under_250ms) timed one debug run of the 40x38 synthetic vault and asserted elapsed < 500 ms. That is the flake bob-cli-ca reports under parallel just check.

Fix: shared synthetic_perf_vaults() plus assert_paired_perf_gate() following 0e75ca56. Untimed warmup, then 7 paired timed runs against a one-task tiny vault; gate min(big-tiny) < 500 ms and min_big < 2000 ms. Functional same_title / items.len()==1 asserts kept. bob-cli-ca left open for the lander.

Tests: (1) Temporary 600 ms sleep in the big timed path (not committed) failed both gates: query min_diff 704 ms, draft min_diff 716 ms. (2) 8/8 isolated cargo test --lib synthetic_vault_ passes while a concurrent cargo test --lib ran (loadavg 20.01 16.83 13.78). (3) just check passed; both tests ok in the 3556-test lib suite.

Limitations: the 500 ms paired floor still matches the old isolated budget; a slowdown smaller than scheduling noise can still hide. Gross 2000 ms bound is for order-of-magnitude regressions only.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1.md) | 0 |
