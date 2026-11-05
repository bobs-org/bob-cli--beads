# Bead: bob-cli-h4.6 — Mac calm pending card and transfer refusal card

[Bead Pages](../README.md) / [bob-cli-h4](README.md) / bob-cli-h4.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.188](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.188.md) · **Assignee:** `bob-cli-h4.6` · **Size:** medium
**Created:** 2026-11-04 14:57:19 EST · **Closed:** 2026-11-05 09:39:03 EST
**Plan:** [202611/transfer\_previews.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/transfer_previews.md)

## Description

mac-pending-and-refusals: never flash red while a transfer destination is unfinished. Run the dry run and render bob's `transfer_pending` as a calm card with the resolved sources (typos caught early) and the four destination forms. Render transfer refusals as a designed card with Bob's message. Add fixtures, design renders, docs, and the manual checks list for Bryan.

## Notes

[2026-11-05T12:59:12Z · bob-cli-h4.6] PROPOSED FOLLOW-UP: Bring docs/reference/mac-capture/keyboard.md under the 6,000-word mounted reference cap — just docs-check reproduces identically at 6,016 words on this phase tree and clean base; bob-cli-h4.5 already recorded the same keyboard-page issue in note #1, while bob-cli-h9 covers protocol.md.

[2026-11-05T14:38:43Z · bob-cli-h4.6--2] PROPOSED FOLLOW-UP: Track the 12 macOS test failures repeated on clean-base SHA dd4a8bf909da9d10ba53253f579363722a9460cc (run 42027902336) and this phase snapshot (run 42043168828): CaptureBackslashGotoTests.testInsertHelperDeclinesWhileComposingSubmittingOrLocked; CaptureEditorWordMotionTests.testMotionsLeaveTextAndUndoUntouched; CapturePanelModelTests.testCommaCommitsPartialRouteThenBobOpensParentTaskPicker and testCommaOnExactRouteUsesBobRewriteLane; CaptureSeparatorToggleTests.testBackslashAliasAfterTaskTypeOpensTypeMenuAndDoubleTapCloses, testCommaAfterCompleteTargetRunOpensNextParentPicker, testDelayedAcceptedAliasSupersedesGatedCompletion, testNativeUndoRestoresLiteralSigilAliasWithoutRetriggering, testPeriodAliasAfterRouteOpensNewIDBlockPicker, testPeriodAliasOnMoveBulletOpensMovePicker, testSemicolonAliasOnOfferMoveBulletOpensMoveAndLinkPicker, and testUndoAfterMoveAliasRestoresLiteralWithoutRetriggering. Existing tracking: bob-cli-h7, bob-cli-h8.5 note #2, bob-cli-h4.4 note #2.

[2026-11-05T14:39:03Z · bob-cli-h4.6--2] Completed pending-transfer and refusal cards with fixtures, renderer coverage, and docs. Verified just portable-check: 2,168 tests passed, 1 skipped. Exact-SHA macOS Build passed; the 12 Test failures recur on clean-base SHA dd4a8bf909da9d10ba53253f579363722a9460cc and are recorded as a proposed follow-up with existing tracking references. Mac is offline for local target compilation. docs-check still has its documented clean-base 6,016/6,000 word-cap failure. epic-symbols reports none.

## Dependencies

- **Depends on:** [bob-cli-h4.3](bob-cli-h4.3.md) ✓ · ⧖ 2026-11-04
- **Depends on:** [bob-cli-h4.5](bob-cli-h4.5.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h4.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h4.6.md) | [bob-cli-h4.6](bob-cli-h4.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@6e09f2c`](https://github.com/bobs-org/bob-mac-capture/commit/6e09f2c7fabfdda0e337da63a6bb48b28c32747f) | feat(capture): render pending transfer and refusal cards | [bob-cli-h4.6](bob-cli-h4.6.md) | 2026-11-05 12:54:44 EST |
