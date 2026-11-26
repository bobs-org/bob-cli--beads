# Bead: bob-cli-q5.4.1 — Snoozed task plugin plumbing

[Bead Pages](../README.md) / [bob-cli-q5.4](bob-cli-q5.4.md) / bob-cli-q5.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.md) · **Assignee:** `bob-cli-q5.4.1.land`
**Created:** 2026-11-26 07:52:01 EST · **Closed:** 2026-11-26 15:12:04 EST
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

[2026-11-26T19:52:53Z · bob-cli-q5.4.1.land] SECOND LAND REVIEW (bob-cli-q5.4.1.land, 2026-11-26): Follow-up triage. The child PROPOSED FOLLOW-UP entries (q5.4.1.1 #1/#3, q5.4.1.2 #3/#4, q5.4.1.3 #1) were all triaged in note #1 and the outcomes stand. (1) The frontmatter-takeover e2e self-test stays DECLINED: npm test on bob-plugins f6458cb0 passes 9969 with 4 skipped and 0 failed. (2) bob-emoji tracking stays a DUPLICATE of bob-cli-cd, which is still ready. (3) The MEET heuristic was fixed by landing tale d7875aac with structural Event detection. (4) Cycler SP14 was mostly fixed by d7875aac. Nav navNoteScopeFlags stays bob-cli-ql, which is still ready. The landing-tale agents (land--code, --1, --2) recorded no new proposals, and this review found no new distinct follow-ups. The land--1 monitor shell-quoting error was an agent command bug, not product work, so it was not filed. Remaining epic work: the main Ctrl+Enter successor recovery (137-plugin-successor-project.js planFirst -> planSuccessors) never passes isSnoozedToday. Reproduced with finalizeClosedTasks: a snoozed Blocked dependent still gets [unblocked:: today]. That is the first tale's SP14 requirement, unmet on the most common path. It is planned as tale plan sase_plan_snooze_plumbing_sp14_closeout, and that tale also performs this epic's and phase bob-cli-q5.4's closeout. Deploy blocker cleared: bob plugins sync --dry-run against origin/master f6458cb0 shows 0 to copy and 34 unchanged. Drift since e36ddc68 (notebook/prose/copy-card/bank/drawers; bob-cli 3659edc0/59037b23 wake-notice fields) has no snooze-contract impact on the plugins.

[2026-11-26T20:12:04Z · bob-cli-q5.4.1.land] Closeout verified: all five child phases are closed. First land review verified phase integration, npm test 9,902 passed / 0 failed (4 skipped), and the live dash.md exclusions. Landing tale d7875aac added decoder support for destination.name null and slim deferred reports, structural Event detection, SP14 in references/project-resident/offer-close, and gesture plus Snoozed boundary regressions. Second land review found no snooze-contract impact from drift and npm test on f6458cb0 passed 9,969 / 0 failed (4 skipped). This tale threads isSnoozedToday through planFirst and adds snoozed, ordinary, and same-note public Done regressions. Gates: npm run build, focused suites 99/99, npm run validate (12/12 plugins), npm test exit 0 (full unit and perf suites), docs:check 447 passed / 1 expected skip. bob plugins sync with the opened linked checkout copied task-status-cycler/main.js; all other plugin rows unchanged, 33 rows unchanged total.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.1.land.md) | [bob-cli-q5.4.1](bob-cli-q5.4.1.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d7875aa`](https://github.com/bobs-org/bob-plugins/commit/d7875aac6d1844cdb60fdc35a25a0c2e2d6e6a65) | feat(snooze): land plugin plumbing behavior | [bob-cli-q5.4.1](bob-cli-q5.4.1.md) | 2026-11-26 13:38:14 EST |
| bob-plugins | [`bob-plugins@0bae838`](https://github.com/bobs-org/bob-plugins/commit/0bae8384b586811b8a5a34afd8f3e32f58df7442) | fix(task-status-cycler): preserve snooze during Done recovery | [bob-cli-q5.4.1](bob-cli-q5.4.1.md) | 2026-11-26 15:14:58 EST |
| bob-cli--plans | [`bob-cli--plans@69ff419`](https://github.com/bobs-org/bob-cli--plans/commit/69ff419e5536eebe0ae2ec76a62674a43728ea02) | docs(plan): mark snooze plugin epic complete | [bob-cli-q5.4.1](bob-cli-q5.4.1.md) | 2026-11-26 15:17:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.4.1.3][1] | Need parent epic plan and decisions | 1 |
| read-by | [agent:bob-cli-q5.4.1.4--1][2] | Need the epic's governing decisions and phase gates | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.1.4.md

<!-- sase:referenced-by:end -->
