# Bead: bob-cli-42.2 — Plan card actions and frozen priority previews

[Bead Pages](../README.md) / [bob-cli-42](README.md) / bob-cli-42.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.05.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.05.linker.w0.md) · **Assignee:** `bob-cli-42.2` · **Size:** medium
**Created:** 2026-10-03 16:27:19 EDT · **Closed:** 2026-10-03 16:58:59 EDT
**Plan:** [202610/ctrl\_shift\_p\_task\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_p_task_card.md)

## Description

card-model: add pure context-aware card and key models with independent per-target priority previews, availability reasons, and table tests.

## Notes

[2026-10-03T20:58:59Z · bob-cli-42.2] Implemented the pure Task Card model, typed key intents, independent frozen priority previews, availability reasons, and single/counted/linked scope metadata. Verified 79 focused Task Card, roll/decay, and stamp tests pass; npm run validate passes; git diff --check and node syntax checks pass. Synced bob-navigation-hotkeys from the linked source checkout and confirmed installed main.js and manifest.json match. epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-42.1](bob-cli-42.1.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-42.3](bob-cli-42.3.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-42.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-42.2/README.md) | [bob-cli-42.2](bob-cli-42.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8813271`](https://github.com/bobs-org/bob-plugins/commit/8813271e51424db76222f2e5db787b50446e9fd9) | feat(navigation-hotkeys): add Task Card planning model | [bob-cli-42.2](bob-cli-42.2.md) | 2026-10-03 17:01:51 EDT |
