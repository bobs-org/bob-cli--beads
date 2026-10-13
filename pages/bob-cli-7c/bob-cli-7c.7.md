# Bead: bob-cli-7c.7 — Bob Mac Capture in-panel pull-in choice step

[Bead Pages](../README.md) / [bob-cli-7c](README.md) / bob-cli-7c.7

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.11.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.11.linker.w0.md) · **Assignee:** `bob-cli-7c.7` · **Size:** large
**Created:** 2026-10-13 09:48:12 EDT
**Plan:** [202610/successor\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_offers.md)

## Description

mac_choice: decode offer/pull_in fields, number offer rows on the preview cards, add a keyboard multi-select choice step on Return, pass --pull-in on submit, use the --require-pull-in-choice race guard, fix missing copy, and verify on macOS CI.

## Notes

[2026-10-13T19:41:23Z · bob-cli-7c.7--6] Verification evidence for mac_choice (not closed yet; GitHub CI on the published commit is still outstanding).

Implemented in linked bob-mac-capture: decode offer/pull_in contract fields; in-panel successor choice on Return; confirm passes opaque keys via --pull-in; Shift-Return sends none; Esc restores the unchanged draft; --require-pull-in-choice race guard with one write-free clap-unknown retry; README/key/copy updates; fake-bob fixtures and focused tests.

Portable-check: green. Monitor 0aynq1d58b1c, exit 0, ~66s. Refreshed athena scratch /tmp/bmc-successor-choice.7zsUiQ from this working tree, then `just portable-check`. Tool run 43f579748f5fd3cd50c426f6048fe2af.

Local macOS scratch on host mac: app product compiled. Monitor bfg74j4geae9. `./Scripts/bundle.sh --identity -` then `./Scripts/xcode-swift.sh build --build-tests`. Log line: "Build of product 'BobMacCapture' complete! (35.91s)". Test-target build failed with `error: no such module 'XCTest'` starting at Tests/CaptureCoreTests/ActiveTaskPickerPresentationTests.swift:1. Earlier authored Color.tertiary compile error in CapturePanelView.swift was fixed before this rerun. Clean-HEAD scratch /tmp/bmc-successor-choice-clean-head reproduced the same XCTest import failure while compiling the app. Isolated scratches /tmp/bmc-successor-choice.20261013.1918 and /tmp/bmc-successor-choice-clean-head were deleted after that comparison. Installed app/checkouts were not touched.

GitHub Actions CI (formatting, Build, Test, Bundle, signature, launch, install) has not yet run on the commit that will publish this tree; that remains the close gate.

[2026-10-13T19:41:41Z · bob-cli-7c.7--6] PROPOSED FOLLOW-UP: host mac Swift toolchain cannot import XCTest — Isolated scratch ./Scripts/xcode-swift.sh build --build-tests fails with no such module XCTest on Tests/CaptureCoreTests/ActiveTaskPickerPresentationTests.swift:1 after BobMacCapture compiled. Reproduced on clean HEAD at 2837025 in /tmp/bmc-successor-choice-clean-head with the same toolchain/command (monitor bfg74j4geae9). Out of scope for this phase; GitHub macos-26 CI remains the test-runner authority. Do not treat this host failure as an authored regression.

## Dependencies

- **Depends on:** [bob-cli-7c.3](bob-cli-7c.3.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.8](bob-cli-7c.8.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7c.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.7.md) | [bob-cli-7c.7](bob-cli-7c.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@395c521`](https://github.com/bobs-org/bob-mac-capture/commit/395c5217523aaf28e81f38c8ef5d471d0e9725e7) | feat(capture): add in-panel successor pull-in choice | [bob-cli-7c.7](bob-cli-7c.7.md) | 2026-10-13 15:43:32 EDT |
