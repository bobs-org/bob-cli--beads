# Bead: bob-cli-j.7 — Hammerspoon cutover and migration cleanup

[Bead Pages](../README.md) / [bob-cli-j](README.md) / bob-cli-j.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.005](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.005.md) · **Assignee:** `bob-cli-j.7` · **Size:** small
**Created:** 2026-08-13 20:32:35 EDT · **Closed:** 2026-08-14 08:03:20 EDT
**Plan:** [202608/bob\_mac\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/bob_mac_capture.md)

## Description

cutover: only after the hardening gate passes, remove the old Hammerspoon hotkey, WebView workflow, duplicated task_capture.lua grammar, and migrated specs from chezmoi; deploy the dotfiles change and document rollback to the last known-good Hammerspoon revision.

## Notes

[2026-08-14T12:03:17Z · 00o] PROPOSED FOLLOW-UP: finish the target-Mac cutover after these phase changes land — run the required post-commit chezmoi update -a --force on the Mac, reload Hammerspoon, install/restart Bob Mac Capture, confirm RegisterEventHotKey makes only the app own Control-Shift-Command-I, and rerun capture, foreground-notification, clipboard, and draft-retention smoke tests; this Linux host could apply and syntax-check only its local deployed Hammerspoon tree.

[2026-08-14T12:03:20Z · 00o] Verified the Hammerspoon cutover source and local deployment: removed only the contiguous TaskCapture/WebView/picker/subprocess/notification/hotkey block, deleted task_capture.lua and its migrated spec, preserved screenshot and Bob Pomodoro runtimes, documented rollback to chezmoi revision 3d841c1e9c6dac9f558709a6ba6ef36082c2c4d4 plus the app's Control-Shift-Command-O preference, and applied the linked source to ~/.hammerspoon with the retired deployed module moved to Trash. Confirmed deployed init.lua byte-matches source, task_capture.lua is absent, retired references are absent, stylua/luac/just lint-lua/git diff --check pass, remaining Hammerspoon tests pass 4/4, and all 11 Rust tests ported from the Lua grammar pass. Bob Mac Capture now defaults new installs to Control-Shift-Command-I while preserving an explicit rollback preference; swift parse, format lint, CaptureCore Linux build, and git diff --check pass, and current master macOS CI at ef64f0a is green. Target-Mac reload, Carbon ownership, and interaction smoke checks are recorded as a PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-j.6](bob-cli-j.6.md) ✓ · ⧖ 2026-08-13
