# Bead: bob-cli-27.1 — Parse and atomically apply Pomodoro duration adjustments

[Bead Pages](../README.md) / [bob-cli-27](README.md) / bob-cli-27.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.21](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.21.md) · **Assignee:** `bob-cli-27.1` · **Size:** medium
**Created:** 2026-09-26 19:06:51 EDT · **Closed:** 2026-09-26 19:21:37 EDT
**Plan:** [202609/adjust\_pomodoro\_duration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/adjust_pomodoro_duration.md)

## Description

adjustment_core: add exact-item signed-count grammar and a staged daily-ledger edit, with integration coverage for bulk capture, timing, failure, and rollback.

## Notes

[2026-09-26T23:21:25Z · bob-cli-27.1] PROPOSED FOLLOW-UP: cargo fmt --check fails on the clean base tree (1765 diffs, e.g. src/lib.rs import order) — likely rustfmt version drift; consider pinning the toolchain or running cargo fmt once

[2026-09-26T23:21:37Z · bob-cli-27.1] adjustment_core done: exact-item +N/-N grammar with strict errors, staged daily-ledger edit (checked arithmetic, midnight wrap, metadata/CRLF preservation, legacy stopwatch + range fallback), pomodoro_adjust JSON kind + human output, atomic batch/dry-run/rollback. Verified: 5 new cli tests pass, all 254 capture tests pass, full suite 1442 green, clippy clean; cargo fmt --check drift is pre-existing on base (recorded as follow-up)

## Dependencies

- **Blocks:** [bob-cli-27.2](bob-cli-27.2.md) ✓ · ⧖ 2026-09-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-27.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-27.1/README.md) | [bob-cli-27.1](bob-cli-27.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5ce5039`](https://github.com/bobs-org/bob-cli/commit/5ce5039aa68199b3a2da8f3bbcee7ac035c0d376) | feat(capture): parse and atomically apply Pomodoro duration adjustments | [bob-cli-27.1](bob-cli-27.1.md) | 2026-09-26 19:22:51 EDT |
