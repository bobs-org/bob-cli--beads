# Bead: bob-cli-3j.5 — Vault-aware value kinds with partial-parse context

[Bead Pages](../README.md) / [bob-cli-3j](README.md) / bob-cli-3j.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.46](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.46.md) · **Assignee:** `bob-cli-3j.5` · **Size:** medium
**Created:** 2026-10-02 11:06:16 EDT · **Closed:** 2026-10-02 12:29:35 EDT
**Plan:** [202610/bob\_shell\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_shell_completion.md)

## Description

vault-kinds: add partial-parse context and read-only vault providers for routes, sections, tasks, task sections, Pomodoro refs, plugins, levels, and vault notes, behind a 150 ms deadline, with a read-only enforcement test and fixture-vault goldens.

## Notes

[2026-10-02T16:29:12Z · bob-cli-3j.5] PROPOSED FOLLOW-UP: pre-existing clippy deny (overly_complex_bool_expr, logic_bug) at tests/cli/capture/pomodoro_name.rs:808 `|| true` fails `cargo clippy --all-targets` identically on the clean base tree (verified in HEAD); needs its own cleanup bead, left untouched here

[2026-10-02T16:29:35Z · bob-cli-3j.5] Vault kinds live: context.rs partial-parse (long/attached/short-cluster + env defaults), providers.rs read-only scans (routes/sections/tasks/task-sections/pomodoros/plugins/levels/!files-in vault notes) behind 150ms deadline (BOB_COMPLETE_DEADLINE_MS override). Verified: 12 new goldens in tests/cli/completion/vault.rs incl. read-only enforcement on write-locked vault (tree hashes, zero git calls, untouched XDG) + warn-only p50 check; 26 lib completion unit tests; full cargo test green (1517 lib + 756 cli, 0 failed); fmt clean; clippy clean except pre-existing pomodoro_name.rs:808 deny recorded as follow-up. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-3j.2](bob-cli-3j.2.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3j.6](bob-cli-3j.6.md) ◐ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3j.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3j.5/README.md) | [bob-cli-3j.5](bob-cli-3j.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`eafe65c`](https://github.com/bobs-org/bob-cli/commit/eafe65c5ccbbb4e631704068ce20b0b69f276c10) | feat(completion): add vault value completion with context and providers | [bob-cli-3j.5](bob-cli-3j.5.md) | 2026-10-02 12:32:46 EDT |
