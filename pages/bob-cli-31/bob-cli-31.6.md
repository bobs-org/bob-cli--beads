# Bead: bob-cli-31.6 — Review keys in Bob Navigation Hotkeys

[Bead Pages](../README.md) / [bob-cli-31](README.md) / bob-cli-31.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.v.linker.w0.md) · **Assignee:** `bob-cli-31.6` · **Size:** medium
**Created:** 2026-09-30 19:32:06 EDT · **Closed:** 2026-09-30 22:35:23 EDT
**Plan:** [202609/task\_freshness\_review.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_freshness_review.md)

## Description

nav-review: vault-wide next/previous due-task jumps (Ctrl+Alt+J/K, and the commands behind ]s / [s), Alt+F refresh with no other change, and Alt+Shift+F refresh-and-advance, including counted and Task Link modes.

## Notes

[2026-10-01T02:34:17Z · bob-cli-31.6] PROPOSED FOLLOW-UP: Ctrl+Alt+J/K jumps have no Vim-normal-mode capture fallback (only Alt+F/Alt+Shift+F got one per spec); verify whether CodeMirror Vim swallows Ctrl+Alt chords and add a fallback if so

[2026-10-01T02:35:23Z · bob-cli-31.6] nav-review landed in bob-plugins: 4 commands (jump-to-next/prev-due-task on Ctrl+Alt+J/K, refresh-task-freshness on Alt+F, refresh-and-advance on Alt+Shift+F) with api-v3 guard, vault-wide queue jumps with wrap/empty notices and leaf-reuse landing, counted+Task-Link Alt+F writes via api.freshness.stampLine only, Vim capture fallback for Alt chords. Verified: new scripts/test-navigation-freshness.cjs 21/21 pass, full npm test 915/915 pass, npm run validate 6/6 valid, manifest bumped to 1.43.0, README row updated, bob plugins sync deployed 2 files.

## Dependencies

- **Depends on:** [bob-cli-31.5](bob-cli-31.5.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.7](bob-cli-31.7.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.9](bob-cli-31.9.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-31.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-31.6/README.md) | [bob-cli-31.6](bob-cli-31.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3fc6a5f`](https://github.com/bobs-org/bob-plugins/commit/3fc6a5f85a837904de2a02d23bb01557fffa0121) | feat(nav): review keys for task freshness (bob-cli-31.6) | [bob-cli-31.6](bob-cli-31.6.md) | 2026-09-30 22:37:00 EDT |
