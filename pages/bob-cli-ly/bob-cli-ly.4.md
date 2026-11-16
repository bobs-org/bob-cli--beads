# Bead: bob-cli-ly.4 — Panel wiring, keys, accept and open, truthful fixtures, Mac docs

[Bead Pages](../README.md) / [bob-cli-ly](README.md) / bob-cli-ly.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cr](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cr.md) · **Assignee:** `bob-cli-ly.4` · **Size:** medium
**Created:** 2026-11-15 16:47:01 EST · **Closed:** 2026-11-16 07:20:48 EST
**Plan:** [202611/note\_goto\_double\_slash.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_goto_double_slash.md)

## Description

mac-note-panel: wire `note_goto` into the panel model and key router (continuation, peel, consume rules), open notes read-only, add generated fixtures and panel tests, document the picker, and land green on macOS CI.

## Notes

[2026-11-16T03:09:35Z · bob-cli-ly.4] PROPOSED FOLLOW-UP: Trim docs/reference/plugins/bob-ledger-tools.md below the 6,000-word reference cap; just docs-check fails only on its unchanged 6,281-word clean-base content.

[2026-11-16T03:14:59Z · bob-cli-ly.4] Handoff caution: the staged watcher resolves HEAD when it starts; because this turn carries the dirty linked checkout, a green result for the old HEAD does not verify these changes. Commit the carried tree, watch CI for that new exact SHA, and close only after it is green.

[2026-11-16T03:27:48Z · bob-cli-ly.4--1] PROPOSED FOLLOW-UP: Investigate CaptureDotRouteAliasTests.testFastDoubleDotBeforeReplyCollapsesToOne: CI run 43780481574 failed at the asks-count assertion on clean base SHA 19e4c4048a0e7bfbdc69eeb356ddb497481dca99, before the uncommitted Notes panel changes were included.

