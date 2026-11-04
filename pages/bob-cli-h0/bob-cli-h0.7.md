# Bead: bob-cli-h0.7 — Move card state, view, and decoding

[Bead Pages](../README.md) / [bob-cli-h0](README.md) / bob-cli-h0.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.37.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.37.linker.w0.md) · **Assignee:** `bob-cli-h0.7` · **Size:** medium
**Created:** 2026-11-04 08:50:24 EST · **Closed:** 2026-11-04 13:31:03 EST
**Plan:** [202611/move\_choice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/move_choice.md)

## Description

mac-card: decode `move_choice`, build the portable three-state card state machine and its tests, and draw the Move card (sigil wells, chips, counter, detail strip, primary label) without wiring it into submit.

## Notes

[2026-11-04T18:31:03Z · bob-cli-h0.7--1] Implemented move_choice decoding, portable three-state model, and standalone Move card. Verified portable-check on athena (2,104 tests passed, 1 skipped), focused move-choice tests (8 passed), and formatting on new Swift files. macOS type-check unavailable: mac SSH timed out. No epic-symbol entries remained.

## Dependencies

- **Depends on:** [bob-cli-h0.4](bob-cli-h0.4.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h0.8](bob-cli-h0.8.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-h0.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-h0.7.md) | [bob-cli-h0.7](bob-cli-h0.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@4906d94`](https://github.com/bobs-org/bob-mac-capture/commit/4906d94fdcb6b162deff64ce83d627d99d8a3fbf) | feat(capture): add move-choice card presentation | [bob-cli-h0.7](bob-cli-h0.7.md) | 2026-11-04 13:32:47 EST |
