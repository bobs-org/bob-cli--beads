# Bead: bob-cli-4f.4 — Split the navigation dependencies-stage test suite

[Bead Pages](../README.md) / [bob-cli-4f](README.md) / bob-cli-4f.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.54](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.54.md) · **Assignee:** `bob-cli-4f.4` · **Size:** large
**Created:** 2026-10-04 21:42:18 EDT · **Closed:** 2026-10-04 22:59:20 EDT
**Plan:** [202610/split\_largest\_bob\_plugins\_js\_files\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_bob_plugins_js_files_1.md)

## Description

nav-deps-stage-tests: split the 2701-line test-navigation-dependencies-stage.cjs into per-area test files of at most 1000 lines each, reusing or adding a harness and losing no tests; the agent plans the final split.

## Notes

[2026-10-05T02:59:20Z · bob-cli-4f.4] 61 tests preserved (14/10/9/7/12/9). Line counts: harness 334; ranker/pool 551; entry/view 317; writes 415; mirror/badge 314; stale guards 419; performance 504. All six pass standalone and combined (61/61); npm test passed (1,809/1,809); npm run validate passed (6/6 plugins). Hand-edited JS ranking starts test-navigation-roll-decay.cjs (2,685), then test-navigation-freshness.cjs (2,259). bob plugins sync completed.

## Dependencies

- **Depends on:** [bob-cli-4f.3](bob-cli-4f.3.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4f.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-4f.4.md) | [bob-cli-4f.4](bob-cli-4f.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b662018`](https://github.com/bobs-org/bob-plugins/commit/b66201867008d00d48c5535ca9ab2ea2ef197e12) | refactor(test): split navigation dependencies-stage suite | [bob-cli-4f.4](bob-cli-4f.4.md) | 2026-10-04 23:01:57 EDT |
