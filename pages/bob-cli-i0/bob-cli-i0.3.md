# Bead: bob-cli-i0.3 — Live status line runner and build history

[Bead Pages](../README.md) / [bob-cli-i0](README.md) / bob-cli-i0.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.199](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.199.md) · **Assignee:** `bob-cli-i0.3` · **Size:** medium
**Created:** 2026-11-06 15:11:24 EST · **Closed:** 2026-11-06 16:10:40 EST
**Plan:** [202611/install\_all\_wait\_and\_whats\_new.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/install_all_wait_and_whats_new.md)

## Description

live-runner: implement `install_ui run`. It is the single-writer live status line around a child build, with Cargo and SwiftPM phase parsers, a chatter filter, logs, a failure excerpt, signal-safe cleanup, change-kind prediction, runs.jsonl recording, and the learning and last-similar-build ETA rungs. `record` and `kind` subcommands round it out. Tests run under real PTYs.

## Notes

[2026-11-06T21:10:40Z · bob-cli-i0.3] Implemented the live Cargo/SwiftPM runner, phase parsers, change-kind prediction, build history and learning ETA rung, record/kind commands, and bash fallback shim. Verified just check-scripts passed; the final install_ui suite passed all 58 tests, including PTY flood, silence, lock wait, display fault, status preservation, and signal cleanup cases.

## Dependencies

- **Depends on:** [bob-cli-i0.1](bob-cli-i0.1.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-i0.5](bob-cli-i0.5.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-i0.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.3/README.md) | [bob-cli-i0.3](bob-cli-i0.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d9b190f`](https://github.com/bobs-org/bob-cli/commit/d9b190f30a298bd89391cf35c01dd4051d1fe9a0) | feat(install): add live build runner and history | [bob-cli-i0.3](bob-cli-i0.3.md) | 2026-11-06 16:24:45 EST |
