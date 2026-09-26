# Bead: bob-cli-26.4 — Finish macOS verification of atomic Pomodoro capture

[Bead Pages](../README.md) / [bob-cli-26](README.md) / bob-cli-26.4

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-26.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-26.land.md) · **Assignee:** `bob-cli-26.4.land`
**Created:** 2026-09-26 17:47:03 EDT
**Plan:** [202609/pomodoro\_mac\_verification.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_mac_verification.md)

## Description

Bob Mac Capture compiles and passes its tests with the additive Pomodoro start contract, and the panel presents the resolved session accessibly.

## Notes

[2026-09-26T22:18:28Z · bob-cli-26.4.land] LAND VERIFY: Phases bob-cli-26.4.1 and bob-cli-26.4.2 are closed. Decoder fix is commit 7282a7a in bob-mac-capture (CaptureDiagnostic flattens try?/decodeIfPresent; testCaptureDiagnosticDecodesAllRangeShapesTolerantly). swift build of CaptureCore succeeds on host mac (Swift 6.3.2, CLT). No commits after the epic started except that fix; nothing to integrate in bob-cli or bob-mac-capture. No --epic-symbol entries.

DISCOVERED ISSUE: GitHub Actions run 36274365429 on 7282a7a (macOS 26 SwiftPM) built cleanly then failed swift test: 503 tests, 1 failure. CapturePanelModelTests.testPlusCommitsGlobalRouteDeclarationAndOpensTaskPicker at CapturePanelModelTests.swift:1911 XCTAssertTrue failed. Earlier asserts in that test passed (draft @@mac_inbox+ plus newline First task, caret 12, completion context task; no waitUntil timeout). fake-bob returns context task for that draft at any cursor, so the recorded capture-complete argv is not cursor 12 with that exact draft. Base 54861b3 was green; 7fae3fd never compiled. This is remaining epic work. Host mac cannot run swift test (no such module XCTest). Planning a child tale; do not close this epic yet.

PROPOSED FOLLOW-UP from bob-cli-26.4.2 (equip host mac 100.108.201.99 with full Xcode 26+ so XCTest imports): declined as a task bead. The matching catalog type is feature, which agents must not create, and the request is host administration outside the repo. README already says to select Xcode or Command Line Tools when import XCTest fails. CI macos-26 already runs swift test. Not refiled under another type.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-26.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-26.4.land.md) | [bob-cli-26.4](bob-cli-26.4.md) | 0 |
