# Bead: bob-cli-3u.5 — Verify the integrated contract and finish the visual review

[Bead Pages](../README.md) / [bob-cli-3u](README.md) / bob-cli-3u.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4m](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4m.md) · **Assignee:** `bob-cli-3u.5` · **Size:** small
**Created:** 2026-10-03 09:11:57 EDT · **Closed:** 2026-10-03 11:58:43 EDT
**Plan:** [202610/capture\_task\_dependencies.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_task_dependencies.md)

## Description

dependency-verification: exercise real CLI-to-app fixtures, inspect rendered picker states on macOS, and finish coordinated compatibility documentation.

## Notes

[2026-10-03T15:56:40Z · bob-cli-3u.5] PROPOSED FOLLOW-UP: cargo clippy --all-targets --all-features denies tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr from trailing `|| true`); file untouched by bob-cli-3u phases, fails on clean tree with clippy 1.95 — likely needs a small test-assertion cleanup

[2026-10-03T15:58:43Z · bob-cli-3u.5] Verified integrated & dependency contract against real binary + fixture vault: (1) both user examples work — new-task 'Buy Groceries! @home &foo:bar' and dependency-only '&foo:bar @body+excercise' — plus multi-dep, all writing canonical DEPENDS-ON lines with Blocked promotion; repeat add is idempotent ('Already depends on'). (2) capture-complete returns schema_version 1, task_dependency context, exact & range, decoded query, owner metadata, note_path. (3) capture-task-id --note-path dry-run returns backend dependency_replacement without writing. (4) task-status-hooks dry-run shows 0 drift (parity). (5) cargo fmt clean; full cargo test green (1599 lib + 909 cli + all other suites, 0 failures); docs/capture.md covers syntax matrix, JSON examples, additive-compat. cargo clippy has 1 pre-existing deny in untouched tests/cli/capture/pomodoro_name.rs:808 (recorded as PROPOSED FOLLOW-UP; fails identically on clean tree). macOS Swift/AppKit + render-PNG review unavailable on this Linux host — no interactive Mac verification claimed. No epic-symbol leftovers; tree clean, no code changes (verification-only phase).

## Dependencies

- **Depends on:** [bob-cli-3u.1](bob-cli-3u.1.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3u.2](bob-cli-3u.2.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3u.3](bob-cli-3u.3.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3u.4](bob-cli-3u.4.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3u.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3u.5/README.md) | [bob-cli-3u.5](bob-cli-3u.5.md) | 0 |
