# Bead: bob-cli-j.2 — Cursor-aware capture completion endpoint

[Bead Pages](../README.md) / [bob-cli-j](README.md) / bob-cli-j.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.005](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.005.md) · **Assignee:** `bob-cli-j.2` · **Size:** medium
**Created:** 2026-08-13 20:32:34 EDT · **Closed:** 2026-08-13 21:41:32 EDT
**Plan:** [202608/bob\_mac\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/bob_mac_capture.md)

## Description

completion: add bob capture-complete as the authoritative cursor-aware completion service over capture targets, sections, and open tasks, returning replacement ranges and stable JSON while preserving the current discovery-command contracts.

## Notes

[2026-08-14T01:41:32Z · bob-cli-j.2] Added native bob capture-complete command: cursor-aware completion over routes/sections/pomodoro-block-ids/sub-bullet tasks, reusing the phase-grammar tokenizer plus the capture-targets/-sections/-tasks scanners (no recursive bob invocation or JSON reparsing). Wired into native.rs, runner.rs, justfile smoke check, README, and tests/cli.rs help-surface tests. Verified: cargo fmt --check, cargo clippy --all-targets --all-features (only 3 pre-existing warnings in unrelated files), cargo test (838 tests passing incl. 46 new capture_language unit tests, 11 capture_complete unit tests, 14 tests/cli.rs integration tests covering every context, empty/no-op results, unicode cursor boundaries, out-of-range/non-boundary cursor rejection, missing notes, discovery errors, and no vault mutation), just install-smoke, and git diff --check. Manually verified end-to-end against a real vault.

[2026-08-14T01:42:02Z · bob-cli-j.2] Verified: cargo fmt --check, cargo clippy --all-targets --all-features (clean except 3 pre-existing warnings in untouched files), cargo test (838 tests passing), just install-smoke, git diff --check, and manual end-to-end CLI smoke test all passed for the capture-complete command.

## Dependencies

- **Depends on:** [bob-cli-j.1](bob-cli-j.1.md) ✓ · ⧖ 2026-08-13
- **Blocks:** [bob-cli-j.5](bob-cli-j.5.md) ◐ · ⧖ 2026-08-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j.2/README.md) | [bob-cli-j.2](bob-cli-j.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f548183`](https://github.com/bobs-org/bob-cli/commit/f548183568474812b5e7c28b2f7bc5c0cb092364) | feat(capture): add capture-complete cursor-aware completion command | [bob-cli-j.2](bob-cli-j.2.md) | 2026-08-13 21:42:24 EDT |
