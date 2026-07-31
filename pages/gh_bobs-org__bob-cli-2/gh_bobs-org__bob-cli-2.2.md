# Bead: gh\_bobs-org\_\_bob-cli-2.2 — Sub-bullet capture in bob capture

[Bead Pages](../README.md) / [gh\_bobs-org\_\_bob-cli-2](README.md) / gh\_bobs-org\_\_bob-cli-2.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Assignee:** `gh_bobs-org__bob-cli-2.2` · **Size:** medium
**Created:** 2026-07-31 11:55:37 UTC · **Closed:** 2026-07-31 12:13:56 UTC
**Plan:** [202607/capture\_sub\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202607/capture_sub_bullets.md)

## Description

write: teach bob capture the @<route>^<block-id> marker plus -t/--task and hidden --task-ref, render and insert the child bullet at the parent task's own indentation, and report the new sub_bullet kind in human and JSON output.

## Notes

[2026-07-31T12:13:56Z · gh_bobs-org__bob-cli-2.2] Implemented @<route>^<block-id>, --task, and hidden --task-ref sub-bullet capture with stale-safe task resolution, indentation/line-ending preservation, parent metadata in human and JSON output, documentation, and comprehensive unit/integration coverage. Verified cargo fmt --check, git diff --check, cargo clippy --all-targets --all-features, the focused sub-bullet/help tests, and full just all (all checks passed).

[2026-07-31T12:14:41Z · gh_bobs-org__bob-cli-2.2] Verified sub-bullet capture implementation with just all and git diff --check; formatting, clippy, 675 Rust/integration/parity tests, and doc tests passed.

## Dependencies

- **Depends on:** [gh\_bobs-org\_\_bob-cli-2.1](gh_bobs-org__bob-cli-2.1.md) ✓
- **Blocks:** [gh\_bobs-org\_\_bob-cli-2.3](gh_bobs-org__bob-cli-2.3.md) ✓

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.gh\_bobs-org\_\_bob-cli-2.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.gh_bobs-org__bob-cli-2.2/README.md) | [gh\_bobs-org\_\_bob-cli-2.2](gh_bobs-org__bob-cli-2.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed (UTC) |
|---|---|---|---|---|
| bob-cli | [`0dc8d66`](https://github.com/bobs-org/bob-cli/commit/0dc8d666f5c4542ac6df8ed81d2fb1d874257835) | feat(native): capture sub-bullets under existing tasks | [gh\_bobs-org\_\_bob-cli-2.2](gh_bobs-org__bob-cli-2.2.md) | 2026-07-31 12:15:06 |
