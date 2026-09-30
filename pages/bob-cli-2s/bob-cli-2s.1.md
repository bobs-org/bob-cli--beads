# Bead: bob-cli-2s.1 — bob-cli: numbered start lineup and the drop engine

[Bead Pages](../README.md) / [bob-cli-2s](README.md) / bob-cli-2s.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3f](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3f.md) · **Assignee:** `bob-cli-2s.1` · **Size:** medium
**Created:** 2026-09-30 08:28:32 EDT · **Closed:** 2026-09-30 08:56:42 EDT
**Plan:** [202609/start\_drop\_queued\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/start_drop_queued_links.md)

## Description

start-lineup: number every whole-item start's queued Task Links (`tasks[].index`, `tasks[].now`, a numbered human index column). Build the pure drop engine: validate numbers against the lineup, remove each dropped Task Link subtree byte-exactly, and report `drop`/`dropped` plus duplicate warnings. Plumb a `drop` list through both start planners, with no grammar yet.

## Notes

[2026-09-30T12:56:11Z · bob-cli-2s.1] PROPOSED FOLLOW-UP: clippy deny `overly_complex_bool_expr` at tests/cli/capture/pomodoro_name.rs:808 (`|| true`) fails `just all` lint on the clean base tree too — pre-existing, untouched by start-lineup

[2026-09-30T12:56:42Z · bob-cli-2s.1] start-lineup done: numbered lineup (tasks[].index/now + bold index column), pure plan_start_drop engine (validate/remove/warn, CRLF + missing-newline safe), drop plumbed through both planners (created-session guard, parsed.body echo), JSON drop/dropped/nested_lines additive, docs updated. Verified: cargo test 2036 passed/0 failed, fmt clean, 13 new engine unit tests + 3 new CLI tests pass, existing lineup tests updated for index column only, =~2 still prose. just-all lint fails only on pre-existing pomodoro_name.rs:808 clippy deny (recorded as follow-up); no epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-2s.2](bob-cli-2s.2.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2s.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2s.1/README.md) | [bob-cli-2s.1](bob-cli-2s.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0b50af3`](https://github.com/bobs-org/bob-cli/commit/0b50af3cff1c86fc3bc995585b5896ae27a6edf6) | feat(capture): number whole-item start lineup and add plan\_start\_drop engine | [bob-cli-2s.1](bob-cli-2s.1.md) | 2026-09-30 09:06:14 EDT |
