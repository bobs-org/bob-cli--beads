# Bead: bob-cli-47.3 — Split bob-navigation-hotkeys main.js

[Bead Pages](../README.md) / [bob-cli-47](README.md) / bob-cli-47.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4z.md) · **Assignee:** `bob-cli-47.3` · **Size:** large
**Created:** 2026-10-04 07:13:46 EDT · **Closed:** 2026-10-04 08:54:23 EDT
**Plan:** [202610/split\_largest\_bob\_plugins\_js\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_bob_plugins_js_files.md)

## Description

split-navigation-hotkeys: apply the build contract to the 52k-line plugins/bob-navigation-hotkeys/main.js. This includes mixin splits of both the plugin class and the 6.4k-line BulletPropertyPickerModal, with its super calls and duplicate onClose.

## Notes

[2026-10-04T12:36:17Z · bob-cli-47.3] PROPOSED FOLLOW-UP: BulletPropertyPickerModal's first onClose (task-card class cleanup) is dead; the later onClose wins and never removes bob-task-card-* — preserved by the split

[2026-10-04T12:50:38Z · bob-cli-47.3] PROPOSED FOLLOW-UP: check-split-parity --split-helper still compares the whole split helper class source through prototype.constructor. Navigation parity reports only that mismatch even though the constructor source bytes are identical and all other helpers and methods compare equal; the checker support needs a later update, outside this phase's explicit scope.

[2026-10-04T12:50:43Z · bob-cli-47.3] PROPOSED FOLLOW-UP: scripts/test-navigation-dependencies-stage.cjs has a timing-sensitive 16 ms threshold: clean-base npm test passed; two post-split full-suite runs failed at 18.23 ms and 26.93 ms, while a focused rerun passed at 7.48 ms.

[2026-10-04T12:54:23Z · bob-cli-47.3] Split into 70 ordered fragments (max 950 lines); installed 11 FilteredPickerModal mixins and 19 plugin mixins, preserving the live onClose and constructor bytes. Build, deterministic second build, build:check, validate, syntax, and line-limit checks passed. Official parity reports only the split helper class-source mismatch; split-aware parity otherwise confirms 574 helpers and 308 methods. Clean-base npm test passed; post-split full runs hit the known 16 ms ranker timing threshold twice, while the focused stage suite passed. Synced 2.2.1; bob plugins list confirms synced.

[2026-10-04T13:05:24Z · bob-cli-47.3] PROPOSED FOLLOW-UP: check-split-parity.mjs --split-helper BulletPropertyPickerModal compares String(class) on prototype.constructor, so the legitimate split class wrapper differs even though all helper methods and the copied constructor bytes match; the plan forbids changing that checker, so its split-helper comparison needs a follow-up fix.

[2026-10-04T13:05:30Z · bob-cli-47.3] PROPOSED FOLLOW-UP: scripts/test-navigation-dependencies-stage.cjs timing test for filtering 1,000 tasks failed twice in the full suite at 26.70 ms and 35.06 ms against 16 ms, while an isolated rerun passed; matches the previously observed timing flake.

[2026-10-04T13:06:42Z · bob-cli-47.3] Navigation hotkeys split complete: audited 574 helpers and 308 plugin methods against 56806594; the official --split-helper check reports only the expected split-class constructor-source mismatch (constructor bytes and all own methods match). 70 fragments, maximum 950 lines, all parse. Build twice unchanged, build:check and validate pass. npm test reports 1753/1754 because the known 1,000-task timing assertion failed twice in full-suite runs; isolated rerun passed. git diff --check clean; bob-navigation-hotkeys 2.2.1 is synced.

## Dependencies

- **Depends on:** [bob-cli-47.2](bob-cli-47.2.md) ✓ · ⧖ 2026-10-04
- **Blocks:** [bob-cli-47.4](bob-cli-47.4.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-47.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-47.3.md) | [bob-cli-47.3](bob-cli-47.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c1762af`](https://github.com/bobs-org/bob-plugins/commit/c1762af3b757579d700dceb010e63a36bf8537b0) | refactor(bob-navigation-hotkeys): split navigation source into fragments | [bob-cli-47.3](bob-cli-47.3.md) | 2026-10-04 09:08:16 EDT |
