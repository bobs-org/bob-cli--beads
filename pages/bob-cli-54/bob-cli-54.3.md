# Bead: bob-cli-54.3 — Wire the picker into Ctrl+Shift+Enter, notices, docs, release

[Bead Pages](../README.md) / [bob-cli-54](README.md) / bob-cli-54.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5h](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.5h/README.md) · **Assignee:** `bob-cli-54.3` · **Size:** medium
**Created:** 2026-10-07 09:22:16 EDT · **Closed:** 2026-10-07 10:02:52 EDT
**Plan:** [202610/ctrl\_shift\_enter\_pomodoro\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_enter_pomodoro_picker.md)

## Description

gesture: move the inbox-route helpers out of the full fragment, add the picker mixin and preflight, route the choice through the link flow, name the destination in Notices, update the harness and tests, add runtime tests, bump to 1.24.0, update docs in both repos, and sync.

## Notes

[2026-10-07T14:02:52Z · bob-cli-54.3] Wired Link-to-today picker into Ctrl+Shift+Enter: split 120 into 122 picker mixin with preflight/budget projection and 124 inbox-route mixin, routed choice via source.pomodoroTarget, named destinations in Notices with 4 new plan errors, stubbed harness to default choice and updated 14 link-runtime + 3 budget assertions, added 15-test picker-runtime suite, bumped to 1.24.0 with README/docs in both repos. Verified: bob-plugins npm build/test (2101 pass)/validate green, bob plugins sync deployed, epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-54.1](bob-cli-54.1.md) ✓ · ⧖ 2026-10-07
- **Depends on:** [bob-cli-54.2](bob-cli-54.2.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-54.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-54.3/README.md) | [bob-cli-54.3](bob-cli-54.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9c825ca`](https://github.com/bobs-org/bob-cli/commit/9c825cacdf8e4713fe6f40241504026df5dd8f46) | docs(plan): link-to-today picker docs for Ctrl+Shift+Enter | [bob-cli-54.3](bob-cli-54.3.md) | 2026-10-07 10:04:30 EDT |
