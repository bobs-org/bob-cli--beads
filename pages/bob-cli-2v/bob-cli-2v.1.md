# Bead: bob-cli-2v.1 — Vault-wide linkable-task discovery and fuzzy ranking

[Bead Pages](../README.md) / [bob-cli-2v](README.md) / bob-cli-2v.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3j](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3j.md) · **Assignee:** `bob-cli-2v.1` · **Size:** medium
**Created:** 2026-09-30 13:00:14 EDT · **Closed:** 2026-09-30 13:25:02 EDT
**Plan:** [202609/task\_link\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_link_picker.md)

## Description

discovery: add the read-only `capture_link_tasks` scanner. It collects Ready, Blocked, Next, and In Progress tasks from area, project, and inbox notes. It adds groups, the canonical order, ledger annotation, block-ID suggestions, schedule pull-forward flags, and a deterministic tiered fuzzy ranker, all with unit tests.

## Notes

[2026-09-30T17:24:44Z · bob-cli-2v.1] PROPOSED FOLLOW-UP: Fix pre-existing clippy deny-by-default failure in tests/cli/capture/pomodoro_name.rs:808 (`|| true` in overly_complex_bool_expr); reproduces identically on the clean base tree, unrelated to this phase.

[2026-09-30T17:25:02Z · bob-cli-2v.1] Added src/native/capture_link_tasks.rs (LinkTask scanner, groups, canonical order, tiered ranker) with 9 unit tests covering the worked-example 8-row order and fields, exclusions, suggestions, pulls_forward, ledger warnings, unreadable notes, and ranker tiers/AND/stability. Shared is_linkable_status wired into pomodoro_link.rs and link_candidates; Ledger::position and pub find_single_future_scheduled_field exposed; bounded_warning reused. Verified: cargo fmt --check clean, full cargo test 2101 passed 0 failed, cargo clippy --lib clean; only clippy error is pre-existing in tests/cli/capture/pomodoro_name.rs:808, reproduced identically on clean base and filed as PROPOSED FOLLOW-UP. Transient dead-code warnings on the new API remain until phase complete wires it into capture-complete.

## Dependencies

- **Blocks:** [bob-cli-2v.4](bob-cli-2v.4.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2v.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2v.1/README.md) | [bob-cli-2v.1](bob-cli-2v.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d67bbb0`](https://github.com/bobs-org/bob-cli/commit/d67bbb0e174f128225424f5ab9a92c2fc09fa612) | feat(capture): add read-only linkable-task discover scanner with tiered ranker | [bob-cli-2v.1](bob-cli-2v.1.md) | 2026-09-30 13:27:40 EDT |
