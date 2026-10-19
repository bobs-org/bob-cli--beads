# Bead: bob-cli-9r.5 — Today marks in rendered views

[Bead Pages](../README.md) / [bob-cli-9r](README.md) / bob-cli-9r.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11r](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11r.md) · **Assignee:** `bob-cli-9r.5` · **Size:** medium
**Created:** 2026-10-19 09:47:17 EDT · **Closed:** 2026-10-19 11:08:16 EDT
**Plan:** [202610/today\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/today_marks.md)

## Description

reading: add src/276-plugin-today-marks-reading.js. Rendered rows get marks only on exact section mapping and stay neutral otherwise. Add row stamping with a live refresh sweep, the daily-note view class, and delegated Mod+click, then test, bump, and sync.

## Notes

[2026-10-19T15:08:01Z · bob-cli-9r.5] PROPOSED FOLLOW-UP: Record decisions:today-mark-shows-ledger-today — epic decision memory_today_mark_record=no skipped the decisions-web strand; land agent may file it if Bryan reopens the memory ask.

[2026-10-19T15:08:04Z · bob-cli-9r.5] PROPOSED FOLLOW-UP: Pre-existing npm test failures on clean master — bob-cli-6v (4 unblocked-glyph wall-clock fixtures), bob-cli-6w (Keep counts once / decision-card Keep test), bob-cli-7i (forward conversion Depends-On / reverse BLOCKS ^prj). Reproduced identically after git stash of this phase.

[2026-10-19T15:08:16Z · bob-cli-9r.5] Reading-view Today marks shipped in bob-ledger-tools 1.59.0: src/276-plugin-today-marks-reading.js (post-processor order 60, exact section mapping or TM19-neutral, row stamping, sweep, daily-view class, delegated Mod+click). npm run build/build:check/validate green; today-marks + today-marks-reading 39/39; npm test 3162 pass / 6 fail all pre-existing on clean master (bob-cli-6v ×4, bob-cli-6w, bob-cli-7i). Fragments ≤1000. Vault synced via bob plugins sync --repo workspace clone. Memory strand not edited (memory_today_mark_record=no).

## Dependencies

- **Depends on:** [bob-cli-9r.4](bob-cli-9r.4.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9r.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9r.5/README.md) | [bob-cli-9r.5](bob-cli-9r.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@035296a`](https://github.com/bobs-org/bob-plugins/commit/035296a26ae8826766857e2bec7c005d55a8e5c0) | feat(ledger-tools): show Today marks in rendered views | [bob-cli-9r.5](bob-cli-9r.5.md) | 2026-10-19 11:09:30 EDT |
