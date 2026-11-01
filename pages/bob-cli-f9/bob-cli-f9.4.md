# Bead: bob-cli-f9.4 — bob-plugins retires the type cap

[Bead Pages](../README.md) / [bob-cli-f9](README.md) / bob-cli-f9.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.by](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.by.md) · **Assignee:** `bob-cli-f9.4` · **Size:** medium
**Created:** 2026-11-01 12:12:36 EST · **Closed:** 2026-11-01 15:28:48 EST
**Plan:** [202611/retire\_type\_cap\_today\_roots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/retire_type_cap_today_roots.md)

## Description

plugins-drop-type-cap: mirror the cap removal across bob-ledger-tools, block-id-prompt, bob-navigation-hotkeys, and task-status-cycler (TODAY L/Lc chip, caps API, routing, pickers, notices), copy the routing vectors, update tests and docs, and sync.

## Notes

[2026-11-01T19:42:49Z · bob-cli-f9.4--2] PROPOSED FOLLOW-UP: Track the four clean-base npm test failures through existing beads bob-cli-et (real-date freshness/GCal tests) and bob-cli-eh (single-slot onLayoutReady test fakes). Reproduced identically on clean bob-plugins HEAD on 2026-11-01 with the same assertions; no duplicate task needed.

[2026-11-01T20:28:48Z · bob-cli-f9.4--4] Verified plugins-drop-type-cap: TODAY chip, caps API, routing, pickers, and notices drop maxThemes/strict; leftover rg hits are the stale-key comment/test. npm test 4751/4755 (4 clean-base failures already tracked by bob-cli-et and bob-cli-eh); validate and docs:check pass. Copied routing vectors from bob-cli 3de72bfd. Synced block-id-prompt, bob-ledger-tools, task-status-cycler, and bob-navigation-hotkeys to the vault.

## Dependencies

- **Depends on:** [bob-cli-f9.2](bob-cli-f9.2.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f9.5](bob-cli-f9.5.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-f9.4.md) | [bob-cli-f9.4](bob-cli-f9.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@270b19b`](https://github.com/bobs-org/bob-plugins/commit/270b19bd0212b95c6413566fe8e379e90fbd85d7) | feat(plan)!: retire the daily type cap from plugins | [bob-cli-f9.4](bob-cli-f9.4.md) | 2026-11-01 15:30:28 EST |
