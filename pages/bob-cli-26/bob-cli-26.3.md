# Bead: bob-cli-26.3 — Bob Mac Capture start preview and submission

[Bead Pages](../README.md) / [bob-cli-26](README.md) / bob-cli-26.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.20](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.20/README.md) · **Assignee:** `bob-cli-26.3` · **Size:** medium
**Created:** 2026-09-26 16:50:55 EDT · **Closed:** 2026-09-26 17:38:10 EDT
**Plan:** [202609/capture\_start\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_start_pomodoro.md)

## Description

mac-capture: decode Bob's additive start contract and present a polished, accessible session preview.

## Notes

[2026-09-26T21:37:55Z · bob-cli-26.3] PROPOSED FOLLOW-UP: run swift test plus macOS panel UI/a11y checks on a macOS runner — this Linux host has no Swift toolchain (xcode-swift.sh requires macOS SDK 26+), so the new CaptureCore/BobMacCapture tests were authored but not executed here

[2026-09-26T21:38:10Z · bob-cli-26.3] Verified: additive pomodoro_start decodes tolerantly in CaptureParseResponse/Item (incl. array-pair diagnostic ranges) and CaptureCommandSuccess; pomodoro_start span maps to a new pink palette category; #name completion ranges end before = (boundary completes name, suffix interior offers none); session preview (start/end, duration, created state, a11y label) renders from dry-run capture JSON with no Swift-side clock; conflicts surface as preview failures; notifications include the session line. Verified with real-bob contract probes (capture-parse/complete JSON shapes), fake-bob branch probes, bash -n, and balance checks. swift test not runnable on this Linux host (no Swift toolchain); see PROPOSED FOLLOW-UP note.

## Dependencies

- **Depends on:** [bob-cli-26.2](bob-cli-26.2.md) ✓ · ⧖ 2026-09-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-26.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-26.3/README.md) | [bob-cli-26.3](bob-cli-26.3.md) | 0 |
