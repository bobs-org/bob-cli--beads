# Bead: bob-cli-ac.1 — Hermetic test suite and pinned toolchain

[Bead Pages](../README.md) / [bob-cli-ac](README.md) / bob-cli-ac.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.w1.md) · **Assignee:** `bob-cli-ac.1` · **Size:** small
**Created:** 2026-10-20 18:36:53 EDT · **Closed:** 2026-10-20 19:16:11 EDT
**Plan:** [202610/crates\_io\_release\_train.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/crates_io_release_train.md)

## Description

hermetic: fix the three tests that fail in a clean environment and add rust-toolchain.toml pinned to 1.95.0.

## Notes

[2026-10-20T23:15:58Z · bob-cli-ac.1] Verified: added rust-toolchain.toml pinned to 1.95.0; fixed the capture priority test with an explicit temp config path, added a test-local uv stub to gkeep doctor subprocesses, and made zsh header testing UTF-8/locale-tolerant. just check passed (fmt, clippy, 3,135 lib tests, 1,930 CLI tests, all integration/doc tests). Clean HOME cargo test --locked --no-fail-fast passed with TZ=UTC and TZ=America/New_York (UTC cold run about 9 min wall; New York cached run about 90 sec).

[2026-10-20T23:16:11Z · bob-cli-ac.1] Pinned Rust 1.95.0; made all three tests hermetic with explicit config, stub uv PATH, and locale-independent zsh checks. Verified just check and clean-HOME cargo test --locked --no-fail-fast under UTC and America/New_York; epic-symbols had no leftovers.

## Dependencies

- **Blocks:** [bob-cli-ac.3](bob-cli-ac.3.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ac.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ac.1/README.md) | [bob-cli-ac.1](bob-cli-ac.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9a0fb95`](https://github.com/bobs-org/bob-cli/commit/9a0fb957a810b314d8a9ef11ca67d95632651f48) | build: pin Rust toolchain and hermeticize tests | [bob-cli-ac.1](bob-cli-ac.1.md) | 2026-10-20 19:17:21 EDT |
