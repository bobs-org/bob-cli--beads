# Bead: bob-cli-fn.5.2 — Undoable ID splices and section picks in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-fn.5](bob-cli-fn.5.md) / bob-cli-fn.5.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fn.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fn.land.md) · **Assignee:** `bob-cli-fn.5.2` · **Size:** medium
**Created:** 2026-11-02 07:14:36 EST · **Closed:** 2026-11-02 10:18:17 EST
**Plan:** [202611/capture\_list\_section\_names.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_list_section_names.md)

## Description

mac-undo: apply an accepted block-ID splice as one native undoable NSTextView edit, insert Bob's section replacement verbatim (including quoted literals), treat the new `section` need as a calm incomplete state, regenerate list and section fixtures from the phase-1 bob, and verify on macOS CI.

## Notes

[2026-11-02T14:33:17Z · bob-cli-fn.5.2--1] macOS CI run 41459735666 (snapshot 66fcbbc82fee46686a26f76c287435980c8dc15c, base 6c7cf3021e6a137b5e13c12107d163d99095e5a) FAILED Test step: 28 failures = 21 tracked base (bob-cli-f3 7 + bob-cli-fu 14) + 7 new CaptureListPanelTests undo (testNestedAcceptIsOneNativeUndoStep, testSameLineAcceptIsOneNativeUndoStep, testOwnerIDReplacementIsOneNativeUndoStep, testTypeThroughRemainderIsOneNativeUndoStep, testProjectNoteNestedIsOneNativeUndoStep, testOlderBobFallbackIsOneNativeUndoStep, testUnrelatedTypingHistorySurvivesTheSplice). Root cause: new tests used windowless NSTextView which has no undoManager, so canUndo false and undo silently no-ops (cf. CaptureSeparatorToggleTests comment). Fix applied in linked bob-mac-capture: makeHostedTextView hosts each undo test textView in NSWindow. Re-running Scripts/macos-ci-check. Section-pick tests passed in same run.

[2026-11-02T14:54:51Z · bob-cli-fn.5.2--2] macOS CI run 41463131070 (snapshot 2031d2726c1803ac618438c0354c7cb39e49d8c9, base 6c7cf3021e6a137b5e3c12107d163d99095e5a5) FAILED Test step: 22 failures = 21 tracked base (bob-cli-f3 7 + bob-cli-fu 14) + 1 remaining new CaptureListPanelTests.testUnrelatedTypingHistorySurvivesTheSplice. 6 of 7 new undo tests now pass after window-hosting fix. Remaining failure is a test artifact, not production: typing " " and the splice run in the same test event so NSUndoManager coalesces them; first undo jumps to nestedDraft instead of typed (line 505) and canUndo is false (line 506). Real typing and picker accept are separate key events. Fix applied in linked bob-mac-capture: testUnrelatedTypingHistorySurvivesTheSplice is now async with breakUndoCoalescing plus an 80ms runloop turn between typing and accept, matching the passing testNativeUndoAndRedoDoNotRetriggerAssist pattern. Re-running Scripts/macos-ci-check.

[2026-11-02T15:18:01Z · bob-cli-fn.5.2--3] macOS CI run 41466582525 (snapshot f6cab4f270a19e186bea9450b8e48c5eda2287ab) FAILED Test step with 21 failures, all tracked base (bob-cli-f3 7 + bob-cli-fu 14), zero CaptureListPanelTests failures. All 7 new undo tests now pass: testNestedAcceptIsOneNativeUndoStep, testSameLineAcceptIsOneNativeUndoStep, testOwnerIDReplacementIsOneNativeUndoStep, testTypeThroughRemainderIsOneNativeUndoStep, testProjectNoteNestedIsOneNativeUndoStep, testOlderBobFallbackIsOneNativeUndoStep, testUnrelatedTypingHistorySurvivesTheSplice. Remaining 21: 11 CaptureClipPreviewHostedTests, CaptureEditorLeaderTests.testToggleLineCaseUndoRestoresOriginalLine, 3 CapturePanelModelTests (testBlockIDLinkCommandAcceptSubmits, testCommandAcceptInsertsAndSubmits, testTaskTypeRetypeMoveKeepsDraftAndUsesEnsureNextAction), CapturePullInChoiceModelTests.testRealKeepMovingFixtureOpensChoiceAndSubmitsItsOpaqueKey, 3 CaptureSeparatorToggleTests, 2 CaptureTaskTypeHostedTests. Fix verified in linked bob-mac-capture working tree: makeHostedTextView hosts in NSWindow, unrelated-history test is async with breakUndoCoalescing + 80ms runloop turn.

[2026-11-02T15:18:17Z · bob-cli-fn.5.2--3] macOS CI run 41466582525 verified: all 7 CaptureListPanelTests undo tests pass (nested, same-line, owner-ID, type-through, project-note, older-Bob, unrelated-history), 21 remaining failures are tracked base only (bob-cli-f3 7 + bob-cli-fu 14). sase bead epic-symbols clean. Fix in linked bob-mac-capture: window-hosted NSTextView for native undo plus async breakUndoCoalescing with 80ms runloop turn for unrelated-history test.

## Dependencies

- **Depends on:** [bob-cli-fn.5.1](bob-cli-fn.5.1.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fn.5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fn.5.2.md) | [bob-cli-fn.5.2](bob-cli-fn.5.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@f4ed5bb`](https://github.com/bobs-org/bob-mac-capture/commit/f4ed5bbcb3c8c07384a9dec3190127eea46eba3c) | feat(mac-capture): undoable ID splices with window-hosted native undo tests | [bob-cli-fn.5.2](bob-cli-fn.5.2.md) | 2026-11-02 10:19:33 EST |
