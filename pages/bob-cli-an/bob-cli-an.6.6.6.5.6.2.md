# Bead: bob-cli-an.6.6.6.5.6.2 — Map review-walk and counted Depends-On line indexes through BLOCKS insertions

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6](bob-cli-an.6.6.6.5.6.md) / bob-cli-an.6.6.6.5.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.2` · **Size:** large
**Created:** 2026-10-24 09:36:38 EDT · **Closed:** 2026-10-24 10:17:03 EDT
**Plan:** [202610/backlog\_batch6\_color\_quote\_walk\_blocks\_shift\_promotion\_race\_mac\_panel\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch6_color_quote_walk_blocks_shift_promotion_race_mac_panel_ci.md)

## Description

blocks-shift-indexes: resolve bob-cli-94 and bob-cli-95 by threading the answered or pending task's post-write line through generated BLOCKS-line edits in bob-navigation-hotkeys instead of reusing pre-write indexes.

## Notes

[2026-10-24T14:16:46Z · bob-cli-an.6.6.6.5.6.2] Implemented blocks-shift-indexes: tracked counted sources through plan.lineEdits via mapLineThroughLineEdits in 270-counted-batches (immutable snapshots + mutable lines, parentLineNext stamping, mapped cursorLine), 420-picker-counted-dependency remove + vault loops (parentLineNext stamping, mapped tracked lines, all-or-nothing refuse), 570 writer cursor mapped through Pomodoro cleanup via withCountedPomodoroCursorMapped in 181-editor-line-diff (570 stays 996 lines). Review: 340 retains reviewOriginContent snapshot, 350 readReviewOriginAfterLine aligns snapshot to current via alignEditorLines (no BLOCKS/cursor substitution, null when unidentified, idempotent), reused in 455 inbox fallback. Tests: new regressions in hotkeys-dependencies (BLOCKS add/remove, runtime one-undo + cursor + stale), stage-stale-guards (vault same-note add/remove with post-plan stamps, cross-note control), review-advance-gestures (BLOCKS insert advance + idempotence, deletion stay, cursor/reader + deletion null). Baseline bob-cli-94/95 reproduced (counted valid:false, settle read BLOCKS at index1 vs task at index2). Focused 181 tests pass; npm run validate pass; npm run docs:check pass (447 passed); npm test pass (3557). Plugin 2.56.3 built, docs:gen inventory updated, bob plugins sync --no-pull deployed (2 copied, 1 unchanged, backups 20261024-101626), bob plugins list shows 2.56.3 synced.

[2026-10-24T14:17:03Z · bob-cli-an.6.6.6.5.6.2] blocks-shift-indexes done: counted sources follow BLOCKS via lineEdits mapping with parentLineNext stamps and mapped cursor (270, 420 x2, 570 via 181 helper); review origin resolves via snapshot alignment (340/350, reused in 455) with idempotent conservative settle. Focused 181 pass, validate pass, docs:check pass (447), npm test pass (3557). Plugin 2.56.3 built, inventory regenerated, deployed via bob plugins sync --no-pull (2 copied, synced).

## Dependencies

- **Blocks:** [bob-cli-an.6.6.6.5.6.3](bob-cli-an.6.6.6.5.6.3.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.2.md) | [bob-cli-an.6.6.6.5.6.2](bob-cli-an.6.6.6.5.6.2.md) | 0 |
