# Bead: bob-cli-27.3 — Show Pomodoro adjustments in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-27](README.md) / bob-cli-27.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.21](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.21.md) · **Assignee:** `bob-cli-27.3` · **Size:** medium
**Created:** 2026-09-26 19:06:51 EDT · **Closed:** 2026-09-26 19:47:54 EDT
**Plan:** [202609/adjust\_pomodoro\_duration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/adjust_pomodoro_duration.md)

## Description

mac_presentation: decode Bob's additive adjustment result and present accurate dry-run and committed before/after timing in Mac Capture, with fixtures and tests.

## Notes

[2026-09-26T23:47:54Z · bob-cli-27.3] mac_presentation done: tolerant pomodoro_adjust spec/summary decoding, CapturePomodoroAdjustPresentation (would adjust/adjusted, before-to-after, clamped note), dedicated panel row + accessibility, notification copy (Adjustment kind, day-file subtitle fallback), pomodoro_adjust span maps to Pomodoro palette (no new category), fake-bob +5/-2/+0/-9/mixed/complete fixtures byte-verified against real bob, 26 contract + 8 fidelity checks green. Swift suites authored but not runnable on this Linux host (no toolchain); macOS CI must confirm at land.

## Dependencies

- **Depends on:** [bob-cli-27.2](bob-cli-27.2.md) ✓ · ⧖ 2026-09-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-27.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-27.3/README.md) | [bob-cli-27.3](bob-cli-27.3.md) | 0 |
