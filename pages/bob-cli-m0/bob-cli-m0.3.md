# Bead: bob-cli-m0.3 — Live layout adapter and lossless executor

[Bead Pages](../README.md) / [bob-cli-m0](README.md) / bob-cli-m0.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e9.md) · **Assignee:** `bob-cli-m0.3` · **Size:** medium
**Created:** 2026-11-15 20:01:48 EST · **Closed:** 2026-11-16 07:04:16 EST
**Plan:** [202611/obsidian\_ctrl\_w\_window\_prefix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_window_prefix.md)

## Description

actions: build the live snapshot adapter and executor that focuses, joins, creates, collapses, and duplicates splits with invariants, rollback, and an API canary.

## Notes

[2026-11-16T12:03:25Z · bob-cli-m0.3] PROPOSED FOLLOW-UP: Clean-base npm test failures remain unrelated: obsidian-block-marks-e2e has a hardcoded-date fixture issue (tracked by bob-cli-m8), the navigation stage-ranker 16 ms budget is tracked by bob-cli-3w, and Ledger Tools timing-budget failures were recorded by bob-cli-m0.1. This run also timed out the browser-backed task-link motion fixture at 90 seconds under full-suite load; it passes 2/2 in isolation, and test:perf passes 5/5.

[2026-11-16T12:04:16Z · bob-cli-m0.3] Implemented and built the live window layout adapter and lossless executor with API canary, left/right split ordering, scroll restoration, empty-leaf duplication, and rollback. Focused adapter/model tests pass 22/22; build check and diff check pass; plugin sync deployed the new bundle. Full npm test has clean-base unrelated failures recorded above; separate perf suite passes 5/5.

## Dependencies

- **Depends on:** [bob-cli-m0.1](bob-cli-m0.1.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-m0.2](bob-cli-m0.2.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-m0.5](bob-cli-m0.5.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-m0.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.3/README.md) | [bob-cli-m0.3](bob-cli-m0.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@4678586`](https://github.com/bobs-org/bob-plugins/commit/4678586a48a18379888946803fd456361731c132) | feat(navigation-hotkeys): add lossless window prefix adapter | [bob-cli-m0.3](bob-cli-m0.3.md) | 2026-11-16 07:07:01 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-m0.3][1] | Need the phase scope and design file, and to inspect prior notes before resuming | 3 |
| read-by | [agent:bob-cli-m0.4--1][2] | Need m0.3 status after wait so we know whether adapter/executor landed before vault sync | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-m0.4.md

<!-- sase:referenced-by:end -->
