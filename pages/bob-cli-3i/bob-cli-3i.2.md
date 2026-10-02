# Bead: bob-cli-3i.2 — Decode and present task blocks in CaptureCore

[Bead Pages](../README.md) / [bob-cli-3i](README.md) / bob-cli-3i.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vb](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vb.md) · **Assignee:** `bob-cli-3i.2` · **Size:** medium
**Created:** 2026-10-02 09:49:31 EDT · **Closed:** 2026-10-02 11:01:30 EDT
**Plan:** [202610/sub\_bullet\_task\_block\_preview.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/sub_bullet_task_block_preview.md)

## Description

mac_task_block_model: in bob-mac-capture, add tolerant `task_blocks` decoding, a shared diff-row model, task-row tokenizing (tags and block IDs), a pure CaptureTaskBlockPresentation (caption, status, rows, folding of long quiet runs, covers rule, accessibility), and sub-bullet wording. Add real-bob fixtures and CaptureCore tests. Commit and get macOS CI green.

## Notes

[2026-10-02T15:01:30Z · bob-cli-3i.2--1] CaptureCore swift test 578 passing on Linux, macOS CI green for 46c5614 (run 37023148696 conclusion success), fixtures real-bob; epic-symbols clean

## Dependencies

- **Depends on:** [bob-cli-3i.1](bob-cli-3i.1.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3i.3](bob-cli-3i.3.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3i.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3i.2.md) | [bob-cli-3i.2](bob-cli-3i.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@46c5614`](https://github.com/bobs-org/bob-mac-capture/commit/46c561497798c44e54406c7ee21b106d32aa895b) | feat(capture): decode and present sub-bullet task blocks | [bob-cli-3i.2](bob-cli-3i.2.md) | 2026-10-02 10:54:11 EDT |
