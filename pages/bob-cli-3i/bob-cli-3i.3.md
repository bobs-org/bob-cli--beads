# Bead: bob-cli-3i.3 — Render the parent task card in the preview pane

[Bead Pages](../README.md) / [bob-cli-3i](README.md) / bob-cli-3i.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vb](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vb.md) · **Assignee:** `bob-cli-3i.3` · **Size:** medium
**Created:** 2026-10-02 09:49:32 EDT · **Closed:** 2026-10-02 11:21:48 EDT
**Plan:** [202610/sub\_bullet\_task\_block\_preview.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/sub_bullet_task_block_preview.md)

## Description

mac_task_block_view: extract a shared BlockDiffCard from PomodoroBlockView, add TaskBlockView (status caption, status rail, diff gutter, indent guides, task tinting, expandable folds), render task blocks after the items, give covered sub-bullet items a compact header, name the parent in the status and summary, and fix the stale "Preview failed" footer. Add fake-bob routes, model, height, and render tests, the README, and green macOS CI.

## Notes

[2026-10-02T15:21:48Z · bob-cli-3i.3--1] Verified: macOS CI run 37025611761 green on bob-mac-capture commit b8b054f (all jobs passed: lint/build/test/bundle/smoke/install); commit adds BlockDiffCard+TaskBlockView, task-block render after items, compact sub-bullet headers, parent naming, footer fix, fake-bob routes plus model/height/render tests and README. sase bead epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-3i.2](bob-cli-3i.2.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3i.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3i.3.md) | [bob-cli-3i.3](bob-cli-3i.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@b8b054f`](https://github.com/bobs-org/bob-mac-capture/commit/b8b054fe17acc94e5bb53f39d5a703d3b0ce2a65) | feat(capture): show the full parent task when capturing a sub-bullet | [bob-cli-3i.3](bob-cli-3i.3.md) | 2026-10-02 11:14:49 EDT |
