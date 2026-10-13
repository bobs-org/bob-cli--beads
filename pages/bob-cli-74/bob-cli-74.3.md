# Bead: bob-cli-74.3 — Project pull-in in bob capture ! and =x closes, JSON and human output

[Bead Pages](../README.md) / [bob-cli-74](README.md) / bob-cli-74.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.73](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.73.md) · **Assignee:** `bob-cli-74.3` · **Size:** medium
**Created:** 2026-10-12 23:40:11 EDT · **Closed:** 2026-10-13 01:08:27 EDT
**Plan:** [202610/project\_pull\_in\_line\_model.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_pull_in_line_model.md)

## Description

cli-capture: keep id-less C in the ! and =x close paths, feed staged project-note text to the planner, build the dependents snapshot only per the Gate, extend SL20, add trigger/hide_removed JSON and surfaced/project-empty human rows, add CLI PP tests including PP23, and measure performance.

## Notes

[2026-10-13T05:08:10Z · bob-cli-74.3] PROPOSED FOLLOW-UP: Verify or fix the two percent-listen failures tracked by bob-cli-6m — just check fails in failed_percent_listen_worker_keeps_listen_retry_guidance and percent_listen_reference_runs_existing_worker_and_installs_audio; both failures and messages reproduce on clean base 5fc27f0.

[2026-10-13T05:08:15Z · bob-cli-74.3] Performance verification: on a temporary copy of the 3.6G Bob vault, 3-run release dry-run medians before (5fc27f0) → after were ordinary non-project ! 0.09s → 0.08s; ordinary non-project =x 0.09s → 0.08s; project with remaining task ! 0.10s → 0.10s; project with remaining task =x 0.09s → 0.09s; last project task ! 0.09s → 0.09s; last project task =x 0.09s → 0.09s. All differences were within run-to-run noise.

[2026-10-13T05:08:27Z · bob-cli-74.3] Implemented project pull-in planning for ! and =x closes, staged post-close notes, gate-scoped dependency snapshots, trigger/hide_removed JSON, and surfaced project rows in human output. Verified with focused CLI tests (9 passed), cargo fmt/git diff --check, and release performance comparisons on a 3.6G vault copy (all within noise). Full just check found the two existing bob-cli-6m percent-listen failures, reproduced on clean base 5fc27f0; recorded them as a proposed follow-up. epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-74.2](bob-cli-74.2.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-74.6](bob-cli-74.6.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-74.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-74.3/README.md) | [bob-cli-74.3](bob-cli-74.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`309e98a`](https://github.com/bobs-org/bob-cli/commit/309e98a92ed290f3893b4fcf4c9e58bb857d94b4) | feat(capture): surface project pull-ins on close | [bob-cli-74.3](bob-cli-74.3.md) | 2026-10-13 01:09:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-74.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-74.3/README.md

<!-- sase:referenced-by:end -->
