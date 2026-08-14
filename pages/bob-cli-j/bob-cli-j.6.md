# Bead: bob-cli-j.6 — Integrated macOS validation and release hardening

[Bead Pages](../README.md) / [bob-cli-j](README.md) / bob-cli-j.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.005](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.005.md) · **Assignee:** `bob-cli-j.6` · **Size:** medium
**Created:** 2026-08-13 20:32:35 EDT · **Closed:** 2026-08-13 22:58:43 EDT
**Plan:** [202608/bob\_mac\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/bob_mac_capture.md)

## Description

hardening: complete app accessibility, appearance, privacy, error, packaging, installation, and user documentation; exercise core and full-app CI; and run the owner-assisted signed on-Mac notification, focus, clipboard, Spaces, IME, latency, and smoke-test gate without changing the existing Hammerspoon hotkey.

## Notes

[2026-08-14T02:58:25Z · bob-cli-j.6] PROPOSED FOLLOW-UP: the owner-assisted on-Mac release gate and a green macOS CI run for this commit still need to happen before bob-cli-j.7 (cutover) can proceed. This Linux SASE agent implemented and reviewed the code-level hardening (product hardening + automated-gate prerequisites) but cannot run swift build/test, codesign, or any of the physical-Mac checks (notification authorization/test notification/Open Note while the panel is visible, hotkey-to-focused-editor latency across 30+ invocations/Spaces/full-screen with p50<50ms and p95<100ms, IME/VoiceOver/light-dark/multi-display/secure-input behavior, route/section/task completion parity against bob, rapid-submit dedup, launch-at-login surviving logout/login). Needs: push this branch, confirm macOS CI is green, then the owner runs the installed-app checklist in the plan's hardening phase section and records the results before j.7 begins.

[2026-08-14T02:58:43Z · bob-cli-j.6] Implemented the feasible product-hardening slice of this phase in bobs-org/bob-mac-capture (code-level only; no Swift toolchain or Mac hardware on this Linux host): (1) BobProcessClient.run() now bounds every bob invocation with a 20s timeout that terminates and reaps a wedged process instead of hanging the panel forever, via a new BobClientError.timedOut case; (2) added Sources/BobMacCapture/Signposts.swift (CaptureSignpost, an os.OSSignposter wrapper) instrumenting hotkey receipt, panel ordering, editor focus, parse, completion, preview, submit, and notification scheduling, all metadata-only; (3) accessibility: empty-draft placeholder, VoiceOver focus/announcement on capture success and on errors, completion-list/-row accessibility labels/traits; (4) menu-bar glyph now reflects an unresolved bob; (5) AppSettings.diagnosticStatus changes now feed a bounded 20-entry diagnosticHistory shown in Settings; (6) Scripts/install.sh now verifies the staged bundle before touching the install path and does a backup-and-swap with automatic rollback if the move or post-install codesign verify fails; (7) README gained Keyboard, Live Preview/Clipboard, Hotkey Conflicts/Login Item, Updating/Rollback, Uninstalling, Privacy, Troubleshooting, and Diagnostics/Signposts sections. Verified via git diff --check (clean), bash -n on all three shell scripts, brace/paren balance checks against the pre-existing baseline, added CaptureCoreTests (timeout throws/terminates the process, and completes normally under the timeout) and a BobMacCaptureTests case for the bounded diagnostic history, and two independent fresh-context agent reviews (no Swift compiler available, so review-by-reading): the first review caught a real same-queue reentrant deadlock in the new timeout path (the DispatchWorkItem ran on stateQueue but called a method that did stateQueue.sync, which would have hung that call forever and wedged the client for all future calls too) — fixed by splitting out a lock-free clearActiveProcessAlreadyOnStateQueue helper for that call site; the second review confirmed the fix and found one minor cleanup gap in install.sh's failure path (a leftover tmp_path on move failure), which is also fixed. Both reviewers found no other correctness, actor-isolation, or privacy-redaction issues. NOT done here and recorded as a PROPOSED FOLLOW-UP: the owner-assisted on-Mac release gate and a green macOS CI run, both of which require pushing this branch and physical Mac hardware — j.7 (cutover) should not begin until those are recorded as passing per the plan's hardening-phase release gate.

[2026-08-14T02:59:10Z · bob-cli-j.6] Implemented BobProcessClient timeout/reaping hardening with os.signpost instrumentation, accessibility improvements (empty-state, VoiceOver announcements, completion-list traits), menu-bar problem indicator, bounded diagnostic history in Settings, atomic install.sh with rollback, and README documentation. Fixed a same-queue reentrant deadlock in the timeout path found during first review; second review confirmed the fix and caught a minor install.sh tempfile cleanup gap, also fixed. Added tests. Deferred macOS CI/on-Mac release gate recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-j.4](bob-cli-j.4.md) ✓ · ⧖ 2026-08-13
- **Depends on:** [bob-cli-j.5](bob-cli-j.5.md) ✓ · ⧖ 2026-08-13
- **Blocks:** [bob-cli-j.7](bob-cli-j.7.md) ◐ · ⧖ 2026-08-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j.6/README.md) | [bob-cli-j.6](bob-cli-j.6.md) | 0 |
