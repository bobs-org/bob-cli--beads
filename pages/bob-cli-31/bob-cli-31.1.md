# Bead: bob-cli-31.1 — Freshness contract, placement helper, evaluator, and config in bob-cli

[Bead Pages](../README.md) / [bob-cli-31](README.md) / bob-cli-31.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.v.linker.w0.md) · **Assignee:** `bob-cli-31.1` · **Size:** medium
**Created:** 2026-09-30 19:32:05 EDT · **Closed:** 2026-09-30 19:54:34 EDT
**Plan:** [202609/task\_freshness\_review.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_freshness_review.md)

## Description

fresh-core: docs/freshness.md (definition, placement and state rules, conformance vectors), the Rust placement helper stamp_fresh / set_refresh, the pure evaluator, and the freshness: config block, with a test per vector and parse-invariance tests for both Rust task parsers.

## Notes

[2026-09-30T23:54:17Z · bob-cli-31.1] PROPOSED FOLLOW-UP: Fix pre-existing clippy deny error (overly_complex_bool_expr, `|| true`) at tests/cli/capture/pomodoro_name.rs:808 — reproduces identically on the clean base tree and blocks `cargo clippy --all-targets` / `just lint`

[2026-09-30T23:54:34Z · bob-cli-31.1] fresh-core done: docs/freshness.md contract with P1-P17/S1-S15 vectors; src/native/freshness/{placement,state} (stamp_fresh/set_refresh/read_freshness/tasks_suffix_start + pure evaluator with queue/counts); src/native/config/freshness.rs (interval 7, optional budget, mistyped-block isolation); verified: 45 freshness + 7 config tests pass, full cargo test green (1394 lib + all integration, 0 failures), cargo fmt clean, lib clippy clean; pre-existing clippy deny error in untouched tests/cli/capture/pomodoro_name.rs:808 reproduces on clean base, recorded as PROPOSED FOLLOW-UP

## Dependencies

- **Blocks:** [bob-cli-31.2](bob-cli-31.2.md) ◐ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.3](bob-cli-31.3.md) ◐ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.5](bob-cli-31.5.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-31.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-31.1/README.md) | [bob-cli-31.1](bob-cli-31.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`32d7007`](https://github.com/bobs-org/bob-cli/commit/32d700717c65ef691d6cb8cb457f948d56445686) | feat(freshness): implement fresh-core contract, placement, evaluator and config | [bob-cli-31.1](bob-cli-31.1.md) | 2026-09-30 19:56:49 EDT |
