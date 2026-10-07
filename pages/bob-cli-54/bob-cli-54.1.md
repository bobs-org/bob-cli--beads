# Bead: bob-cli-54.1 — Pomodoro target core (pure model and explicit-target planner)

[Bead Pages](../README.md) / [bob-cli-54](README.md) / bob-cli-54.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5h](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.5h/README.md) · **Assignee:** `bob-cli-54.1` · **Size:** medium
**Created:** 2026-10-07 09:22:15 EDT · **Closed:** 2026-10-07 09:32:28 EDT
**Plan:** [202610/ctrl\_shift\_enter\_pomodoro\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_enter_pomodoro_picker.md)

## Description

core: add pure block-id-prompt helpers for capture-parity Pomodoro names, today's open-entry model, ranked picker rows, the create intent, and an explicit-target link planner (existing or new named entry), with unit tests; no behavior change yet.

## Notes

[2026-10-07T13:32:28Z · bob-cli-54.1] Core done: 075-pomodoro-link-targets.js (949 lines) with capture-parity names, entry model, ranked rows, create intent, explicit-target planner; planPomodoroLinkInsertion delegates on target (target-less path unchanged). Verified: npm run build ok, npm test 2065/2065 pass (25 new), npm run validate 6/6, bob plugins sync ok. No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-54.2](bob-cli-54.2.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-54.3](bob-cli-54.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-54.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-54.1/README.md) | [bob-cli-54.1](bob-cli-54.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@881b9ad`](https://github.com/bobs-org/bob-plugins/commit/881b9adb5f6cfb8760fbc68b6459aab11d01e301) | feat(block-id-prompt): add explicit pomodoro link target planning | [bob-cli-54.1](bob-cli-54.1.md) | 2026-10-07 09:33:48 EDT |
