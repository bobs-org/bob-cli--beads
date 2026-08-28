# Bead: bob-cli-1t.3 — \`bob capture-pomodoro-name\` write command

[Bead Pages](../README.md) / [bob-cli-1t](README.md) / bob-cli-1t.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0fk](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0fk.md) · **Assignee:** `bob-cli-1t.3` · **Size:** medium
**Created:** 2026-08-28 12:37:06 EDT · **Closed:** 2026-08-28 13:15:53 EDT
**Plan:** [202608/capture\_named\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_named_pomodoro.md)

## Description

pomodoro_name_command: add the single-purpose command that canonicalizes a name and appends it to one open, unnamed Pomodoro through an atomic rename.

## Notes

[2026-08-28T17:15:53Z · bob-cli-1t.3] Verified bob capture-pomodoro-name canonicalizes names, atomically appends or replaces the em-dash tail, preserves unrelated bytes including LF/CRLF, returns versioned JSON plus human output, and refuses stale/ambiguous/completed/already-named/missing-note writes with {ok:false} and no mutation. cargo fmt --check, cargo clippy --all-targets --all-features, and cargo test passed. On a scratch daily note, exactly one placeholder line changed and capture-pomodoros -f json reported DEEP WORK / deep-work.

## Dependencies

- **Depends on:** [bob-cli-1t.1](bob-cli-1t.1.md) ✓ · ⧖ 2026-08-28
- **Blocks:** [bob-cli-1t.5](bob-cli-1t.5.md) ◐ · ⧖ 2026-08-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1t.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1t.3/README.md) | [bob-cli-1t.3](bob-cli-1t.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a03bd58`](https://github.com/bobs-org/bob-cli/commit/a03bd58070857ea56434a4cc042aa13a725354e8) | feat(capture): add bob capture-pomodoro-name write command | [bob-cli-1t.3](bob-cli-1t.3.md) | 2026-08-28 13:17:04 EDT |
