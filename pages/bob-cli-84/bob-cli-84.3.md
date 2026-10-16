# Bead: bob-cli-84.3 — Highlights-only Accessibility reader

[Bead Pages](../README.md) / [bob-cli-84](README.md) / bob-cli-84.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7w.md) · **Assignee:** `bob-cli-84.3` · **Size:** medium
**Created:** 2026-10-15 17:50:48 EDT · **Closed:** 2026-10-16 07:20:31 EDT
**Plan:** [202610/highlights\_tabs\_switcher.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tabs_switcher.md)

## Description

ax-reader: `AXHighlightsTabsReader` in BobMacCapture implements the RefsCore reader protocol, using only public AX API against Highlights' process. It never launches Highlights, never prompts, and works off the main actor with messaging timeouts and a time budget. It reads window AXDocument and the native tab bar, and presses one verified tab button for select. Tab names stay in memory only. An optional read-only probe runs on the Mac.

## Notes

[2026-10-16T11:20:14Z · bob-cli-84.3] PROPOSED FOLLOW-UP: Add the skipped decisions record stating Bob Mac Capture uses Accessibility only to read and select Highlights tabs (epic decision decision_record=no; land agent to triage)

[2026-10-16T11:20:20Z · bob-cli-84.3] PROPOSED FOLLOW-UP: Scripts/typecheck-tests.sh fails on CLT-only Macs because its bare swiftc stub/test invocations lack -sdk (unable to load standard library for arm64-apple-macosx26.0); pass the macOS SDK explicitly. Same environment also exposes that Scripts/typecheck/XCTest.swift lags real XCTest (async XCTAssertEqual in RefsInspectorTests fails against the stub but passes in CI)

[2026-10-16T11:20:31Z · bob-cli-84.3] Implemented AXHighlightsTabsReader (Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift, commit 284fe9b in bob-mac-capture) plus AXHighlightsTabsReaderTests (.notRunning for read/select with unknown bundle id, never launches). Verified: swift-format lint exit 0; Scripts/bundle.sh exit 0 on mac scratch; manual swiftc typecheck of BobMacCaptureTests clean for new files (4 remaining errors proven identical on base tree: XCTest-stub async-assert lag); just portable-check on athena exit 0 (1236 tests pass). Read-only live probe vs Bryan's Highlights (10-tab window): 1 window, main, title+doc present, tabgroup at depth 1, 10 tabs, 1 selected; counts/shapes only, script deleted with scratch.

## Dependencies

- **Depends on:** [bob-cli-84.1](bob-cli-84.1.md) ✓ · ⧖ 2026-10-15
- **Depends on:** [bob-cli-84.2](bob-cli-84.2.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-84.6](bob-cli-84.6.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-84.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.3/README.md) | [bob-cli-84.3](bob-cli-84.3.md) | 0 |
