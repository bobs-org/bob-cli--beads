# Bead: bob-cli-q5.4.1.2 — Snoozed cache and planned-today exclusions

[Bead Pages](../README.md) / [bob-cli-q5.4.1](bob-cli-q5.4.1.md) / bob-cli-q5.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.md) · **Assignee:** `bob-cli-q5.4.1.2` · **Size:** medium
**Created:** 2026-11-26 07:52:01 EST · **Closed:** 2026-11-26 09:08:22 EST
**Plan:** [202611/snooze\_plugin\_plumbing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_plugin_plumbing.md)

## Description

planned-today: build snoozedCache and the public isSnoozedToday/isPlannedToday/snoozed.rows APIs; wire target-aware invalidation, day and minute refreshes, freshness, lane walks and dashboard exclusions, mirror the planned-today vectors, and make the approved minimal live dash.md query/count edit.

## Notes

[2026-11-26T14:07:45Z · bob-cli-q5.4.1.2] Phase evidence: snoozedCache + planned-today exclusions implemented in bob-plugins (ledger-tools). New: src/290a-snoozed-today-cache.js (cache rebuild/invalidation/minute+rollover APIs), src/340a-plan-dashboard-section.js (split for 1000-line limit), src/381-snoozed-cache-exports.js, scripts/fixtures/walks/planned-today.json (byte-identical to bob-cli), scripts/test-ledger-tools-planned-today.cjs (14 tests). Edited: 170 lifecycle+api (isSnoozedToday/isPlannedToday/snoozed v1 namespace, event wiring, interval, teardown), 180 (budgets/laneWalk memo+predicate, planBlock paint), 070 (section+READY exclusions, snoozed tallies, skipIndices), 071 (queue exclusion, snoozed tally), 100 (walkScope/inScope/checklist/recurring/decide), 090 (decide param), 160 (row.isSnoozedToday), 230 (context+stamp), 080 (SP14 markUnblocked flag), 340 (isSnoozed plumbing), 290 (1-line paint call), 310+fragments.json, package.json test list. SP1-SP12/SP15/SP17 parity verified (membership, tiers, next_wake_at, history woke_at, whole-lane meters unchanged); SP13 wake-swap and SP16 excess simulated; SP14 unit-covered.

[2026-11-26T14:07:55Z · bob-cli-q5.4.1.2] Verification: npm run build ok; npm run validate ok (12/12 plugins); npm run docs:check ok (447 passed); test:unit 9887 pass / 1 fail = test-obsidian-frontmatter-takeover-e2e self-test, reproduced on clean HEAD worktree (17/18 there) so pre-existing/environmental, unrelated (property-editor modal DOM); test:perf 26/26 ok. Targeted suites all green: today, dashboard-parity, lane-walk, navigation-lane-walk, walker-footer, freshness (queue/states/namespace/review-model/recurring/placement/mark), ready-badge, plan-budget, work-badge-tone, snooze vectors+twin-copies, planned-today (14/14). Deployed via bob plugins sync (backups 20261126-090548, 20261126-090735); vault main.js carries the APIs. Live dash.md edit committed by vault-sync as bc6607cb8+6bae272e5 (pushed, local==remote); PENDING/NEXT/READY queries and DataviewJS counts exclude isSnoozedToday beside isToday, TODAY query unchanged; count/query parity holds (section counts vs filtered queries, whole-lane meters untouched).

[2026-11-26T14:08:00Z · bob-cli-q5.4.1.2] PROPOSED FOLLOW-UP: snoozed fact-building detects Event tasks with a MEET-substring heuristic (snoozedIsEventTask); a precise event_task_at note scan would need async target-note reads. snooze add already refuses Event targets so only hand-authored rows are affected.

[2026-11-26T14:08:04Z · bob-cli-q5.4.1.2] PROPOSED FOLLOW-UP: gesture callers outside this phase still use Today-only predicates (task-status-cycler 088 projectRecoveryTaskIsToday feeding markUnblockedLine scope; navigation 195-rotten-keep freshnessTargetIsToday). The pure markUnblockedLine and all review/lane/dashboard paths already honor isSnoozedToday; threading the flag through those gesture callers belongs to navigation-cleanup / link-and-complete.

[2026-11-26T14:08:22Z · bob-cli-q5.4.1.2] SP parity + gates green: snoozedCache with isSnoozedToday/isPlannedToday/snoozed.rows APIs, target-aware invalidation and minute/rollover refresh, freshness/recurring/decide/checklist/placement exclusions, lane-walk and dashboard section exclusions with whole-lane meters unchanged, live dash.md query/count edit synced and pushed, deployed bundle carries the APIs. Only failure (frontmatter-takeover e2e) reproduces on clean HEAD. Two PROPOSED FOLLOW-UP notes recorded (MEET heuristic, later-phase gesture callers).

## Dependencies

- **Depends on:** [bob-cli-q5.4.1.1](bob-cli-q5.4.1.1.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.4.1.3](bob-cli-q5.4.1.3.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4.1.2/README.md) | [bob-cli-q5.4.1.2](bob-cli-q5.4.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.4.1.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4.1.2/README.md

<!-- sase:referenced-by:end -->
