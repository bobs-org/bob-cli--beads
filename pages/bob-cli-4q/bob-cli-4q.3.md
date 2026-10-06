# Bead: bob-cli-4q.3 — Route gate on Ctrl+Shift+Enter in block-id-prompt

[Bead Pages](../README.md) / [bob-cli-4q](README.md) / bob-cli-4q.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0xh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0xh.md) · **Assignee:** `bob-cli-4q.3` · **Size:** small
**Created:** 2026-10-06 14:57:18 EDT · **Closed:** 2026-10-06 15:30:04 EDT
**Plan:** [202610/inbox\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inbox_routing.md)

## Description

link-toggle-gate: have block-id-prompt's link and unlink paths ask through nav `inboxRoute` before writing, move after a committed toggle, and compose one toast with a `route` walk outcome. Fall back to today's behavior when nav lacks the api; block-id-prompt 1.23.0.

## Notes

[2026-10-06T19:30:04Z · bob-cli-4q.3] link-toggle-gate done in bob-plugins (block-id-prompt 1.23.0): getInboxRouteApi v1 detector; inbox gate in applyPomodoroTaskLink/Unlink (cancel writes nothing, stay is today, move links/unlinks then commits with one composed toast and route/link-today walk outcome); 13 new runtime tests, full npm suite 1938/1938 green, build:check clean, deployed block-id-prompt only and vault in sync; epic-symbols clean

## Dependencies

- **Depends on:** [bob-cli-4q.1](bob-cli-4q.1.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4q.4](bob-cli-4q.4.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4q.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4q.3/README.md) | [bob-cli-4q.3](bob-cli-4q.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3689d34`](https://github.com/bobs-org/bob-plugins/commit/3689d347841adc3e7955a39ca89b250079bdba47) | feat(block-id-prompt): gate pomodoro link toggle on inbox route | [bob-cli-4q.3](bob-cli-4q.3.md) | 2026-10-06 15:31:37 EDT |
