# Bead: bob-cli-q5.4.1 — Snoozed task plugin plumbing

[Bead Pages](../README.md) / [bob-cli-q5.4](bob-cli-q5.4.md) / bob-cli-q5.4.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.md) · **Assignee:** `bob-cli-q5.4.1.land`
**Created:** 2026-11-26 07:52:01 EST
**Plan:** [202611/snooze\_plugin\_plumbing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_plugin_plumbing.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/snooze_plugin_plumbing.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-ql][2] | The snooze plugin epic added isSnoozedToday to ledger markUnblockedLine (SP14) and its landing tale threads planned-today through task-status-cycler recovery; nav is the remaining plugin |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_plugin_plumbing.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ql/README.md

<!-- sase:links:end -->

## Description

Complete bob-cli-q5.4 so Obsidian excludes snoozed tasks from review and dashboard lanes, preserves gesture cleanup and notes, and requests due wakes through bob with one notification fallback.

## Notes

[2026-11-26T17:12:58Z · bob-cli-q5.4.1.land] LAND TRIAGE (bob-cli-q5.4.1.land, 2026-11-26): (1) bob-cli-q5.4.1.1 #1 and bob-cli-q5.4.1.3 #1, frontmatter-takeover e2e self-test failure: DECLINED, no longer reproduces. Full npm test on the integrated tree (bob-plugins e36ddc68) passes 9902/9906 with 4 skipped and 0 failed; bob-cli-qi.3's 8e6a5a61 rewrote that harness. (2) bob-cli-q5.4.1.1 #3, bob-emoji tracked in vault Git: DUPLICATE, +1 recorded on existing bob-cli-cd (ready, now +3), still reproduces. (3) bob-cli-q5.4.1.2 #3, MEET-substring Event heuristic (snoozedIsEventTask): KEPT AS EPIC WORK, caused by this epic. The landing tale replaces it with the structural Rust event_task_at rule (canonical daily note plus ## Events section). (4) bob-cli-q5.4.1.2 #4, Today-only gesture predicates: task-status-cycler projectRecoveryTaskIsToday and the successor hasLiveLink isToday scope are KEPT AS EPIC WORK (SP14 parity flagged for later phases of this epic, never done). Nav 195-rotten-keep freshnessTargetIsToday is DECLINED: snoozed rows carry no review tier, so the rottenKeepIsDueRung gate already leaves their keeps uncounted. Nav navNoteScopeFlags never passing Today or snoozed membership predates this epic and is filed as bob-cli-ql (bug, small, ready). (5) Discovered: bob snooze wake deferred report omits documented fields. Caused by bob-cli-q5.1.1.3, so it was recorded as a DISCOVERED ISSUE note on active epic bob-cli-q5. Remaining epic work found by verification: the waker decoder rejects real CLI reports (destination.name null for an untyped wake into an unnamed Pomodoro, reproduced with bob 0.6.0 in an isolated vault; slim deferred envelope), plus missing phase-3 and phase-4 public-gesture regression tests. Planned as a landing tale.

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.4.1.3][1] | Need parent epic plan and decisions | 1 |
| read-by | [agent:bob-cli-q5.4.1.4--1][2] | Need the epic's governing decisions and phase gates | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.1.4.md

<!-- sase:referenced-by:end -->
