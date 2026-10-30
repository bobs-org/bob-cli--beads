# Bead: bob-cli-ea.8 — Obsidian trigger, ledger guard, and Events painting

[Bead Pages](../README.md) / [bob-cli-ea](README.md) / bob-cli-ea.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2w.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2w.linker.w0.md) · **Assignee:** `bob-cli-ea.8` · **Size:** medium
**Created:** 2026-10-29 19:40:04 EDT
**Plan:** [202610/bob\_gcal\_daily\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_gcal_daily_events.md)

## Description

obsidian-events: run bob gcal sync when today's note is created, add a gcal-sync toast adapter, stop the section-move gesture from dropping task rows into the ledger, paint Events rows when chosen, test, document, and deploy.

## Notes

[2026-10-30T06:39:33Z · bob-cli-ea.8] PROPOSED FOLLOW-UP: Regenerate bob-cli generated docs after the Calendar decision records (already tracked by bob-cli-b6); docs-check fails on the clean 98f9a23 base because docs/develop/decisions.md is stale, outside this plugin phase.

[2026-10-30T06:47:24Z · bob-cli-ea.8] PROPOSED FOLLOW-UP: Fix the four successor-theme wiring failures that remain on clean bob-plugins base 957f741 (related prior work: bob-cli-dm.7.1.4); the same four assertions fail in the current tree, outside this phase scope.

## Dependencies

- **Depends on:** [bob-cli-ea.6](bob-cli-ea.6.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-ea.9](bob-cli-ea.9.md) ◐ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ea.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ea.8/README.md) | [bob-cli-ea.8](bob-cli-ea.8.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@cd214ff`](https://github.com/bobs-org/bob-plugins/commit/cd214ff67db0a6f78199275854446f4d2d3bcb9c) | fix(task-status-cycler): keep task rows out of Pomodoros | [bob-cli-ea.8](bob-cli-ea.8.md) | 2026-10-30 02:49:15 EDT |
| bob-plugins | [`bob-plugins@116ad00`](https://github.com/bobs-org/bob-plugins/commit/116ad007e2b23449f74a55c9748aa36837ebd1cb) | feat(command-mode): summarize Calendar sync outcomes | [bob-cli-ea.8](bob-cli-ea.8.md) | 2026-10-30 02:51:00 EDT |
