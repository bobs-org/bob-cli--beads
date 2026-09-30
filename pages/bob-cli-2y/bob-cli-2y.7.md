# Bead: bob-cli-2y.7 — bob-ledger-tools api v2 with a synchronous Today, lane budgets, and query refresh

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.7` · **Size:** medium
**Created:** 2026-09-30 16:42:00 EDT · **Closed:** 2026-09-30 17:46:34 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

ledger-today-api: synchronous Today cache with midnight rollover and the Tasks reload event, api v2 (isToday, todayRank, nextBudget, pendingBudget), lane chips in the bob-plan block, JS tests on the shared vectors.

## Notes

[2026-09-30T21:46:34Z · bob-cli-2y.7] ledger-today-api done in bob-plugins (uncommitted working tree): api v2 frozen {version:2,caps,planBudget,todayKeys,isToday,todayRank,nextBudget,pendingBudget}, nowBudget/hasNowTag/maxNow removed; synchronous Today cache (layout-ready/resolved/changed with event content/create-delete-rename/midnight rollover) firing pinned obsidian-tasks-plugin:reload-open-search-results only on key change (verified against installed Tasks bundle: TasksEvents subscription + blockLink ' ^id' format); computeTodayLinks/resolveTodayKeys mirror list_queued_links; lane chips + next/pending_cap_exceeded lints; legacy max_now loads. Verified: new scripts/test-ledger-tools-today.cjs (T1-T9 verbatim) + updated plan-budget tests, npm test 870 pass, validate 6/6, manifest 1.7.0, deployed via bob plugins sync (backup 20260930-214611). No epic-symbol entries remain.

## Dependencies

- **Blocks:** [bob-cli-2y.10](bob-cli-2y.10.md) ◐ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.5](bob-cli-2y.5.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2y.9](bob-cli-2y.9.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.7/README.md) | [bob-cli-2y.7](bob-cli-2y.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3297b25`](https://github.com/bobs-org/bob-plugins/commit/3297b2559f81402931abf7896d8978f3efd3b4ce) | feat(ledger): bob-ledger-tools api v2 with synchronous Today, lane budgets, and query refresh | [bob-cli-2y.7](bob-cli-2y.7.md) | 2026-09-30 17:48:37 EDT |
