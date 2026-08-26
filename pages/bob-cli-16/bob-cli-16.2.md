# Bead: bob-cli-16.2 — Picker, routing, and commit

[Bead Pages](../README.md) / [bob-cli-16](README.md) / bob-cli-16.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0eb](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0eb.md) · **Assignee:** `bob-cli-16.2` · **Size:** medium
**Created:** 2026-08-26 10:04:14 EDT · **Closed:** 2026-08-26 11:11:48 EDT
**Plan:** [202608/pomodoro\_bullet\_move.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/pomodoro_bullet_move.md)

## Description

pomodoro-move-ui: add the destination picker rows and modal with typed create-new-Pomodoro support, route `Ctrl+Shift+M` to the Pomodoro move when the cursor is on a sub-bullet, and commit the planned move as one guarded editor transaction with a reporting notice.

## Notes

[2026-08-26T15:11:48Z · bob-cli-16.2] Implemented Pomodoro bullet move picker/routing/commit path in bob-plugins; verified npm test and npm run validate pass; epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-16.1](bob-cli-16.1.md) ✓ · ⧖ 2026-08-26
- **Blocks:** [bob-cli-16.3](bob-cli-16.3.md) ◐ · ⧖ 2026-08-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-16.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-16.2/README.md) | [bob-cli-16.2](bob-cli-16.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@87d38d6`](https://github.com/bobs-org/bob-plugins/commit/87d38d6de676787997197d2a037ccb25fafd16b1) | feat(navigation-hotkeys): add pomodoro bullet move picker | [bob-cli-16.2](bob-cli-16.2.md) | 2026-08-26 11:12:48 EDT |
