# Bead: bob-cli-2o.7 — bob-plugins: Bob Ledger Tools plan view, \`bob-plan\` block, and public API

[Bead Pages](../README.md) / [bob-cli-2o](README.md) / bob-cli-2o.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.7` · **Size:** medium
**Created:** 2026-09-29 18:09:56 EDT · **Closed:** 2026-09-29 19:13:27 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

ledger-plan-view: mirror the plan-budget definition in bob-ledger-tools; render a live ```` ```bob-plan ```` block (PLAN and NOW chips, today's themes with the highlight starred, and lint lines); and expose a versioned `api` (caps, planBudget, nowBudget) for the dash and the other plugins.

## Notes

[2026-09-29T23:12:56Z · bob-cli-2o.7] PROPOSED FOLLOW-UP: vault on apollo was missing .obsidian/plugins/bob-ledger-tools (and also lacks bob-project-tasks, bob-vim-surround, task-status-cycler); this phase synced ledger-tools, rollout should confirm the full set

[2026-09-29T23:13:27Z · bob-cli-2o.7] ledger-plan-view done in bob-plugins: computePlanBudget/parsePlanCaps/hasNowTag/nowBudgetFromTasks mirror docs/plan.md (all 7 conformance vectors pass), live bob-plan block with PLAN/NOW chips + themes + lints and styles.css, versioned api {version:1,caps,planBudget,nowBudget} documented in README, manifest 1.4.0->1.5.0, new scripts/test-ledger-tools-plan-budget.cjs (23 tests) registered; npm test 781 pass, validate 6/6, deployed via bob plugins sync -p bob-ledger-tools (vault files match). No epic-symbols. Changes left uncommitted in bob-plugins working tree for the land agent.

## Dependencies

- **Depends on:** [bob-cli-2o.1](bob-cli-2o.1.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.10](bob-cli-2o.10.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.13](bob-cli-2o.13.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.9](bob-cli-2o.9.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.7/README.md) | [bob-cli-2o.7](bob-cli-2o.7.md) | 0 |
