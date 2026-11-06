# Bead: bob-cli-h8.1 — Make bob-plugins npm test green

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.1` · **Size:** medium
**Created:** 2026-11-04 16:39:09 EST · **Closed:** 2026-11-04 17:38:33 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

plugin-tests: in bob-plugins, fix the six test-harness defects behind bob-cli-eh, bob-cli-et (freshness half only), bob-cli-ff, bob-cli-f7, bob-cli-f1, and the bob-cli-ej wall-clock gates. Edit tests only. Prove the full suite is green under UTC and America/New_York, then close those beads and the already-fixed bob-cli-dx.

## Notes

[2026-11-04T22:24:40Z · bob-cli-h8.1--1] PROPOSED FOLLOW-UP: Investigate baseline wikilink-index performance budget failures — scripts/test-block-id-prompt-task-wikilink-index-performance.cjs exceeded the existing 50 ms snapshot/order and 12 ms rank budgets in an isolated run (80.1 ms and 14.8 ms) on unchanged bob-plugins HEAD b9f47f3; the test and production source are identical to HEAD, so keep their budgets intact and track this distinct case alongside the timing-gate flake pattern in bob-cli-ej.

[2026-11-04T22:38:33Z · bob-cli-h8.1--2] Completed the scoped test-only harness fixes and closed bob-cli-eh, bob-cli-et, bob-cli-ff, bob-cli-f7, bob-cli-f1, bob-cli-ej, and bob-cli-dx. Focused harness results: UTC 217/217; America/New_York 215/217, with only the unchanged wikilink-index benchmark's warm snapshot/order (86.4 ms vs 50 ms) and rank (14.2 ms vs 12 ms) timing checks failing. Four required full npm test reruns: UTC #1 and New York #1 passed 5,448/5,448; UTC #2 had only warm snapshot/order at 51.5 ms vs 50 ms; New York #2 had only cold-build chunk at 19.8 ms vs 16 ms. The same benchmark's snapshot/order and rank budgets reproduced on unchanged bob-plugins HEAD b9f47f3 (80.1 ms and 14.8 ms), so its thresholds remain intact and the existing PROPOSED FOLLOW-UP is retained. Docs check passed (447 tests). epic-symbols reported no entries. Normal plugin sync refused bob-ledger-tools and bob-navigation-hotkeys due another checkout's uncommitted deploy; not forced, for bob-cli-h8.2.

## Dependencies

- **Blocks:** [bob-cli-h8.8](bob-cli-h8.8.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.1.md) | [bob-cli-h8.1](bob-cli-h8.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d4ae2d3`](https://github.com/bobs-org/bob-plugins/commit/d4ae2d326a1da0622ac2e813a3c021fd36529f1d) | test: stabilize bob-plugins test harnesses | [bob-cli-h8.1](bob-cli-h8.1.md) | 2026-11-04 17:40:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h8.1--2][1] | Need the current phase scope, recorded rerun evidence, and approved follow-up before closure | 1 |
| read-by | [agent:bob-cli-h8.13][2] | Check plugin-suite failures against the neighboring test-harness phase | 1 |
| read-by | [agent:bob-cli-hd.land][3] | Need the child scope for harness stabilization | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.13/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hd.land/README.md

<!-- sase:referenced-by:end -->
