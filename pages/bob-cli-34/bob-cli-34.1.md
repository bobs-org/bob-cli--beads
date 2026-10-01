# Bead: bob-cli-34.1 — Navigation Hotkeys: decay config, Schedule Log roll streak, and pure recommendation planner

[Bead Pages](../README.md) / [bob-cli-34](README.md) / bob-cli-34.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0um](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0um.md) · **Assignee:** `bob-cli-34.1` · **Size:** medium
**Created:** 2026-09-30 23:56:47 EDT · **Closed:** 2026-10-01 00:06:05 EDT
**Plan:** [202609/priority\_roll\_decay.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/priority_roll_decay.md)

## Description

decay-core: add the `decay`/`rolls` config grammar, the roll-streak reader with its entry classification, the date roll that avoids the current date, the recommendation planner, the decay and cancel reason formatters, and the preview model. Includes a new conformance test file. No UI changes.

## Notes

[2026-10-01T04:06:05Z · bob-cli-34.1] decay-core done in bob-plugins: decay/rolls config grammar with normalizePriorityDecayConfig/getPriorityLevelRollLimit, classifyScheduleLogRollReason + count/getPriorityRollStreak, rollPriorityRecommendationDate avoiding current date, planPriorityRollRecommendation, formatPriorityDecayScheduleReason/formatPriorityDecayCancelReason, buildPriorityRollPreviewModel; all 15 conformance vectors covered in scripts/test-navigation-roll-decay.cjs (13 tests pass) registered in package.json test; full suite 958 pass 0 fail; bob plugins sync deployed; no epic-symbol leftovers; no UI changes

## Dependencies

- **Blocks:** [bob-cli-34.2](bob-cli-34.2.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-34.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-34.1/README.md) | [bob-cli-34.1](bob-cli-34.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@09d9578`](https://github.com/bobs-org/bob-plugins/commit/09d9578916419c73165e0ac9471fc0b83398ab67) | feat(nav): add priority decay core with roll streak and preview model | [bob-cli-34.1](bob-cli-34.1.md) | 2026-10-01 00:07:57 EDT |
