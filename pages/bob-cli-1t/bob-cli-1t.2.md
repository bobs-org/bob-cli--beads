# Bead: bob-cli-1t.2 — \`@route:id#pomodoro\` grammar and capture execution

[Bead Pages](../README.md) / [bob-cli-1t](README.md) / bob-cli-1t.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0fk](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0fk.md) · **Assignee:** `bob-cli-1t.2` · **Size:** medium
**Created:** 2026-08-28 12:37:06 EDT · **Closed:** 2026-08-28 13:16:02 EDT
**Plan:** [202608/capture\_named\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_named_pomodoro.md)

## Description

capture_named_marker: extend the capture grammar with the third Pomodoro-name component, route it through capture execution's Pomodoro selection, and report it in capture-parse spans, needs, and diagnostics.

## Notes

[2026-08-28T17:16:02Z · bob-cli-1t.2] Verified cargo test (unit + CLI), cargo fmt, and clippy on the capture path. @dev:id#bugs dry-run JSON appends under BUGS while @dev:id inserts under the current Pomodoro; both notes stay unchanged. bob capture-parse -f json -- '@dev:some-id#' reports mode incomplete with needs ["pomodoro_name"]. Empty #, missing block ID before the name, invalid name chars, completed-only, unknown-name suggestion, unnamed-open, and multiple-open-timed-with-explicit-name cases match the design.

## Dependencies

- **Depends on:** [bob-cli-1t.1](bob-cli-1t.1.md) ✓ · ⧖ 2026-08-28
- **Blocks:** [bob-cli-1t.4](bob-cli-1t.4.md) ◐ · ⧖ 2026-08-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1t.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1t.2/README.md) | [bob-cli-1t.2](bob-cli-1t.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9b7282d`](https://github.com/bobs-org/bob-cli/commit/9b7282d8b2bba90c798ce0143c55c988e615a841) | feat(capture): add @route:id#pomodoro named targeting | [bob-cli-1t.2](bob-cli-1t.2.md) | 2026-08-28 13:16:57 EDT |
