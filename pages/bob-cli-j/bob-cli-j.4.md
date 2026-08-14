# Bead: bob-cli-j.4 — Capture execution and reliable feedback

[Bead Pages](../README.md) / [bob-cli-j](README.md) / bob-cli-j.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.005](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.005.md) · **Assignee:** `bob-cli-j.4` · **Size:** medium
**Created:** 2026-08-13 20:32:35 EDT · **Closed:** 2026-08-13 22:12:25 EDT
**Plan:** [202608/bob\_mac\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/bob_mac_capture.md)

## Description

feedback: wire submit and explicit clipboard-resolving preview through bob capture, prevent duplicate writes, preserve drafts and destinations on every failure, add inline status, and implement signed UNUserNotificationCenter notifications with foreground presentation, authorization diagnostics, a test action, and Open Note.

## Notes

[2026-08-14T02:11:48Z · bob-cli-j.4] PROPOSED FOLLOW-UP: bobs-org/bob-mac-capture Sources/CaptureCore/CaptureModels.swift CaptureTargetsResponse/CaptureTarget (added in phase foundation/bob-cli-j.3) do not match the real bob capture-targets --format json contract. Verified against both the installed bob binary and current bob-cli source (src/native/capture_targets.rs CaptureTargetsResult/CaptureTarget): real output is {ok, bob_dir, count, targets:[{route, name, label, kind, is_default, status, relative_path}]} with no schema_version, while the Swift model expects {ok, schema_version, targets:[{route, title, sections, aliases}]}. Because BobProcessClient.decode() requires schema_version, every real captureTargets() call currently fails to decode (CaptureTargetsCache silently reports it as a stale-cache diagnostic, so nothing crashes, but the launch-time target cache never actually populates from a real bob). This is unrelated to phase feedback (which never calls captureTargets()) but will block phase intelligence completion UI unless fixed first — its own tests currently only exercise a fake-bob fixture that was written to match the same wrong shape, so the drift is not caught by existing coverage.

[2026-08-14T02:11:58Z · bob-cli-j.4] PROPOSED FOLLOW-UP: Run the bobs-org/bob-mac-capture macOS CI gate (swift-format lint, swift build, swift test, bundle assembly, plutil, codesign verify) after this phase commit is pushed — this Linux worker implemented submit/preview wiring through bob capture, a rebuilt CaptureCommandResponse/CaptureCommandSuccess/Failure model matching the real (schema_version-less) bob capture JSON contract, UNUserNotificationCenter notifications (delegate, categories, Open Note action, test action, authorization display), an Obsidian open-URL helper, a codesign-based signing diagnostic, and new/updated tests, but cannot execute Swift/AppKit/UserNotifications/plutil/codesign locally. Two independent fresh-context reviews of the diff were run in place of a compiler; the first found and this worker fixed one real actor-isolation bug (NotificationService static content/category/routing helpers needed nonisolated so synchronous unit tests could call them), the second found no further issues, but neither substitutes for the real macOS toolchain.

[2026-08-14T02:12:25Z · bob-cli-j.4] Wired bob-mac-capture's capture panel submit/preview through bob capture. Fixed CaptureCommandResponse to match the real (schema_version-less) bob capture JSON success/failure contract instead of foundation's fictional shape, and removed the non-existent --open flag. Added double-submit/late-callback suppression via a shared activeRequestID, failure-preserving draft/destination state with Retry/Copy Diagnostic and accessibility focus, an explicit clipboard-resolving preview action asserted to omit --no-clip, an Obsidian open-URL helper built from the returned absolute target (scheme verified against chezmoi Hammerspoon's obsidianOpenUrl for parity), a UNUserNotificationCenter NotificationService (delegate set before authorization, foreground presentation, Open Note category/action, test notification, live authorization display, nonisolated pure content/routing builders for testability), and a codesign-based signing diagnostic surfaced in Settings/README. Added/extended CaptureCore and BobMacCapture unit tests and corrected the fake-bob fixture's capture JSON to the real schema. Verified locally: git diff --check clean, bash -n on the fixture, fixture JSON exercised through python3 -m json.tool for every new capture()/preview()/ok:false path and argv recording, no trailing whitespace, primary bob-cli workspace untouched. No Swift toolchain exists on this Linux host, so swift build/test/bundle/codesign could not run directly; ran two independent fresh-context agent reviews as a substitute correctness pass instead — the first caught and this worker fixed a real actor-isolation bug (NotificationService's static content/category/routing helpers needed nonisolated so synchronous unit tests could call them), the second confirmed the fix and found nothing further. Filed PROPOSED FOLLOW-UP notes for (1) a pre-existing capture-targets schema mismatch discovered during this work (out of scope for this phase, will block phase intelligence) and (2) running the macOS CI gate once this commit is pushed.

[2026-08-14T02:12:55Z · bob-cli-j.4] Implemented feedback phase: CaptureCommandResponse/Success/Failure models fixed to match real bob capture --format json contract (no schema_version, removed nonexistent --open flag); CapturePanelModel.submit()/preview() wired through BobProcessClient with double-submit suppression, failure-preserving state, Retry/Copy Diagnostic, and accessibility focus on errors; added Obsidian open-URL helper verified against chezmoi Hammerspoon implementation; implemented UNUserNotificationCenter-backed NotificationService with nonisolated pure builders; added codesign-based signing-state diagnostic; updated docs/tests including fake-bob fixture JSON shape. Verified via two independent fresh-context agent reviews (no Swift toolchain available on this host) — first caught and fixed an actor-isolation bug, second confirmed the fix and found no further issues.

## Dependencies

- **Depends on:** [bob-cli-j.3](bob-cli-j.3.md) ✓ · ⧖ 2026-08-13
- **Blocks:** [bob-cli-j.6](bob-cli-j.6.md) ◐ · ⧖ 2026-08-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j.4/README.md) | [bob-cli-j.4](bob-cli-j.4.md) | 0 |
