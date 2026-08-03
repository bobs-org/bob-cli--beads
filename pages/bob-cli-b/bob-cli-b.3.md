# Bead: bob-cli-b.3 — bob capture-tasks discovery command

[Bead Pages](../README.md) / [bob-cli-b](README.md) / bob-cli-b.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bryanbugyi34@gmail.com` · **Assignee:** `bob-cli-b.3` · **Size:** medium
**Created:** 2026-07-31 07:55:38 EDT · **Closed:** 2026-07-31 08:22:36 EDT
**Plan:** [202607/capture\_sub\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202607/capture_sub_bullets.md)

## Description

list: add the read-only bob capture-tasks subcommand that lists a note's open tasks as colored human output and stable JSON for pickers, and wire it into the runner, help surfaces, justfile smoke list, and README.

## Notes

[2026-07-31T12:22:36Z · bob-cli-b.3] Implemented the read-only bob capture-tasks command with open-task filtering, stable picker JSON, grouped/color-safe human output, native runner/help and install-smoke wiring, README documentation, unit coverage, and CLI end-to-end coverage. Verified focused capture-tasks/help tests and full just all: fmt, clippy --all-targets --all-features, 385 library tests, 239 CLI tests, all parity suites, and doc tests passed.

[2026-07-31T12:23:19Z · bob-cli-b.3] Post-completion finalizer verified the phase remains closed and the full just all gate passed: formatting, Clippy across all targets/features, 385 library tests, 239 CLI tests, parity suites, and doc tests.

## Dependencies

- **Depends on:** [bob-cli-b.2](bob-cli-b.2.md) ✓
- **Blocks:** [bob-cli-b.4](bob-cli-b.4.md) ✓
