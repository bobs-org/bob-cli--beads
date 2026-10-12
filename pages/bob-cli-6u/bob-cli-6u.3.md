# Bead: bob-cli-6u.3 — Rust freshness reads and writes \[unblocked::\]

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.3` · **Size:** medium
**Created:** 2026-10-12 10:25:46 EDT · **Closed:** 2026-10-12 11:20:59 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

cli-freshness: placement (run-extending key, mark/clear/prune helpers, stamps clear it, lint), evaluator (RESURFACED from scheduled or unblocked, TICKLER due_on, tie order, keeps), bob freshness output and schema bump, UB vectors.

## Notes

[2026-10-12T15:20:40Z · bob-cli-6u.3] PROPOSED FOLLOW-UP: just check has 2 pre-existing capture::r#ref percent-listen failures (failed_percent_listen_worker_keeps_listen_retry_guidance, percent_listen_reference_runs_existing_worker_and_installs_audio) that fail identically on the clean base tree; tracked by bob-cli-6m

[2026-10-12T15:20:46Z · bob-cli-6u.3] PROPOSED FOLLOW-UP: highlights_ref listen test run_listen_reports_interrupt_exits flaked once under full-suite parallelism (ETXTBSY from sase listen render) but passes in isolation on both base and this tree; likely environmental, watch for recurrence

[2026-10-12T15:20:59Z · bob-cli-6u.3] cli-freshness done and verified: placement (unblocked run-extending key, canonical order fresh/refresh/keeps/unblocked, mark_unblocked WRITE skips UB2-UB6, clear/prune helpers, stamps clear it, fresh_misplaced covers it, new unblocked_malformed/duplicate lints), evaluator (returned_on/by per Design S4, RESURFACED from either source, TICKLER due_on=returned_on, TICKLER order due_on-path-line keeping R2 green, decide_for never decides unblock ticklers per unblock_keeps=yes), CLI schema 13->14 with returned_by/unblocked_on rows and tickler-unblocked human copy, UB vectors in state_tests/placement_tests/CLI tests plus 3 vectors.json rows with rust+js runners, UB12 parser invariance for both Rust parsers. just check: fmt+clippy clean, all freshness/note_ready/seed suites green; only failures are 2 base-identical pre-existing percent-listen tests (bob-cli-6m) and 1 environmental listen flake green in isolation (both recorded as follow-ups). note_ready row_bucket confirmed: unblock tickler is bucket rotten so counts as rotten make-up; docs/plan.md already says rotten includes resurfaced, no edit needed.

## Dependencies

- **Depends on:** [bob-cli-6u.1](bob-cli-6u.1.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.10](bob-cli-6u.10.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.5](bob-cli-6u.5.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.7](bob-cli-6u.7.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.3/README.md) | [bob-cli-6u.3](bob-cli-6u.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f51ba28`](https://github.com/bobs-org/bob-cli/commit/f51ba2890392ccf32e84dc0d9751c12bb4177912) | feat(freshness): read and write \[unblocked::\] with RESURFACED evaluation | [bob-cli-6u.3](bob-cli-6u.3.md) | 2026-10-12 11:22:28 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md

<!-- sase:referenced-by:end -->
