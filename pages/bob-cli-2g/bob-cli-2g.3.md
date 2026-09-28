# Bead: bob-cli-2g.3 — Beautiful picker card, sizing, accessibility, docs, and macOS verification

[Bead Pages](../README.md) / [bob-cli-2g](README.md) / bob-cli-2g.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-2f.3.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.3.w1.md) · **Assignee:** `bob-cli-2g.3` · **Size:** medium
**Created:** 2026-09-28 18:28:11 EDT · **Closed:** 2026-09-28 19:09:34 EDT
**Plan:** [202609/mac\_active\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/mac_active_task_picker.md)

## Description

picker-design: replace the functional view with the final design, including the large card, pinned Pomodoro headers, rich rows, detail strip, empty states, chip, and key-hint footer. Add the fixed-height sizing policy, accessibility announcements, README visuals, rendered-image review, and macOS build, test, and lint verification.

## Notes

[2026-09-28T23:09:24Z · bob-cli-2g.3] PROPOSED FOLLOW-UP: run macOS verification for picker-design (just format-lint build test), the BOB_MAC_CAPTURE_RENDER_DIR rendered-image review with image inspection, and the GUI smoke test (type ^: open, filter, arrow, Return, Cmd-Return, Esc twice, Backspace, chip) — no Swift toolchain on this Linux host and tailnet host mac unreachable (ssh timed out), so the new Swift code is statically checked only

[2026-09-28T23:09:34Z · bob-cli-2g.3] Implemented picker-design in bob-mac-capture: new ActiveTaskPickerView.swift (card, filter bar, pinned headers, rich rows, detail strip, empty states, chip, key hints, height policy, rich-text builder), palette status styles, panel integration (editor dim, footer hints, fixed-height metrics), model preview-install hook, design tests incl. gated render review, README visuals. Verified: epic-symbols clean, no dangling refs to removed functional view, delimiter balance on all touched files, SwiftUI announcement/contrast APIs confirmed; full swift build/test + rendered-image review + GUI smoke test pending on macOS per bead note (no toolchain here, mac host unreachable). Work left uncommitted in external checkout for review.

## Dependencies

- **Depends on:** [bob-cli-2g.1](bob-cli-2g.1.md) ✓ · ⧖ 2026-09-28
- **Depends on:** [bob-cli-2g.2](bob-cli-2g.2.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2g.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2g.3/README.md) | [bob-cli-2g.3](bob-cli-2g.3.md) | 0 |
