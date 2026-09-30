# Bead: bob-cli-2r.4 — Render the Pomodoro block view in the preview pane

[Bead Pages](../README.md) / [bob-cli-2r](README.md) / bob-cli-2r.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3c.md) · **Assignee:** `bob-cli-2r.4` · **Size:** medium
**Created:** 2026-09-30 07:52:28 EDT · **Closed:** 2026-09-30 10:18:18 EDT
**Plan:** [202609/pomodoro\_full\_block\_preview.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_full_block_preview.md)

## Description

mac_block_view: add PomodoroBlockView (status rail, diff gutter, indent guides, syntax tint) and render blocks after the item stack. Drop verbatim lines the blocks already cover, dim blocks with a pending close card, and remove the duplicated path in the destination summary. Add link, move, and note fixtures, fake-bob routes, model, height, and render tests, the README, and green macOS CI.

## Notes

[2026-09-30T14:18:02Z · bob-cli-2r.4] Visual review skipped: the reachable Mac has CLT-only toolchain with no XCTest module, so swift test cannot link there; render test is committed and skips cleanly without BOB_MAC_CAPTURE_RENDER_DIR. Unrelated: master-tip commit d46667b (another agent, numbered drop-aware start card) is red on CI with a truncated lint log and no compiler error; commit 5497775 below it is green.

[2026-09-30T14:18:18Z · bob-cli-2r.4] Done: PomodoroBlockView with status caption/New badge, status rail, diff gutter, indent guides, verbatim tinted wrapping rows; PreviewPane renders blocks after items with pending-close dimming and covers() omission; single summary deduped; 4 real-bob fixtures + fake-bob routes (+5 now carries a block); model, height, and gated render tests added; README updated. Verified: macOS CI run 36727031554 green for 5497775 (full suite passed incl. 3 new model tests and height test; render test skips without env var); exact tree also builds clean via repo script; fake-bob serves all 16 probed drafts as valid JSON; no epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-2r.2](bob-cli-2r.2.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2r.3](bob-cli-2r.3.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2r.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2r.4/README.md) | [bob-cli-2r.4](bob-cli-2r.4.md) | 0 |
