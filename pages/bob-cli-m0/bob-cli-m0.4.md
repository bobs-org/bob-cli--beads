# Bead: bob-cli-m0.4 — Ring, card, minimap, and motion painter

[Bead Pages](../README.md) / [bob-cli-m0](README.md) / bob-cli-m0.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e9.md) · **Assignee:** `bob-cli-m0.4` · **Size:** medium
**Created:** 2026-11-15 20:01:48 EST · **Closed:** 2026-11-16 07:18:08 EST
**Plan:** [202611/obsidian\_ctrl\_w\_window\_prefix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_window_prefix.md)

## Description

hint: paint the armed ring, key-cap badge, hint card with minimap, nudges, pulses, and receipts from the view model, with a light/dark preview harness.

## Notes

[2026-11-16T11:48:54Z · bob-cli-m0.4] PROPOSED FOLLOW-UP: bob-plugins npm test still fails on clean origin/master with Chromium PATH hard-fail in test-command-mode-sheet-sequence-dom.cjs (closed bob-cli-f1 was supposed to skip) and block-marks e2e relative-date failures; load-flake perf budgets also fail under the full suite. Does not block this painter phase.

[2026-11-16T12:18:08Z · bob-cli-m0.4--1] Painter landed in bob-plugins: createWindowHintHost, Window prefix CSS, preview harness, and 11 hint-view unit tests. Fast-forwarded onto 4678586 (m0.3 adapter) via stash/ff-only/sync/stash-pop with no -F; renamed adapter windowPrefixLeafLabel to windowPrefixLiveLeafLabel so it no longer shadows the model helper. Window-prefix unit tests 33/33, build:check, and bob plugins sync of bob-navigation-hotkeys all passed. epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-m0.2](bob-cli-m0.2.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-m0.5](bob-cli-m0.5.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-m0.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-m0.4.md) | [bob-cli-m0.4](bob-cli-m0.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1a9e304`](https://github.com/bobs-org/bob-plugins/commit/1a9e304d828b36c5735fcb42ccf14a43e894e8ea) | feat(navigation): paint Ctrl+W window-prefix hint | [bob-cli-m0.4](bob-cli-m0.4.md) | 2026-11-16 07:20:22 EST |
