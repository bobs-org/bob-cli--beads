# Bead: bob-cli-2c.2 — Report the started session's queued Task Links

[Bead Pages](../README.md) / [bob-cli-2c](README.md) / bob-cli-2c.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2s.md) · **Assignee:** `bob-cli-2c.2` · **Size:** medium
**Created:** 2026-09-28 12:19:13 EDT · **Closed:** 2026-09-28 12:56:17 EDT
**Plan:** [202609/pomodoro\_start\_next\_operator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_start_next_operator.md)

## Description

start_lineup: list and read-only resolve the started entry's direct-child Task Links through the close planner's vault view, and report them as `pomodoro_start.tasks` rows and human lineup lines.

## Notes

[2026-09-28T16:56:01Z · bob-cli-2c.2] PROPOSED FOLLOW-UP: Fix pre-existing clippy deny failure in tests/cli.rs (logic-bug lint on `|| true` expression in the scheduled-capture assertion near line 31812, present identically in HEAD); `cargo clippy --all-targets --all-features` cannot pass until it is addressed

[2026-09-28T16:56:17Z · bob-cli-2c.2] start_lineup done: new capture_pomodoro_start module lists direct-child Task Links and resolves them read-only via staged CloseVault (close helpers now pub(crate)); whole-item starts report tasks[] rows + human lineup rows with unchanged markers, dim warnings, and 'nothing queued'; link/task starts omit tasks. Verified: 4 new unit tests, new CLI lineup test (Ready/Next/InProgress/Blocked, embed, missing-ID/missing-note, same-draft task, nulls, no note writes), full suite green (1035 lib + 512 cli), fmt clean. Pre-existing clippy deny error at tests/cli.rs:31812 recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-2c.1](bob-cli-2c.1.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2c.3](bob-cli-2c.3.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2c.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2c.2/README.md) | [bob-cli-2c.2](bob-cli-2c.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`193e9f9`](https://github.com/bobs-org/bob-cli/commit/193e9f9b4b3759204a10ec6369d79972af1044ac) | feat(capture): report the started session's queued Task Links | [bob-cli-2c.2](bob-cli-2c.2.md) | 2026-09-28 12:58:15 EDT |
