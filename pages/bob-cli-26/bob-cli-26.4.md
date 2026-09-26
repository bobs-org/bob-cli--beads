# Bead: bob-cli-26.4 — Finish macOS verification of atomic Pomodoro capture

[Bead Pages](../README.md) / [bob-cli-26](README.md) / bob-cli-26.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-26.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-26.land.md) · **Assignee:** `bob-cli-26.4.land`
**Created:** 2026-09-26 17:47:03 EDT · **Closed:** 2026-09-26 18:58:45 EDT
**Plan:** [202609/pomodoro\_mac\_verification.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_mac_verification.md)

## Description

Bob Mac Capture compiles and passes its tests with the additive Pomodoro start contract, and the panel presents the resolved session accessibly.

## Notes

[2026-09-26T22:18:28Z · bob-cli-26.4.land] LAND VERIFY: Phases bob-cli-26.4.1 and bob-cli-26.4.2 are closed. Decoder fix is commit 7282a7a in bob-mac-capture (CaptureDiagnostic flattens try?/decodeIfPresent; testCaptureDiagnosticDecodesAllRangeShapesTolerantly). swift build of CaptureCore succeeds on host mac (Swift 6.3.2, CLT). No commits after the epic started except that fix; nothing to integrate in bob-cli or bob-mac-capture. No --epic-symbol entries.

DISCOVERED ISSUE: GitHub Actions run 36274365429 on 7282a7a (macOS 26 SwiftPM) built cleanly then failed swift test: 503 tests, 1 failure. CapturePanelModelTests.testPlusCommitsGlobalRouteDeclarationAndOpensTaskPicker at CapturePanelModelTests.swift:1911 XCTAssertTrue failed. Earlier asserts in that test passed (draft @@mac_inbox+ plus newline First task, caret 12, completion context task; no waitUntil timeout). fake-bob returns context task for that draft at any cursor, so the recorded capture-complete argv is not cursor 12 with that exact draft. Base 54861b3 was green; 7fae3fd never compiled. This is remaining epic work. Host mac cannot run swift test (no such module XCTest). Planning a child tale; do not close this epic yet.

PROPOSED FOLLOW-UP from bob-cli-26.4.2 (equip host mac 100.108.201.99 with full Xcode 26+ so XCTest imports): declined as a task bead. The matching catalog type is feature, which agents must not create, and the request is host administration outside the repo. README already says to select Xcode or Command Line Tools when import XCTest fails. CI macos-26 already runs swift test. Not refiled under another type.

[2026-09-26T22:58:45Z · bob-cli-26.4.3.land] Rechecked phases bob-cli-26.4.1/.2 and closed child epic bob-cli-26.4.3 against the linked plan. Mac commits 7282a7a (tolerant diagnostic range decoder and object/pair/null/absent/malformed test) and 1a5f7a5 (serialized fake-bob multiline record writes) are present; panel source renders Bob-owned session timing/destination and accessibility text. macOS 26 CI run 36277377633 passed build and all 503 Swift tests, including the prior global plus-commit failure and diagnostic decoder test, plus bundle/smoke/install. The local mac host still lacks XCTest and a GUI session, which bob-cli-26.4.2 documented; CI resolves the automated verification requirement. No later non-epic commits in bob-cli or the Mac base branch require integration. The sole PROPOSED FOLLOW-UP from bob-cli-26.4.2, installing full Xcode on the host, was declined in the prior landing note as host administration outside the agent-creatable task catalog; CI provides coverage. All descendant beads are closed, this linked epic plan validates, and no --epic-symbol entries remain. Global plan-link/bead-doctor findings concern older unrelated archive/event history; this repo has no just check or symvision recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-26.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-26.4.land.md) | [bob-cli-26.4](bob-cli-26.4.md) | 0 |
