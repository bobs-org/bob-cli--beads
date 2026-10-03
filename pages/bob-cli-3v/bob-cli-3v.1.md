# Bead: bob-cli-3v.1 — Keep-streak contract and Rust support

[Bead Pages](../README.md) / [bob-cli-3v](README.md) / bob-cli-3v.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4o](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4o.md) · **Assignee:** `bob-cli-3v.1` · **Size:** medium
**Created:** 2026-10-03 10:36:59 EDT · **Closed:** 2026-10-03 10:53:49 EDT
**Plan:** [202610/rotten\_keep\_streak.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_keep_streak.md)

## Description

contract-rust: specify the shared behavior, implement reading and reset semantics, preserve seed behavior, and publish schema 4 with parity vectors.

## Notes

[2026-10-03T14:53:39Z · bob-cli-3v.1] PROPOSED FOLLOW-UP: clippy --all-targets fails on untouched tests/cli/capture/pomodoro_name.rs:808 boolean logic bug (|| true); pre-existing on clean base, unrelated to keep-streak work

[2026-10-03T14:53:49Z · bob-cli-3v.1] contract-rust done: keeps read/reset/preserve + seed preserve-mode, decay config + 2026-10-19 activation + decide, schema 4 rows/counts/config/human, fixture vectors.json, docs §§2a/10a; cargo test full green (1598 lib + 906 cli), fmt clean, lib clippy clean

## Dependencies

- **Blocks:** [bob-cli-3v.2](bob-cli-3v.2.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3v.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3v.1/README.md) | [bob-cli-3v.1](bob-cli-3v.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c46f25d`](https://github.com/bobs-org/bob-cli/commit/c46f25d759f5d9f7e46311fd0cf7ebc795af7efe) | feat(freshness): keep-streak contract and Rust support for bob-cli-3v.1 | [bob-cli-3v.1](bob-cli-3v.1.md) | 2026-10-03 10:55:18 EDT |
