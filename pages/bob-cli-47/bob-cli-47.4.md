# Bead: bob-cli-47.4 — Split scripts/test-navigation-hotkeys.cjs

[Bead Pages](../README.md) / [bob-cli-47](README.md) / bob-cli-47.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4z.md) · **Assignee:** `bob-cli-47.4` · **Size:** large
**Created:** 2026-10-04 07:13:46 EDT · **Closed:** 2026-10-04 09:46:14 EDT
**Plan:** [202610/split\_largest\_bob\_plugins\_js\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_bob_plugins_js_files.md)

## Description

split-navigation-hotkeys-tests: move the shared preamble and file-wide helpers into a harness module, and split the 500 tests into per-area test files listed in package.json. The same 500 names must still pass.

## Notes

[2026-10-04T13:46:14Z · bob-cli-47.4] Split the 500 navigation hotkeys tests into 33 per-area files with a shared harness. Verified identical test names, all tests pass, npm test, npm run validate, plugin sync, and no remaining epic symbols.

## Dependencies

- **Depends on:** [bob-cli-47.3](bob-cli-47.3.md) ✓ · ⧖ 2026-10-04
- **Blocks:** [bob-cli-47.5](bob-cli-47.5.md) ◐ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-47.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-47.4.md) | [bob-cli-47.4](bob-cli-47.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5d074dc`](https://github.com/bobs-org/bob-plugins/commit/5d074dc340173f94cb9353f11a0241d9a8717af5) | refactor(test): split navigation hotkeys suite | [bob-cli-47.4](bob-cli-47.4.md) | 2026-10-04 09:47:50 EDT |
