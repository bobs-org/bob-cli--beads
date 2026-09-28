# Bead: bob-cli-2b.3 — bob randomize command, output, and integration tests

[Bead Pages](../README.md) / [bob-cli-2b](README.md) / bob-cli-2b.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2q.md) · **Assignee:** `bob-cli-2b.3` · **Size:** medium
**Created:** 2026-09-28 10:45:18 EDT · **Closed:** 2026-09-28 11:51:01 EDT
**Plan:** [202609/bob\_randomize.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/bob_randomize.md)

## Description

command: add the clap CLI and runner registration; orchestrate lock, pre-sync, plan and guarded apply with retries, scoped commit, and post-sync; render the human and JSON outputs and exit codes; add tests/randomize.rs integration coverage, including git, conflicts, determinism, and task-status-hooks parity.

## Notes

[2026-09-28T15:50:48Z · bob-cli-2b.3] PROPOSED FOLLOW-UP: just lint fails on pre-existing clippy deny (overly_complex_bool_expr) at tests/cli.rs:31482, untouched by this bead; fix the `|| true` logic bug or gate the lint

[2026-09-28T15:51:01Z · bob-cli-2b.3] Implemented bob randomize command (src/native/randomize.rs), registered in runner/native/justfile, removed planner+plumbing dead-code allows; 14 tests in tests/randomize.rs all pass, full cargo test green (1028+503+27+14+31+1), fmt clean, real-vault dry-run matches contract (222 tasks/28 notes); just lint blocked by pre-existing tests/cli.rs:31482 deny recorded as follow-up

## Dependencies

- **Depends on:** [bob-cli-2b.1](bob-cli-2b.1.md) ✓ · ⧖ 2026-09-28
- **Depends on:** [bob-cli-2b.2](bob-cli-2b.2.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2b.4](bob-cli-2b.4.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2b.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2b.3/README.md) | [bob-cli-2b.3](bob-cli-2b.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1e8484b`](https://github.com/bobs-org/bob-cli/commit/1e8484b8df228cc11041f9a3b9fc1a5b08392329) | feat(randomize): add bob randomize priority reshuffle command | [bob-cli-2b.3](bob-cli-2b.3.md) | 2026-09-28 11:56:10 EDT |
