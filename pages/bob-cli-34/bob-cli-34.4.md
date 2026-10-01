# Bead: bob-cli-34.4 — Navigation Hotkeys: recommended roll for Task Link sessions

[Bead Pages](../README.md) / [bob-cli-34](README.md) / bob-cli-34.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0um](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0um.md) · **Assignee:** `bob-cli-34.4` · **Size:** medium
**Created:** 2026-09-30 23:56:48 EDT · **Closed:** 2026-10-01 01:22:36 EDT
**Plan:** [202609/priority\_roll\_decay.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/priority_roll_decay.md)

## Description

picker-links: read each linked task's streak from its own note and reuse the composed batch planner for each note group. Commits go through commitLinkPickerNoteWrites with one shared Pomodoro prune and dependent recovery for cancelled tasks. Also bumps the manifest.

## Notes

[2026-10-01T05:22:36Z · bob-cli-34.4] picker-links done in bob-plugins: per-note roll recommendations via planLinkRollBatchSummary, applyLinkRecommendedRoll commit with shared prune and dependent recovery, single/batch preview with no pinned stage-two row; 990 npm tests pass, manifests valid, plugin synced

## Dependencies

- **Depends on:** [bob-cli-34.3](bob-cli-34.3.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-34.5](bob-cli-34.5.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-34.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-34.4/README.md) | [bob-cli-34.4](bob-cli-34.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@427f79c`](https://github.com/bobs-org/bob-plugins/commit/427f79c2566ccea68c6a9e0feda4c8e7cbd6c1bb) | feat(picker-links): add recommended roll for task-link picker sessions | [bob-cli-34.4](bob-cli-34.4.md) | 2026-10-01 01:25:11 EDT |
