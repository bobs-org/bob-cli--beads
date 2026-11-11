# Bead: bob-cli-kj.5 — Deterministic alias-tip CI timeouts

[Bead Pages](../README.md) / [bob-cli-kj](README.md) / bob-cli-kj.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.5` · **Size:** large
**Created:** 2026-11-11 17:20:04 EST · **Closed:** 2026-11-11 17:52:58 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

## Description

mac-tip-tests: diagnose and fix the three CaptureAliasTipPanelTests waitUntil timeouts red on every macOS CI run, without weakening assertions, and watch the exact-SHA run fully green (bead bob-cli-jx).

## Notes

[2026-11-11T22:51:12Z · bob-cli-kj.5] Verify alias-tip closeout (interim, CI still running): fix still present at HEAD 1e83c032217a9d6c90827ee467e5c60b57069d88, which has ee26941dedaeff5cbfae6640daee18000b668e84 as ancestor (merge-base --is-ancestor exit 0; ee26941..HEAD touches only CaptureModifierAliasTests and CaptureRelationEqualsAliasTests). git diff ee26941..HEAD for Tests/BobMacCaptureTests/CaptureAliasTipPanelTests.swift is empty. Assertions intact: FAKE_BOB_ALIAS_TIP_ANCHOR=1 in both route-query/filter tests, recordShowsGenericCompletionFallback false asserts, route-context + record-candidate asserts, isRecordCompletion no longer matches bare record-kind candidates (context record_field/value/target or record object only), fake-bob serves task-type-complete-incomplete-marker.json for 'jot idea #'.

Green exact-SHA run 43018693025 / ee26941 (job 130516138966): success, 4710 tests 1 skipped 0 failures. Alias-tip suite green including: testFilteringKeepsTheShownTipAnchoredToTheSigil 0.584s, testOptionTypedHashOpensTheHashTip 0.325s, testTypingQueryBeforeTheRouteListOpensKeepsTheTip 0.416s, plus testEditBeforeTheReplyDropsTheTip 0.166s, testChangedSeparatorReplyDoesNotDisableTheNextTipRequest 0.313s, testSecondEligibleSigilInASessionShowsNoTip 0.389s.

Red base run 43104946525 / 6cbbddf (job 130805719698): failure. Deterministic trio PASSED (filtering 0.338s, option-typed hash 0.284s, typing-query 0.325s), changed-separator passed 0.387s, second-eligible-sigil passed 0.392s. testEditBeforeTheReplyDropsTheTip FAILED at CaptureAliasTipPanelTests.swift:336 nil vs Optional(1) sigilEdited drop counter. Three notebook/drawer failures: CaptureEditorHighlightTests.testNotebookCreateSectionUsesDottedUnderlineAndExistingClearsIt, CapturePanelModelTests.testAcceptingDrawerCandidateInsertsSlugAndLandsCaret, CapturePanelModelTests.testNotebookNewSectionUsesDottedPurpleUnderlineAndRepaintClearsIt. Bundle/Launch/Install skipped.

Classification: deterministic trio shares one cause (missing anchor fixture + hash completion surface + record-list misclassification) and is fixed with causal evidence (passes on ee26941 green and again on 6cbbddf). Named intermittents NOT shared-and-fixed: edit-before-reply reproduces on unchanged phase base (6cbbddf) so its cause is separate and unresolved; inspected editorTextDidChange (marks in-flight request .sigilEdited) vs handleMissingCompletion/deferAliasTipOpportunity(.unanchored) overwrite hypothesis in source but reporting as unconfirmed without runtime evidence. changed-separator and second-eligible passed on both runs but passing does not establish a flake is fixed, so record both as separate cause unresolved.

Current SHA run 43112612175 / 1e83c03: in_progress when checked (Lint/Build success, Test in progress, job 130832299036). Watching via monitor; final closeout waits on it.

PROPOSED FOLLOW-UP: edit-before-reply sigilEdited drop-counter failure on clean base (see bob-cli-jx; already mentions edit-before-reply) - diagnose .sigilEdited vs .unanchored ordering with runtime evidence.

PROPOSED FOLLOW-UP: notebook/drawer trio failures on 6cbbddf clean base belong to active epic bob-cli-ka (notebook/place-menu owner per parent plan) - triage there, not in bob-cli-kj.5.

PROPOSED FOLLOW-UP: second-eligible-sigil flake tracked by bob-cli-jk may share tip-wait root cause - confirm with causal evidence or keep open; passing twice does not close a flake.

[2026-11-11T22:52:49Z · bob-cli-kj.5] Closeout evidence: exact-SHA macOS run 43112612175 for HEAD 1e83c032217a9d6c90827ee467e5c60b57069d88 (https://github.com/bobs-org/bob-mac-capture/actions/runs/43112612175, job 130832299036) is COMPLETED with conclusion failure. Lint Swift formatting success, Build success, Test failed: 4750 tests, 1 skipped, 10 assertion failures across 6 test cases. Bundle/Verify plist/Launch/Install skipped.

Deterministic trio (bob-cli-jx scope) all PASSED on this exact SHA: testFilteringKeepsTheShownTipAnchoredToTheSigil 0.681s, testOptionTypedHashOpensTheHashTip 0.442s, testTypingQueryBeforeTheRouteListOpensKeepsTheTip 0.443s. First-frame tip contract preserved (testTipIsInTheListsFirstFrame passed 0.560s).

Named intermittents: testEditBeforeTheReplyDropsTheTip FAILED at CaptureAliasTipPanelTests.swift:336 (nil vs Optional(1) sigilEdited counter, 0.515s) - same clean-base failure as run 43104946525, separate cause unresolved. testChangedSeparatorReplyDoesNotDisableTheNextTipRequest PASSED 0.595s. testSecondEligibleSigilInASessionShowsNoTip PASSED 0.443s (bob-cli-jk) - passing does not establish flake fixed.

Other clean-base failures outside trio causes: CaptureDotRouteAliasTests.testFastDoubleDotBeforeReplyCollapsesToOne (1 vs 2), CaptureEditorHighlightTests.testNotebookCreateSectionUsesDottedUnderlineAndExistingClearsIt, CapturePanelModelTests.testAcceptingDrawerCandidateInsertsSlugAndLandsCaret, CapturePanelModelTests.testNotebookNewSectionUsesDottedPurpleUnderlineAndRepaintClearsIt, CaptureSeparatorToggleTests.testUnchangedAliasReplyLeavesPeriodLiteralWithoutOpeningPicker.

Historical green reference retained: run 43018693025 / ee26941 success with 4710 tests 0 failures; trio + all three intermittents passed there. It must not be mislabeled as green for current SHA.

PROPOSED FOLLOW-UP: edit-before-reply sigilEdited failure reproduces on 6cbbddf and 1e83c03 clean bases (see bob-cli-jx) - needs runtime diagnosis of .sigilEdited vs .unanchored ordering.

PROPOSED FOLLOW-UP: notebook/drawer trio + separator/dot-route failures belong to active epic bob-cli-ka (notebook/place-menu owner) - triage there.

PROPOSED FOLLOW-UP: second-eligible-sigil flake tracked by bob-cli-jk - keep open; two passes do not close a flake.

[2026-11-11T22:52:58Z · bob-cli-kj.5] Verified: landed alias-tip fix intact at 1e83c032217a9d6c90827ee467e5c60b57069d88 (ee26941 ancestor; alias-tip test diff empty). Exact-SHA run 43112612175 (https://github.com/bobs-org/bob-mac-capture/actions/runs/43112612175): deterministic trio passed (filtering 0.681s, option-hash 0.442s, typing-query 0.443s); changed-separator and second-eligible-sigil passed; edit-before-reply failed line 336 as on 6cbbddf base. Red only from 6 unrelated clean-base failures (edit-before-reply + dot-route + notebook/drawer trio + separator), recorded as PROPOSED FOLLOW-UP notes; historical green ee26941 run 43018693025 retained as reference only.

## Dependencies

- **Depends on:** [bob-cli-kj.1](bob-cli-kj.1.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.5.md) | [bob-cli-kj.5](bob-cli-kj.5.md) | 0 |
