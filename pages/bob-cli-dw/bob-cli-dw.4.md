# Bead: bob-cli-dw.4 — Retune the capture\_related paired lib perf gates after post-fix recurrence

[Bead Pages](../README.md) / [bob-cli-dw](README.md) / bob-cli-dw.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-dp.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dp.land.md) · **Assignee:** `bob-cli-dw.4` · **Size:** small
**Created:** 2026-10-28 15:35:24 EDT · **Closed:** 2026-10-28 15:49:00 EDT
**Plan:** [202610/backlog\_batch\_b6.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b6.md)

## Description

capture-related-perf-flake: resolve bob-cli-ca in bob-cli src/native/capture_related/tests.rs. Both synthetic_vault_query_is_under_250ms and synthetic_vault_draft_contract_is_under_250ms still flake under parallel cargo test load after the paired-baseline fix 7b8c5ddb. Reopened by bob-cli-do.land +1 on 2026-10-28: just check f9d3fb57f9ada3da1680791bcbf3d156 failed synthetic_vault_draft_contract_is_under_250ms with paired excess 517.54 ms against 500 ms; isolated rerun passed and later just check 6dda6f4fd3b209fa1e6f3cff9e65b629 passed. Keep the paired-baseline design (warmup, min(big-tiny) plus gross bound); retune the bound, pairing, or load isolation so the gate stays meaningful under parallel suite load. Verify with focused isolated and parallel runs plus just check / sase tool run check. Related closed bob-cli-bo and bob-cli-d9 are load-tolerance precedents, not duplicates.

## Notes

[2026-10-28T19:49:00Z · bob-cli-dw.4] Retuned paired capture_related perf excess ceiling from 500 ms to 750 ms while retaining the 2 s gross bound and seven paired samples. Both focused tests passed isolated and in parallel; just check passed (3,832 lib tests, 2,362 CLI tests, remaining workspace tests); git diff --check clean; epic-symbols empty.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dw.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dw.4/README.md) | [bob-cli-dw.4](bob-cli-dw.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dw.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dw.4/README.md

<!-- sase:referenced-by:end -->
