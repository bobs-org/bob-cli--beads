# Bead: bob-cli-4f.2 — Split the block-id-prompt test suite

[Bead Pages](../README.md) / [bob-cli-4f](README.md) / bob-cli-4f.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.54](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.54.md) · **Assignee:** `bob-cli-4f.2` · **Size:** large
**Created:** 2026-10-04 21:42:18 EDT · **Closed:** 2026-10-04 22:24:55 EDT
**Plan:** [202610/split\_largest\_bob\_plugins\_js\_files\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_bob_plugins_js_files_1.md)

## Description

block-id-prompt-tests: split the 4945-line test-block-id-prompt.cjs into a shared harness and per-area test files of at most 1000 lines each, losing no tests; the agent plans the final split.

## Notes

[2026-10-05T02:22:46Z · bob-cli-4f.2] PROPOSED FOLLOW-UP: Stage ranker 16 ms flake (bob-cli-3w) — first full npm test after the split failed scripts/test-navigation-dependencies-stage.cjs:1051 at 16.62 ms; isolated file passed 61/61 on the split tree and on clean base 03f0c17; clean-base npm test passed 1809/1809; retry on the split tree passed 1809/1809.

[2026-10-05T02:24:55Z · bob-cli-4f.2] Split scripts/test-block-id-prompt.cjs into scripts/block-id-prompt-harness.cjs plus ten per-area files. 179/179 original tests preserved byte-for-byte (order-independent digest 9137bf6de9ac5aa6755eefc5304c2ad85ac91da0f7a28e114f80a8282ac1f3d5) at pre-split commit 03f0c177989871805561e84cd16f7310cdbed32f. Focused `node --test scripts/test-block-id-prompt-*.cjs` passed 179/179 with 0 fail/skip/cancel. Independent file counts: dependencies 10, markers 8, pomodoro-context 9, target-update 35, pomodoro-insertion 28, work-log 10, pomodoro-link-runtime 23, pomodoro-unlink-runtime 11, task-link-deletion 27, plan-budget-and-freshness 18 (sum 179). npm run build:check passed; npm test passed 1809/1809 on retry (first full run hit the known bob-cli-3w 16.62ms ranker flake at test-navigation-dependencies-stage.cjs:1051; isolated 61/61 and clean-base npm test 1809/1809); npm run validate passed 6/6. File sizes: harness 273, largest area target-update 821, README 354, package.json 14; original monolith deleted; only this phase's files changed. bob plugins sync --no-pull -r <workspace bob-plugins> -p block-id-prompt: up to date (plugin source unchanged). epic-symbols bob-cli-4f.2: none.

## Dependencies

- **Depends on:** [bob-cli-4f.1](bob-cli-4f.1.md) ✓ · ⧖ 2026-10-04
- **Blocks:** [bob-cli-4f.3](bob-cli-4f.3.md) ◐ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4f.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-4f.2.md) | [bob-cli-4f.2](bob-cli-4f.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2486da9`](https://github.com/bobs-org/bob-plugins/commit/2486da9c17b3fdade1a954ecf31e2e88acef5751) | refactor(test): split block-id-prompt suite | [bob-cli-4f.2](bob-cli-4f.2.md) | 2026-10-04 22:26:13 EDT |
