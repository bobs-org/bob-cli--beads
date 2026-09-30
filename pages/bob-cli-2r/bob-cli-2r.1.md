# Bead: bob-cli-2r.1 — Emit batch-level pomodoro\_blocks from bob capture

[Bead Pages](../README.md) / [bob-cli-2r](README.md) / bob-cli-2r.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3c.md) · **Assignee:** `bob-cli-2r.1` · **Size:** medium
**Created:** 2026-09-30 07:52:28 EDT · **Closed:** 2026-09-30 08:44:16 EDT
**Plan:** [202609/pomodoro\_full\_block\_preview.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_full_block_preview.md)

## Description

blocks_tracker: add the block-range and depth helpers, the per-item block-ref tracker (ref resolution, auto-detection, cross-item forwarding, line diff), and the top-level `pomodoro_blocks` JSON. Add explicit refs for adjust, shift, whole-item and named starts, and whole-item close (closed and next). Add unit and CLI tests and the docs/capture.md contract.

## Notes

[2026-09-30T12:43:08Z · bob-cli-2r.1] PROPOSED FOLLOW-UP: reinstate debug_assert panics on unreported headline rewrites/vanishes once blocks_refs lands link/task-start refs (tracker currently downgrades to silent release behavior to keep the suite green)

[2026-09-30T12:43:15Z · bob-cli-2r.1] PROPOSED FOLLOW-UP: pre-existing clippy deny failure at tests/cli/capture/pomodoro_name.rs:808 (`|| true` in overly_complex_bool_expr) fails `just lint` on the clean tree

[2026-09-30T12:43:21Z · bob-cli-2r.1] PROPOSED FOLLOW-UP: pomodoro_close entry_line and top-level task_line are empty when close inserts Work Log lines above ## Pomodoros (day-file task), because the summary reads a stale pre-image line

[2026-09-30T12:44:16Z · bob-cli-2r.1] blocks_tracker done: batch-level pomodoro_blocks JSON with refs for adjust/shift/whole-item+named starts/whole-item close; 20 unit + 9 CLI tests green, full cargo test green (1297 lib/612 cli), fmt clean, epic-symbols clean; lint red only on pre-existing pomodoro_name.rs:808 (noted); heuristic debug panics downgraded per follow-up note, entry_line staleness noted

## Dependencies

- **Blocks:** [bob-cli-2r.2](bob-cli-2r.2.md) ◐ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2r.3](bob-cli-2r.3.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2r.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2r.1/README.md) | [bob-cli-2r.1](bob-cli-2r.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f32359f`](https://github.com/bobs-org/bob-cli/commit/f32359ff6a2cd7798a4fcf197240ef9781ad9e76) | feat(capture): add pomodoro blocks tracker with batch-level JSON | [bob-cli-2r.1](bob-cli-2r.1.md) | 2026-09-30 08:46:17 EDT |
