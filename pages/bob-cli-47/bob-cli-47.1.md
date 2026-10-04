# Bead: bob-cli-47.1 — Split task-status-cycler main.js and establish the plugin source build

[Bead Pages](../README.md) / [bob-cli-47](README.md) / bob-cli-47.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4z.md) · **Assignee:** `bob-cli-47.1` · **Size:** large
**Created:** 2026-10-04 07:13:46 EDT · **Closed:** 2026-10-04 07:42:34 EDT
**Plan:** [202610/split\_largest\_bob\_plugins\_js\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_bob_plugins_js_files.md)

## Description

split-task-status-cycler: pilot the src/ fragment build, staleness check, and parity check on the smallest target plugin. Document the new contract and split plugins/task-status-cycler/main.js into fragments plus plugin-class mixins.

## Notes

[2026-10-04T11:38:23Z · bob-cli-47.1] PROPOSED FOLLOW-UP: Stabilize the navigation dependency stage ranker timing budget. The clean bob-plugins base c3349aae7fa34c34aaecd2a9c85097fef5b5d762 failed the full suite twice at scripts/test-navigation-dependencies-stage.cjs:1051 (20.41 ms and 16.45 ms against a 16 ms limit); the implemented worktree passes all 1754 tests and that same benchmark at 9.67 ms. This timing-sensitive check is unrelated to the cycler split; no separate tracking bead is known.

[2026-10-04T11:42:34Z · bob-cli-47.1] Implemented the ordered 21-fragment build for task-status-cycler. npm run build produced a deterministic unchanged second build; build:check and validate passed. Parity against c3349aae7fa34c34aaecd2a9c85097fef5b5d762 passed for 183 helpers and 187 own prototype methods. npm test passed 1754/1754, including all 179 cycler tests. All source fragments are at or below 1000 lines (largest 921). bob plugins sync completed and bob plugins list reports task-status-cycler 1.23.1 synced.

## Dependencies

- **Blocks:** [bob-cli-47.2](bob-cli-47.2.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-47.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-47.1.md) | [bob-cli-47.1](bob-cli-47.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6f8aca0`](https://github.com/bobs-org/bob-plugins/commit/6f8aca0beae21e66922ae61a6d865d642d056803) | feat(plugins): add deterministic fragment build and split task status cycler | [bob-cli-47.1](bob-cli-47.1.md) | 2026-10-04 07:43:42 EDT |
