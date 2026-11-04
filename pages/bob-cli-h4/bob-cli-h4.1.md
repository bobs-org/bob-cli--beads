# Bead: bob-cli-h4.1 — bob emits landing blocks for transfers (target, tombstones, moved tasks, sections)

[Bead Pages](../README.md) / [bob-cli-h4](README.md) / bob-cli-h4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.188](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.188.md) · **Assignee:** `bob-cli-h4.1` · **Size:** medium
**Created:** 2026-11-04 14:57:18 EST · **Closed:** 2026-11-04 15:44:25 EST
**Plan:** [202611/transfer\_previews.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/transfer_previews.md)

## Description

bob-landing-blocks: make every capture `>` transfer report batch-level `task_blocks` with new roles `merge_target`, `merge_source`, and `moved`. Moved blocks carry `moved_from` and a before-image taken from the source note. Add a batch-level `section_blocks` array for section merges. All JSON is additive.

## Notes

[2026-11-04T20:28:37Z · bob-cli-h4.1] PROPOSED FOLLOW-UP: Fix the clean-base strict docs-check anchor warning in reference/mac-capture/keyboard.md:104 (anchor does not exist); the same warning is already recorded as a PROPOSED FOLLOW-UP on bob-cli-h2.3#1.

[2026-11-04T20:44:02Z · bob-cli-h4.1] PROPOSED FOLLOW-UP: Resolve clean-base just lint failures in capture_language/editor_pomodoro.rs and past.rs (8 clippy errors); reproduced by just lint on clean tracked HEAD and already reported in bob-cli-h2.3#1.

[2026-11-04T20:44:25Z · bob-cli-h4.1] Implemented transfer task and section landing blocks, moved-task source before-images, serialization, docs, and refreshed note-pull fixtures. Verified cargo fmt, cargo check --all-targets, 21 transfer CLI tests, full just test, and git diff --check. just lint still hits the clean-base clippy errors in editor_pomodoro.rs/past.rs; docs-check strict build still hits the clean-base keyboard.md:104 anchor warning. Both baseline issues are recorded as proposed follow-ups.

## Dependencies

- **Blocks:** [bob-cli-h4.5](bob-cli-h4.5.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h4.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h4.1/README.md) | [bob-cli-h4.1](bob-cli-h4.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`decd465`](https://github.com/bobs-org/bob-cli/commit/decd465c2f2f0f2f1dbea7feb444e28c97a2751c) | feat(capture): emit transfer landing blocks | [bob-cli-h4.1](bob-cli-h4.1.md) | 2026-11-04 15:59:06 EST |
