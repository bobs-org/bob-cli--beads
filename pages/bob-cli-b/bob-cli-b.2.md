# Bead: bob-cli-b.2 — Sub-bullet capture in bob capture

[Bead Pages](../README.md) / [bob-cli-b](README.md) / bob-cli-b.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bryanbugyi34@gmail.com` · **Assignee:** `bob-cli-b.2` · **Size:** medium
**Created:** 2026-07-31 07:55:37 EDT · **Closed:** 2026-07-31 08:13:56 EDT
**Plan:** [202607/capture\_sub\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202607/capture_sub_bullets.md)

## Description

write: teach bob capture the @<route>^<block-id> marker plus -t/--task and hidden --task-ref, render and insert the child bullet at the parent task's own indentation, and report the new sub_bullet kind in human and JSON output.

## Notes

[2026-07-31T12:13:56Z · bob-cli-b.2] Implemented @<route>^<block-id>, --task, and hidden --task-ref sub-bullet capture with stale-safe task resolution, indentation/line-ending preservation, parent metadata in human and JSON output, documentation, and comprehensive unit/integration coverage. Verified cargo fmt --check, git diff --check, cargo clippy --all-targets --all-features, the focused sub-bullet/help tests, and full just all (all checks passed).

[2026-07-31T12:14:41Z · bob-cli-b.2] Verified sub-bullet capture implementation with just all and git diff --check; formatting, clippy, 675 Rust/integration/parity tests, and doc tests passed.

## Dependencies

- **Depends on:** [bob-cli-b.1](bob-cli-b.1.md) ✓
- **Blocks:** [bob-cli-b.3](bob-cli-b.3.md) ✓
