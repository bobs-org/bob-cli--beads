# Bead: bob-cli-j.3 — Signed app foundation and macOS CI

[Bead Pages](../README.md) / [bob-cli-j](README.md) / bob-cli-j.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.005](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.005.md) · **Assignee:** `bob-cli-j.3` · **Size:** medium
**Created:** 2026-08-13 20:32:34 EDT · **Closed:** 2026-08-13 21:31:35 EDT
**Plan:** [202608/bob\_mac\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/bob_mac_capture.md)

## Description

foundation: scaffold bobs-org/bob-mac-capture as a macOS 26 SwiftPM app with a pure CaptureCore, direct cancellable bob process client, fixture-backed tests, macOS CI, deterministic bundle/install/sign scripts, LSUIElement lifecycle, Carbon hotkey, pre-warmed non-activating NSPanel, draft-safe multi-line editor, settings, and launch-at-login support.

## Notes

[2026-08-14T01:31:20Z · bob-cli-j.3] PROPOSED FOLLOW-UP: Run the macOS CI gate after the bob-mac-capture scaffold is committed and pushed — this Linux worker created the macOS 26 workflow but cannot execute Swift/AppKit, plutil, or codesign locally.

[2026-08-14T01:31:35Z · bob-cli-j.3] Implemented bobs-org/bob-mac-capture SwiftPM foundation scaffold and verified primary bob-cli workspace is clean; in app repo verified git diff --check, bash -n for scripts/fixture, fixture JSON parsing with python3 -m json.tool, plist parsing with python3 -m plistlib, just recipe parsing, executable modes, and absence of trailing whitespace. Swift/AppKit, plutil, and codesign are unavailable on this Linux host, so macOS CI/signature execution is recorded as a proposed follow-up.

[2026-08-14T01:32:56Z · bob-cli-j.3] Verified app foundation locally with git diff --check, shell syntax checks, fake bob JSON parsing, plistlib Info.plist parsing, just recipe parsing, executable modes, and no trailing whitespace; Swift/AppKit/plutil/codesign validation remains for macOS CI follow-up.

## Dependencies

- **Depends on:** [bob-cli-j.1](bob-cli-j.1.md) ✓ · ⧖ 2026-08-13
- **Blocks:** [bob-cli-j.4](bob-cli-j.4.md) ◐ · ⧖ 2026-08-13
- **Blocks:** [bob-cli-j.5](bob-cli-j.5.md) ✓ · ⧖ 2026-08-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j.3/README.md) | [bob-cli-j.3](bob-cli-j.3.md) | 0 |
