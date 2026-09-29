# Bead: bob-cli-2k.3 — Wire the selection into all close forms, JSON, and human output

[Bead Pages](../README.md) / [bob-cli-2k](README.md) / bob-cli-2k.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.34](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.34.md) · **Assignee:** `bob-cli-2k.3` · **Size:** medium
**Created:** 2026-09-29 13:45:03 EDT · **Closed:** 2026-09-29 14:32:08 EDT
**Plan:** [202609/close\_task\_selection.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_task_selection.md)

## Description

selection-capture: pass the parsed selection into the planner for whole-item,
link, and new-task closes, and remove the temporary refusal. Emit
`in_progress`, `complete`, `task_links`, and `tasks[].index` in the
`pomodoro_close` JSON. Print a numbered index column in human output, and fix the
`carries 1 links` plural. Pin all of it with CLI integration tests on the worked
example, including batches, link forms, dry-run parity, and every diagnostic.

## Notes

[2026-09-29T18:31:46Z · bob-cli-2k.3] PROPOSED FOLLOW-UP: clippy deny failure pre-exists on clean base (tests/cli/capture/pomodoro_name.rs:808 `|| true` trips clippy::overly_complex_bool_expr); `cargo clippy --all-targets --all-features` fails identically without this phase change

[2026-09-29T18:31:54Z · bob-cli-2k.3] PROPOSED FOLLOW-UP: plan close_task_selection.md worked-example post-images for =x2/=x0/link-forms show the closed entry folded as one line, but hand-edit + =x on the real binary keeps orphaned notes as sub-bullets (byte-parity verified); selection-docs should print the real bytes pinned in pomodoro_close_selection.rs

[2026-09-29T18:32:08Z · bob-cli-2k.3] Wired =x<N>!<M> selection into whole-item, link, and new-task closes (removed temp refusal); JSON gains in_progress/complete/task_links/tasks[].index with explicit nulls; human output gains outcome-colored index column, indented Work Log lines, and 'carries 1 link' fix. Verified: new pomodoro_close_selection.rs (10 tests: all worked rows, link forms, batches, dry-run parity, every diagnostic, CRLF), updated plain-=x contract, cargo test fully green (1167+535+rest, 0 fail), fmt clean, no new clippy warnings.

## Dependencies

- **Depends on:** [bob-cli-2k.1](bob-cli-2k.1.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2k.2](bob-cli-2k.2.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2k.4](bob-cli-2k.4.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2k.5](bob-cli-2k.5.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2k.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2k.3/README.md) | [bob-cli-2k.3](bob-cli-2k.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2c32a91`](https://github.com/bobs-org/bob-cli/commit/2c32a91940b415e4c281910040c6cd415a5fe76f) | feat(capture): wire selection capture into pomodoro close | [bob-cli-2k.3](bob-cli-2k.3.md) | 2026-09-29 14:34:25 EDT |
