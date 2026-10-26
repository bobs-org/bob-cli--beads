# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6 — Backlog batch 14: fresh stamps on Pomodoro ledger lines, red Mac Refs CI, the bob-cli check tool, legacy dependency readers, and relation-index publish storms

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land`
**Created:** 2026-10-26 12:58:46 EDT
**Plan:** [202610/backlog\_batch14\_ledger\_integrity\_mac\_ci\_and\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md

<!-- sase:links:end -->

## Description

Close five existing tasks by keeping freshness stamps off Pomodoro ledger lines, turning bob-mac-capture master CI green again, declaring bob-cli's named check tool, retiring the R8 legacy-child dependency readers, and coalescing relation-index publishes.

## Notes

[2026-10-26T19:05:50Z · bob-cli-ce.land] DISCOVERED ISSUE (from bob-cli-ce.land, triaging bob-cli-ce.11's PROPOSED FOLLOW-UP): phase .4's legacy-reader retirement left red tests on current masters. (1) bob-cli c4922e66: just check fails 1 lib test, native::task_status_hooks::tests::sync::fenced_column_zero_content_does_not_end_dependency_scan (panic at src/native/task_status_hooks/tests/sync.rs:233; lib 3638 passed / 1 failed). Test file last touched by 0f76d558 feat(task-deps): retire legacy child dependency readers. (2) bob-plugins 0bf8920: npm test fails 19/3832. 18 are scripts/test-dependency-line-migration.cjs cases (not ok 423-440: folds embed..., R2 adopts..., parseArgs...) that still need the removed parseDependencyLegacyChildDetails. 1 is scripts/test-navigation-dependencies-stage-performance.cjs 'stage collections reuse one snapshot per parent' at :324, 'managed-only parents never build the legacy identity map' (actual undefined, expected null), after 241ca2d feat(navigation): read dependencies from managed lines only. All other suites pass. No task bead filed because this active epic's lander owns it.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@d05f5a5`](https://github.com/bobs-org/bob-mac-capture/commit/d05f5a561d94f68b9ab70fd0630a0d9eb08eb5a0) | fix(refs): deliver the Highlights-key focus once when content is cached | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) | 2026-10-26 15:04:08 EDT |
| bob-plugins | [`bob-plugins@35bda67`](https://github.com/bobs-org/bob-plugins/commit/35bda672fce16740517a5b8b3352bdb540603f47) | test(navigation): retire the legacy dependency-line migration with the R8 readers | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) | 2026-10-26 15:12:24 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2--4][1] | Verify the assigned phase parent epic remains open after closing only its phase | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land][2] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land/README.md

<!-- sase:referenced-by:end -->
