# Bead: bob-cli-3u.2 — Discover prerequisite tasks throughout the vault

[Bead Pages](../README.md) / [bob-cli-3u](README.md) / bob-cli-3u.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4m](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4m.md) · **Assignee:** `bob-cli-3u.2` · **Size:** medium
**Created:** 2026-10-03 09:11:57 EDT · **Closed:** 2026-10-03 10:29:26 EDT
**Plan:** [202610/capture\_task\_dependencies.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_task_dependencies.md)

## Description

dependency-discovery: add vault-wide prerequisite discovery, fuzzy ranking, exact note identities, and safe block-ID assignment support.

## Notes

[2026-10-03T14:24:23Z · bob-cli-3u.2] PROPOSED FOLLOW-UP: clippy deny-by-default overly_complex_bool_expr in tests/cli/capture/pomodoro_name.rs:808 fails just lint identically on the clean base tree (verified via stash); needs its own fix outside this phase

[2026-10-03T14:24:27Z · bob-cli-3u.2] PROPOSED FOLLOW-UP: clippy overly_complex_bool_expr in tests/cli/capture/pomodoro_name.rs:808 fails on clean base tree; needs its own fix outside this phase

[2026-10-03T14:29:26Z · bob-cli-3u.2] Discovery implemented and verified: vault-wide task_dependency completion (lanes/history order, shared tiered rank, exact note_path/locator/group/already/disabled rows, quoted replacements, read-only), capture-task-id --note-path/--allow-closed with previous-daily guard, 18 new tests; full cargo test green (lib 1578 + cli 900 + all targets), fmt clean; just lint blocked only by pre-existing pomodoro_name.rs:808 clippy error proven identical on clean base (recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-3u.1](bob-cli-3u.1.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3u.3](bob-cli-3u.3.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3u.4](bob-cli-3u.4.md) ◐ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3u.5](bob-cli-3u.5.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3u.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3u.2/README.md) | [bob-cli-3u.2](bob-cli-3u.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cfe88fc`](https://github.com/bobs-org/bob-cli/commit/cfe88fcb26c11f332db06337cfa68e80df8ac747) | feat(capture): add vault-wide task dependency discovery for bob-cli-3u.2 | [bob-cli-3u.2](bob-cli-3u.2.md) | 2026-10-03 10:30:54 EDT |
