# Bead: gh\_bobs-org\_\_bob-cli-2.3 — bob capture-tasks discovery command

[Bead Pages](../README.md) / [gh\_bobs-org\_\_bob-cli-2](README.md) / gh\_bobs-org\_\_bob-cli-2.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Assignee:** `gh_bobs-org__bob-cli-2.3` · **Size:** medium
**Created:** 2026-07-31 11:55:38 UTC · **Closed:** 2026-07-31 12:22:36 UTC
**Plan:** [202607/capture\_sub\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202607/capture_sub_bullets.md)

## Description

list: add the read-only bob capture-tasks subcommand that lists a note's open tasks as colored human output and stable JSON for pickers, and wire it into the runner, help surfaces, justfile smoke list, and README.

## Notes

[2026-07-31T12:22:36Z · gh_bobs-org__bob-cli-2.3] Implemented the read-only bob capture-tasks command with open-task filtering, stable picker JSON, grouped/color-safe human output, native runner/help and install-smoke wiring, README documentation, unit coverage, and CLI end-to-end coverage. Verified focused capture-tasks/help tests and full just all: fmt, clippy --all-targets --all-features, 385 library tests, 239 CLI tests, all parity suites, and doc tests passed.

[2026-07-31T12:23:19Z · gh_bobs-org__bob-cli-2.3] Post-completion finalizer verified the phase remains closed and the full just all gate passed: formatting, Clippy across all targets/features, 385 library tests, 239 CLI tests, parity suites, and doc tests.

## Dependencies

- **Depends on:** [gh\_bobs-org\_\_bob-cli-2.2](gh_bobs-org__bob-cli-2.2.md) ✓
- **Blocks:** [gh\_bobs-org\_\_bob-cli-2.4](gh_bobs-org__bob-cli-2.4.md) ◐

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.gh\_bobs-org\_\_bob-cli-2.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.gh_bobs-org__bob-cli-2.3/README.md) | [gh\_bobs-org\_\_bob-cli-2.3](gh_bobs-org__bob-cli-2.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed (UTC) |
|---|---|---|---|---|
| bob-cli | [`851d7a1`](https://github.com/bobs-org/bob-cli/commit/851d7a1601cef987bbff084bcb1c1a08061f7398) | feat(native): list open capture tasks | [gh\_bobs-org\_\_bob-cli-2.3](gh_bobs-org__bob-cli-2.3.md) | 2026-07-31 12:23:42 |
