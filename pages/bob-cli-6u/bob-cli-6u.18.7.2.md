# Bead: bob-cli-6u.18.7.2 — Capture struck-link insert, closed-status, and consumed-link output fixes

[Bead Pages](../README.md) / [bob-cli-6u.18.7](bob-cli-6u.18.7.md) / bob-cli-6u.18.7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.land.md) · **Assignee:** `bob-cli-6u.18.7.2` · **Size:** small
**Created:** 2026-10-12 20:32:25 EDT · **Closed:** 2026-10-12 20:57:55 EDT
**Plan:** [202610/prj\_line\_blocking\_land\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_land_audit_fixes.md)

## Description

cli-capture: the toggle insert ignores struck links, + rendering uses configured closed statuses, consumed @r:id gets honest human and JSON output, a fenced-index regression test that fails on the old code, and complete capture docs.

## Notes

[2026-10-13T00:42:01Z · bob-cli-6u.18.7.2] Implemented: insertion now detects only unstruck child links and has a struck-history regression; project-note + rendering and the new-task project-block helper use configured status types, with a custom Cancelled regression; consumed @route:id emits kind="link_guard", a non-success human summary, and additive removed_pomodoro_links/day_file only when cleanup occurred; added the shifted-fence resident regression; documented consumed-shape omissions and added the bob-cli-73 renderer note. cargo fmt and git diff --check pass. Full just check is pending.

[2026-10-13T00:57:40Z · bob-cli-6u.18.7.2--1] PROPOSED FOLLOW-UP: Continue investigating the two deterministic percent-listen CLI failures tracked by bob-cli-6m (percent_listen_reference_runs_existing_worker_and_installs_audio and failed_percent_listen_worker_keeps_listen_retry_guidance); this phase's just check reproduced both, while 1,405 CLI tests and all 2,451 unit tests passed. Phase verification: cargo fmt --check and git diff --check pass; the blocked-target consumed-link regression passes alone and now asserts the additive removed_pomodoro_links=1 and day_file fields emitted when cleanup occurs. The full just check otherwise passes clippy and all remaining targets. Capture JSON remains additive; implementation/docs/tests cover struck-link insertion, configured closed statuses, truthful consumed-link human/JSON output, and the fenced-index regression. No other skipped findings.

[2026-10-13T00:57:55Z · bob-cli-6u.18.7.2--1] Completed capture fixes and documented additive JSON behavior. cargo fmt --check and git diff --check pass; the blocked-target consumed-link CLI regression passes alone. Full just check passes all checks except the two pre-existing percent-listen tests tracked by bob-cli-6m (recorded as a PROPOSED FOLLOW-UP); 1,405 CLI tests and 2,451 unit tests pass. epic-symbols reported no remaining entries.

## Dependencies

- **Blocks:** [bob-cli-6u.18.7.5](bob-cli-6u.18.7.5.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.2.md) | [bob-cli-6u.18.7.2](bob-cli-6u.18.7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e45c3ab`](https://github.com/bobs-org/bob-cli/commit/e45c3ab0290d91e3358ebad5194f55b2d0d04782) | fix(capture): correct consumed link reporting and status handling | [bob-cli-6u.18.7.2](bob-cli-6u.18.7.2.md) | 2026-10-12 20:58:50 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.7.2--1][1] | Need phase scope, design file, and prior phase notes for verification and closure | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.2.md

<!-- sase:referenced-by:end -->