[2026-11-16T04:05:49Z · bob-cli-ly.4--3] CI follow-up: preflight run 43800683604 (https://github.com/bobs-org/bob-mac-capture/actions/runs/43800683604) tested snapshot SHA 656390050fc473b7337504958af5401fcc9360d0 from base 5bc9478f3322bbdcb4da52e72bcfba8e85b0e62f. Build passed; Test failed with only `error: fatalError`, no test name, no hang sample artifact, and no actionable stack in `gh run view --log-failed`. This differs from known clean-base run 43780481574, which completed 4,773 tests and failed only CaptureDotRouteAliasTests.testFastDoubleDotBeforeReplyCollapsesToOne. Recheck on the committed exact HEAD before close.

[2026-11-16T04:25:53Z · bob-cli-ly.4--4] macOS CI compile regression found in run 43802559714 (snapshot SHA d1ac712b1e82411c490f05e6a288ad95bca7ae49, base 5bc9478f3322bbdcb4da52e72bcfba8e85b0e62f): CaptureNoteGotoPanelTests.swift memberwise CaptureKeyRoutingContext arguments were out of declaration order, plus markerExists needed explicit self in an async closure. Fixed those test call sites. The earlier portable-check passed 2,512 tests with 1 skipped but does not type-check this Mac test target; post-commit portable, preflight, and exact-HEAD watcher are being staged. Phase remains open.

[2026-11-16T04:56:17Z · bob-cli-ly.4--5] Exact-SHA preflight run 43804755348 (https://github.com/bobs-org/bob-mac-capture/actions/runs/43804755348; snapshot ba382442592e51d4821232ab0f7d6f308325ec00, base d12cd6c7d94d61d300e102257e065eb17d8ad646) compiled but failed two new CaptureNoteGotoPanelTests cases: testFastDraftOpensFilteredCatalogIncludingViews lacked a fake-bob //monthly completion, and the no-selection router context inherited pickerHasSelection=true. Added the monthly catalog fixture response/range handling and made the selection state explicit. Portable check passed 2,512 tests with 1 skipped. Exact-HEAD watcher did not run because the preflight failed. Re-run portable-check, macOS preflight, and watcher after this fix is committed; keep bob-cli-ly.4 open pending green exact-SHA verification. Unchanged docs-check baseline remains 6,281 words, 281 over the 6,000-word cap.

[2026-11-16T06:10:52Z · bob-cli-ly.4--7] Exact-SHA verification failure: macOS run 43811774646 (https://github.com/bobs-org/bob-mac-capture/actions/runs/43811774646) tested snapshot SHA e4b9ab54103febe77189d28125bb850c3783a7e6 from base HEAD 39ba0d0ea0304a2780f31c5da5c0e0bd094b5f3d. Portable check passed 2,512 tests with 1 skipped; macOS format and build passed, but Test failed at CaptureSeparatorToggleTests.testBackslashGluedToSectionNameStaysLiteral and testOlderBobMoveAliasReplyLeavesLiteralWithoutOpeningPicker. Both passed on clean-base run 43780481574; the known CaptureDotRouteAliasTests.testFastDoubleDotBeforeReplyCollapsesToOne remains the separate clean-base follow-up. The exact-SHA watcher did not run because the chain stopped at macOS CI failure. Pending //monthly parse fixture changes are carried into staged rerun monitor 4dj0w6; keep this phase and parent epic open pending rerun.

[2026-11-16T06:43:47Z · bob-cli-ly.4--8] Verification follow-up: portable-check passed 2,512 tests with 1 skipped; macOS preflight run 43815369694 (https://github.com/bobs-org/bob-mac-capture/actions/runs/43815369694) passed at snapshot SHA e80199e747255b6ab0aadd9ca93a889cb68015f4, which includes the pending //monthly fixture correction. The watcher selected run 43807263097 for committed HEAD 39ba0d0ea0304a2780f31c5da5c0e0bd094b5f3d; that run failed the missing monthly fixture test and CaptureAliasTipPanelTests.testChangedSeparatorReplyDoesNotDisableTheNextTipRequest. The two separator-toggle failures from run 43811774646 did not recur. This is not yet green exact-HEAD verification: commit the pending fixture correction, then rerun portable-check, macOS preflight, and the exact-SHA watcher; keep this phase open. The unchanged docs-check baseline remains 6,281 words, 281 over the 6,000-word cap.

[2026-11-16T07:06:04Z · bob-cli-ly.4--8] Additional rerun result: preflight run 43818820494 (https://github.com/bobs-org/bob-mac-capture/actions/runs/43818820494) passed all required macOS steps at snapshot SHA 63a47335b58ed85c7fbf8e98e804b7dec75c3889; the following watcher again selected failed run 43807263097 for HEAD 39ba0d0ea0304a2780f31c5da5c0e0bd094b5f3d. The fixture correction is still only a local working-tree change. Staged monitor sp1nxf29fw12 runs only just portable-check because the shell chain was split at &&; its follow-up must run Scripts/macos-ci-check and .sase/watch-note-goto-ci.sh against the committed fixture-correction SHA before closing this phase. Keep bob-cli-ly.4 open until that exact-HEAD run and watcher pass. Parent epic remains open. Docs-check baseline is unchanged at 6,281 words, 281 over the 6,000-word cap.

[2026-11-16T07:46:46Z · bob-cli-ly.4--a] Exact-SHA CI run 43821665141 (https://github.com/bobs-org/bob-mac-capture/actions/runs/43821665141) matched HEAD f24475e53185c8ca94534d6633ed35dc28ad1353 but failed only CaptureSeparatorToggleTests.testOlderBobMoveAliasReplyLeavesLiteralWithoutOpeningPicker at CaptureSeparatorToggleTests.swift:1272. This test also failed in an earlier phase run and later passed; the current commit changes only the //monthly fake-bob parse fixture. macos-ci-check passed the identical tree at snapshot SHA 70de9a5f845bb557cb0a0a3dc7e1379a9bcd38eb (run 43822641566). No phase regression is reproduced; rerunning the failed exact-SHA job and keeping this phase open.

[2026-11-16T08:09:12Z · bob-cli-ly.4--b] Exact-SHA rerun attempt 2: https://github.com/bobs-org/bob-mac-capture/actions/runs/43821665141 tested headSha f24475e53185c8ca94534d6633ed35dc28ad1353 and failed in Test after lint and Build passed. Full run summary: 4,784 tests, 1 skipped, 1 failed. Attempt 2 failed CaptureSeparatorToggleTests.testUnchangedAliasReplyLeavesPeriodLiteralWithoutOpeningPicker at line 1170 because the capture-rewrite record assertion was absent after its fixed 200 ms wait; the attempt 1 failure, testOlderBobMoveAliasReplyLeavesLiteralWithoutOpeningPicker, passed on attempt 2. The commit changes only the fake-bob //monthly fixture and its JSON response, so no Notes picker phase regression is reproduced. Prior portable-check remains 2,512 passed, 1 skipped; docs-check baseline remains 6,281 words, 281 over cap. Keep bob-cli-ly.4 open and parent bob-cli-ly open. The clean-base CaptureDotRouteAliasTests.testFastDoubleDotBeforeReplyCollapsesToOne follow-up remains separate.

[2026-11-16T10:37:18Z · bob-cli-ly.4] Recovery scope is small enough for one coder: all Notes panel code, fixtures, and docs are already landed in bob-mac-capture through f24475e53185c8ca94534d6633ed35dc28ad1353. The latest exact-SHA run 43821665141 attempt 2 fails only an unchanged-alias subprocess record assertion after a fixed 200 ms sleep. Replaced fixed sleeps in four unchanged-reply separator tests with an immediate rewrite-start assertion and a bounded wait for rewrite completion; fake replies deliberately wait 300 ms to exercise this timing. No production code or memory changes. Verified the approved bases=yes branch on the live Mac: an existing visible .base opened through obsidian://bob-open-notes with count=1/path1 and no line1, the resulting view type was bases, its contents were identical before/after, and the previous active leaf was restored. epic-symbols reports no entries. Next verification must compile this edited tree in a scratch Mac copy, run portable-check and Scripts/macos-ci-check, then commit through sase_final and watch the new committed exact SHA before closing only this phase. Do not reuse the old f24475e5 failed run as evidence for the fixed tree.

[2026-11-16T11:13:53Z · bob-cli-ly.4--1] Verification recovery: monitor ggvpm81v09dc passed portable-check (2,512 tests, 1 skipped) and scratch Mac bundle plus all four typecheck targets. Preflight run https://github.com/bobs-org/bob-mac-capture/actions/runs/43852193445 (snapshot f5f21a13c6662bc05c18d54a51f8e954e71ef7b6) passed lint/build, all 10 CaptureNoteGotoPanelTests and all 82 CaptureSeparatorToggleTests, then failed only CaptureAliasTipPanelTests.testListThenPickerSequenceShowsAtMostOneTip (3 cascading assertions). Its first route tip must beat a 200 ms completion debounce; a late reply is correctly dropped, so the assumed first shown tip is missing. Changed this session-limit test to await and apply the real fake-bob route-tip reply before requesting completion, with a deliberate 300 ms reply and an 8-second bound; added explicit first-tip count and session-drop assertions. Only two test files are dirty (the four separator cases carried from the prior turn plus this alias-tip case); production, docs, fixtures, and memory are unchanged. Recompile and preflight this new tree before committing, then watch the new committed exact HEAD; do not watch old f24475e5 while these edits are dirty.

[2026-11-16T11:53:37Z · bob-cli-ly.4--2] Green preflight: monitor m59y80ee7mcg completed successfully (portable-check, scratch Mac bundle and all four test-target typechecks, then Scripts/macos-ci-check). Required macOS lint, build, tests, bundle, si

… and 1853 more characters

## Dependencies

- **Depends on:** [bob-cli-ly.2](bob-cli-ly.2.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-ly.3](bob-cli-ly.3.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ly.5](bob-cli-ly.5.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ly.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ly.4.md) | [bob-cli-ly.4](bob-cli-ly.4.md) | 5 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@5bc9478`](https://github.com/bobs-org/bob-mac-capture/commit/5bc9478f3322bbdcb4da52e72bcfba8e85b0e62f) | feat(capture): open notes from the // Go To Notes picker | [bob-cli-ly.4](bob-cli-ly.4.md) | 2026-11-15 22:33:52 EST |
| bob-mac-capture | [`bob-mac-capture@d12cd6c`](https://github.com/bobs-org/bob-mac-capture/commit/d12cd6c7d94d61d300e102257e065eb17d8ad646) | fix(capture): compile Notes picker macOS tests | [bob-cli-ly.4](bob-cli-ly.4.md) | 2026-11-15 23:29:36 EST |
| bob-mac-capture | [`bob-mac-capture@39ba0d0`](https://github.com/bobs-org/bob-mac-capture/commit/39ba0d0ea0304a2780f31c5da5c0e0bd094b5f3d) | fix(capture): correct Notes picker CI fixtures | [bob-cli-ly.4](bob-cli-ly.4.md) | 2026-11-15 23:58:25 EST |
| bob-mac-capture | [`bob-mac-capture@f24475e`](https://github.com/bobs-org/bob-mac-capture/commit/f24475e53185c8ca94534d6633ed35dc28ad1353) | fix(capture): add monthly Notes picker parse fixture | [bob-cli-ly.4](bob-cli-ly.4.md) | 2026-11-16 02:08:15 EST |
| bob-mac-capture | [`bob-mac-capture@1e0a344`](https://github.com/bobs-org/bob-mac-capture/commit/1e0a344e948b81e675dfcd6090aa4cd901721c01) | test(capture): synchronize separator replies and alias tip setup | [bob-cli-ly.4](bob-cli-ly.4.md) | 2026-11-16 06:55:13 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ly.4--1][1] | Need the assigned phase scope, design path, and epic decisions while recovering the failed exact-SHA Mac CI run | 1 |
| read-by | [agent:bob-cli-ly.4--2][1] | Review note 13 and phase completion criteria after green macOS preflight | 1 |
| read-by | [agent:bob-cli-ly.4--4][1] | Review the open Notes picker phase before recording the newly confirmed macOS test-target compile regression and staging verification | 2 |
| read-by | [agent:bob-cli-ly.4--5][1] | Review the phase bead before recording this second failed macOS CI run and its focused fixture corrections | 1 |
| read-by | [agent:bob-cli-ly.4--8][1] | Review the phase record before appending the failed watcher and exact-SHA evidence | 1 |
| read-by | [agent:bob-cli-ly.5][2] | Check panel phase notes for bases confirmation evidence | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ly.4.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ly.5/README.md

<!-- sase:referenced-by:end -->
