# Bead: bob-cli-fe.8 — Ctrl+Enter Pomodoro completion parity (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-fe](README.md) / bob-cli-fe.8

**Status:** ○ open · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c4.md) · **Assignee:** `bob-cli-fe.8` · **Size:** medium
**Created:** 2026-11-01 16:00:43 EST
**Plan:** [202611/merged\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merged_pomodoros.md)

## Description

obsidian-close-names: mirror R6 narrowing and shedding in task-status-cycler's Pomodoro completion so ledgers stay byte-identical with bob's x.

## Notes

[2026-11-02T11:31:25Z · bob-cli-fe.8] PROPOSED FOLLOW-UP: Clean-base bob-plugins npm test reproduces the same five failures (4,947 pass / 5 fail): missing Chromium in test-command-mode-sheet-sequence-dom [bob-cli-f1]; freshness namespace date-dependent reload event [bob-cli-et]; note-ready startup storm and relation-index layout-ready [bob-cli-eh]; schedule-work-log future-date failure [bob-cli-ff]. This exact cluster is also recorded on bob-cli-fe.7 note #1. Verified with this patch stashed on clean bob-plugins HEAD; not caused by bob-cli-fe.8.

[2026-11-02T11:39:30Z · bob-cli-fe.8] PROPOSED FOLLOW-UP: Deploy the completed R6 close-name parity changes after the active Stats clock build in the deployed Bob Ledger Tools plugin is landed. bob plugins sync refuses the current checkout because the deployed Ledger Tools and Task Status Cycler builds have uncommitted provenance; force-sync would remove the deployed Stats clock controls from Ledger Tools. Verified the owner of that deployed Stats build is still running. No vault plugin files were overwritten; phase verification is complete, deployment and bead closure remain pending.

## Dependencies

- **Blocks:** [bob-cli-fe.10](bob-cli-fe.10.md) ◐ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-fe.5](bob-cli-fe.5.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-fe.7](bob-cli-fe.7.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fe.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.8/README.md) | [bob-cli-fe.8](bob-cli-fe.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7a647e8`](https://github.com/bobs-org/bob-plugins/commit/7a647e821406caf09dfe8a7d124cdc5e55609fcd) | feat(pomodoro): mirror close-name shedding in cycler | [bob-cli-fe.8](bob-cli-fe.8.md) | 2026-11-02 06:40:16 EST |
