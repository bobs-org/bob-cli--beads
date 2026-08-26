# Bead: bob-cli-16.1 — Pure named-Pomodoro model, discovery, and planner

[Bead Pages](../README.md) / [bob-cli-16](README.md) / bob-cli-16.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0eb](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0eb.md) · **Assignee:** `bob-cli-16.1` · **Size:** medium
**Created:** 2026-08-26 10:04:14 EDT · **Closed:** 2026-08-26 10:57:39 EDT
**Plan:** [202608/pomodoro\_bullet\_move.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/pomodoro_bullet_move.md)

## Description

pomodoro-move-engine: add the named-Pomodoro grammar, entry/bullet-context model, sibling target discovery with count and clamping, and the pure same-file move planner to bob-navigation-hotkeys, all exported and unit tested with no UI or routing change.

## Notes

[2026-08-26T14:57:39Z · bob-cli-16.1] Added named-Pomodoro grammar (parsePomodoroEntryLine, normalizePomodoroName, formatPomodoroEntryLine), collectPomodoroEntries/findPomodoroBulletContext, sibling discovery (discoverMovablePomodoroBulletTargets), and the same-file move planner (planPomodoroBulletMove) plus supporting capture/remove/rebase helpers to plugins/bob-navigation-hotkeys/main.js, all exported via helpers. Added full unit test coverage in scripts/test-navigation-hotkeys.cjs (parsing, normalization, entry collection, context/discovery incl. grandchild promotion and clamping, move planning incl. new/existing destinations, duplicate merging, placeholder repair on both source and destination, stale-target/invalid-destination rejection, and an out-and-back round-trip). Ran code-review; fixed one real bug it found (lone-placeholder destination was blanked out when the moved block merged away as a duplicate) with a regression test. npm test (559 tests) and npm run validate (6/6 plugins) both pass in bob-plugins; git status clean and pushed. No UI, routing, manifest, or existing behavior changed. epic-symbols check: none.

## Dependencies

- **Blocks:** [bob-cli-16.2](bob-cli-16.2.md) ✓ · ⧖ 2026-08-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-16.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-16.1/README.md) | [bob-cli-16.1](bob-cli-16.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@117e33c`](https://github.com/bobs-org/bob-plugins/commit/117e33c63c45ddc46ac2d78ff214177559f90b30) | feat(bob-navigation-hotkeys): add named-Pomodoro grammar and bullet-move planner | [bob-cli-16.1](bob-cli-16.1.md) | 2026-08-26 10:56:45 EDT |
