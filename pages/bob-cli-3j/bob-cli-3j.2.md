# Bead: bob-cli-3j.2 — Hidden \_\_complete endpoint, protocol 1, and static value kinds

[Bead Pages](../README.md) / [bob-cli-3j](README.md) / bob-cli-3j.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.46](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.46.md) · **Assignee:** `bob-cli-3j.2` · **Size:** medium
**Created:** 2026-10-02 11:06:16 EDT · **Closed:** 2026-10-02 11:56:05 EDT
**Plan:** [202610/bob\_shell\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_shell_completion.md)

## Description

engine: pin clap_complete's dynamic engine behind one module, add the early-intercepted hidden __complete endpoint speaking protocol 1, the kinds table with static decisions, the presenter rules and groups, coverage and golden tests, and the first docs/completion.md.

## Notes

[2026-10-02T15:53:03Z · bob-cli-3j.2] PROPOSED FOLLOW-UP: clippy deny clippy::overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 (stray || true) fails just lint identically on the clean base tree; needs its own fix -r lint gate fails on pre-existing error unrelated to engine phase

[2026-10-02T15:56:05Z · bob-cli-3j.2] Engine phase done: clap_complete 4.6.11 pinned (clap 4.6.7), hidden __complete endpoint with protocol 1, static kinds table with bidirectional coverage tests, presenter rules/groups, 16 golden integration tests + unit tests all passing, full cargo test green (1510 lib + 743 cli), docs/completion.md added. just lint fails only on pre-existing clippy deny at tests/cli/capture/pomodoro_name.rs:808, identical on clean base, recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-3j.1](bob-cli-3j.1.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3j.3](bob-cli-3j.3.md) ◐ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3j.5](bob-cli-3j.5.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3j.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3j.2/README.md) | [bob-cli-3j.2](bob-cli-3j.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b9a067d`](https://github.com/bobs-org/bob-cli/commit/b9a067da5c8a55ca5e153c6469df06fdc3c0efa2) | feat(completion): add native shell completion engine with protocol and presenter | [bob-cli-3j.2](bob-cli-3j.2.md) | 2026-10-02 11:59:11 EDT |
