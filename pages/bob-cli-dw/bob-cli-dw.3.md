# Bead: bob-cli-dw.3 — Restore the unconfigured-theme caret-underline XCTests on macOS CI

[Bead Pages](../README.md) / [bob-cli-dw](README.md) / bob-cli-dw.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-dp.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dp.land.md) · **Assignee:** `bob-cli-dw.3` · **Size:** large
**Created:** 2026-10-28 15:35:24 EDT · **Closed:** 2026-10-28 15:48:22 EDT
**Plan:** [202610/backlog\_batch\_b6.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b6.md)

## Description

mac-unconfigured-theme-ci: resolve bob-cli-dr in bob-mac-capture. Master macOS 26 SwiftPM Test has failed on every push since 8b57693 with the same four assertions in CapturePanelModelTests.testCaretLeavingUnconfiguredThemeUnderlinesAfterAnalysis and CaptureUnconfiguredThemeHostedTests.testTypingUnconfiguredThemeThenMovingCaretUnderlinesWithoutFreezing (timeout then XCTAssertTrue at the caret-underline lines). Runs 40724077224 (8b57693), 40728493998 (ebb798a attempted fix), and 40729693701 (e5f6604) all report four failures; Bundle/launch/install are skipped, so master has no green macOS signal. Open bob-mac-capture through sase repo open. The failures predate bob-cli-dl.7 and touch only the unconfigured-theme dashed underline from 8b57693. Verify on the Mac CI path named by the task; do not invent a local green as a substitute for that CI signal. Never run just check-full.

## Notes

[2026-10-28T19:42:27Z · bob-cli-dw.3] PRE-PLAN VERIFIED: Work already landed in bob-mac-capture commit 2c3407d6c096bbc7617313b63434dcae7cd2654b (explicit empty underline style), ancestor of current master c8c4366d897baab836b4f05693aede4ca0a01a51. macOS 26 SwiftPM run https://github.com/bobs-org/bob-mac-capture/actions/runs/40746228778 (job 123020643000) passed 3265 tests with zero failures, both named caret tests, no-selection-write regression, Bundle, signature, launch smoke, and install/reinstall. Current master run 40750655496 (job 123036129488) also passed both caret tests (0.108s model; 1.405s hosted) and no-selection-write test. No source changes needed for this phase. No epic-symbol entries. Preparing the user-required validated tale for verification and closeout; leave bob-cli-dr and bob-cli-dw to the epic land agent.

[2026-10-28T19:42:38Z · bob-cli-dw.3] PROPOSED FOLLOW-UP: Current bob-mac-capture master has an unrelated refused-cancel relation-row assertion failure — clean-base SHA c8c4366d897baab836b4f05693aede4ca0a01a51, macOS 26 SwiftPM run https://github.com/bobs-org/bob-mac-capture/actions/runs/40750655496 (job 123036129488), CaptureRelationPanelTests.testRefusedCancelRowsUseLabelKeysAndKeepTheReasonVisible at line 1566 expects Optional("1 link") but receives Optional("one-off · 1 link"). This is the only failure among 3267 tests; both caret-underline tests pass. Introduced test is in c8c4366, after fully green caret fix 2c3407d. Read-only investigation made no source changes. Searches for RefusedCancel and relation_card_refused_cancel_rows found no tracking bead. Land agent should triage against plan:202610/relation_card_refused_cancel_rows.md; do not fold it into the already-fixed caret scope.

[2026-10-28T19:48:22Z · bob-cli-dw.3] Repair already landed as 2c3407d (paintHighlighting overwrites theme range with NSUnderlineStyle([]) + clears underline color while caret in name). Verified macOS 26 SwiftPM run 40746228778 job 123020643000 on full SHA 2c3407d: SUCCESS, 3265 tests 0 failures; testCaretLeavingUnconfiguredThemeUnderlinesAfterAnalysis passed (0.067s), testTypingUnconfiguredThemeThenMovingCaretUnderlinesWithoutFreezing passed (1.351s), plus testCaretMoveWithUnconfiguredThemeDoesNotRewriteEditor and testUnconfiguredThemeHasNoMarkWhileCaretIsInTheName; Bundle, Verify plist/signature, Launch smoke, Install/reinstall all passed. Current master c8c4366 (descendant, relation-row changes only) run 40750655496 job 123036129488: both caret tests still pass (0.108s / 1.405s) plus no-selection-write regression; sole failure among 3267 is unrelated CaptureRelationPanelTests.testRefusedCancelRowsUseLabelKeysAndKeepTheReasonVisible at line 1566 (Optional one-off 1 link vs 1 link), preserved as PROPOSED FOLLOW-UP for epic-land triage against plan:202610/relation_card_refused_cancel_rows.md. No source changes made; no epic-symbols.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dw.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dw.3.md) | [bob-cli-dw.3](bob-cli-dw.3.md) | 0 |
