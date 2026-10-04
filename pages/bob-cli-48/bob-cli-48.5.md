# Bead: bob-cli-48.5 — Navigation walk support, complete-and-advance, and text-first cursor identity

[Bead Pages](../README.md) / [bob-cli-48](README.md) / bob-cli-48.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.07.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.07.linker.w1.md) · **Assignee:** `bob-cli-48.5` · **Size:** medium
**Created:** 2026-10-04 09:05:23 EDT · **Closed:** 2026-10-04 11:02:14 EDT
**Plan:** [202610/gtd\_pre\_post\_review\_tiers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gtd_pre_post_review_tiers.md)

## Description

nav: teach navigation-hotkeys the PRE/POST tiers and notices, route Alt+F / Alt+Shift+F on checklist rows to cycler completion, skip them in counted and Task Link batches, match the cursor by text first, and drop a previous-day walk anchor.

## Notes

[2026-10-04T15:01:59Z · bob-cli-48.5] PROPOSED FOLLOW-UP: Corroborate bob-cli-3w — scripts/test-navigation-dependencies-stage.cjs:1051 (stage ranker 16 ms) failed in full npm test at 19.43 ms and passed isolated on the clean tree at 9.66 ms

[2026-10-04T15:02:14Z · bob-cli-48.5] bob-navigation-hotkeys 2.3.0: PRE/POST walk notices and gates, text-first cursor identity, day-scoped reviewAnchor, Alt+F/Alt+Shift+F complete via cycler v2, counted and Task Link batches skip checklist rows. Verified fragments <=1000, 85 freshness+checklist tests, npm run validate 6/6, epic-symbols empty. Full npm test 1789 pass / 1 fail is the known bob-cli-3w ranker flake (19.43 ms vs 16 ms; isolated clean tree 9.66 ms).

## Dependencies

- **Depends on:** [bob-cli-48.2](bob-cli-48.2.md) ✓ · ⧖ 2026-10-04
- **Depends on:** [bob-cli-48.4](bob-cli-48.4.md) ✓ · ⧖ 2026-10-04
- **Blocks:** [bob-cli-48.6](bob-cli-48.6.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-48.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-48.5/README.md) | [bob-cli-48.5](bob-cli-48.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@252ec0e`](https://github.com/bobs-org/bob-plugins/commit/252ec0ecbd59fd604cbfa0f76b88e60219d9cc91) | feat(navigation): teach PRE/POST review walk complete-and-advance | [bob-cli-48.5](bob-cli-48.5.md) | 2026-10-04 11:08:45 EDT |
