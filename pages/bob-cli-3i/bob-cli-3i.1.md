# Bead: bob-cli-3i.1 — Emit batch-level task\_blocks from bob capture

[Bead Pages](../README.md) / [bob-cli-3i](README.md) / bob-cli-3i.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vb](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vb.md) · **Assignee:** `bob-cli-3i.1` · **Size:** medium
**Created:** 2026-10-02 09:49:31 EDT · **Closed:** 2026-10-02 10:35:19 EDT
**Plan:** [202610/sub\_bullet\_task\_block\_preview.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/sub_bullet_task_block_preview.md)

## Description

task_blocks_contract: move the Pomodoro block diff helpers into a shared module, add a batch-level parent-task tracker fed by sub-bullet items, and emit the additive top-level `task_blocks` JSON (final-state block, cumulative diff against the note before the capture). Add unit and CLI tests and the docs/capture.md contract. Pomodoro block JSON stays byte-identical.

## Notes

[2026-10-02T14:34:31Z · bob-cli-3i.1] PROPOSED FOLLOW-UP: flaky lib test native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes fails under parallel runs (unlocked process-global BOB_DAY_FILE with_env race); reproduces identically on clean base with `cargo test --lib -- capture_pomodoros capture_complete`; already tracked by task bead bob-cli-2e; full lib suite passes single-threaded (1487/1487)

[2026-10-02T14:35:19Z · bob-cli-3i.1] task_blocks_contract done: shared block_diff module (pomodoro JSON byte-identical via type aliases), TaskBlockTracker with forwarding/merging/cumulative diff wired through plan/batch/output; 12 unit + 5 CLI tests pass; docs/capture.md Task blocks contract added. Verified: cargo fmt --check pass, cargo clippy pass (no new warnings), cargo test --lib single-threaded 1487/1487, cargo test --test cli 727/727. One parallel-only lib flake (capture_pomodoros missing_note, BOB_DAY_FILE with_env race) reproduces identically on clean base, recorded as PROPOSED FOLLOW-UP citing task bob-cli-2e.

## Dependencies

- **Blocks:** [bob-cli-3i.2](bob-cli-3i.2.md) ◐ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3i.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3i.1/README.md) | [bob-cli-3i.1](bob-cli-3i.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`00d4941`](https://github.com/bobs-org/bob-cli/commit/00d49417e080a8a2aef3379f7962ca096ce98161) | feat(capture): emit batch-level task\_blocks from bob capture json | [bob-cli-3i.1](bob-cli-3i.1.md) | 2026-10-02 10:37:36 EDT |
