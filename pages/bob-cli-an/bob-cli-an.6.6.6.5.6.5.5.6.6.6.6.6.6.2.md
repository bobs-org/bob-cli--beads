# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2 — Turn bob-mac-capture master CI green on the RefsPanel Highlights-key tests

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2` · **Size:** large
**Created:** 2026-10-26 12:58:46 EDT · **Closed:** 2026-10-26 14:15:36 EDT
**Plan:** [202610/backlog\_batch14\_ledger\_integrity\_mac\_ci\_and\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md)

## Description

mac-refs-ci-red: resolve bob-cli-ci by deciding, per failing RefsPanel test, whether 1311536 regressed the product or outdated the expectation, and fixing the side that is wrong without weakening assertions.

## Notes

[2026-10-26T17:08:53Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2] Planning evidence before source edits: no prior-work notes or remaining-work handoff; choose tale/medium. Inspected 1311536, d8a828f and fetched c7a5f37 (cc.9); read CI logs 40225855522 and 40358201800. Per-test classification: (1) Design renderTabsLoaded expects old previous-tab morning_notes; current contract selects today_report. Hover fixture likewise must target a different open row while retaining XCTAssertNotEqual. (2) Tabs restore test query keep + papers filters out kept chat/small_reading before select, so its nil selection/90 offset failures are invalid fixture setup, not evidence to relax restore behavior. (3-4) Focus publish and reselection tests expose a product bug: inspectorLoader.$content emits in willSet, but tryFireHighlightsKeyFocus rereads inspectorLoader.content and sees old data; use the emitted map and test one-shot delivery. (5) TabSwitch test opens an ephemeral Highlights session then expects the next library show to stay in Tabs, contrary to 1311536 documented restore contract; split ordinary-Tabs consumption coverage from ephemeral restoration. (6) CurrentTab failure at 1311536 line 3125 is specifically currentID=nil while selected/preselected assertions passed; libraryDidPublish reconstructs RefsTabsListing without currentID, so preserve the field and force a refresh regression. c7a5f37 retains both product defects. cc coordination note records the Copy restore fixture issue and leaves Copy-specific changes to cc. epic-symbols currently reports no entries. No implementation or XCTest execution yet.

[2026-10-26T18:15:28Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2--4] VERIFICATION CLOSEOUT (2026-10-26)

Modified paths in bob-mac-capture:
- Sources/BobMacCapture/Refs/RefsPanelModel.swift
- Tests/BobMacCaptureTests/RefsPanelModelTests.swift
- Tests/BobMacCaptureTests/RefsPanelDesignTests.swift

Planned test classification and correction:
1. RefsPanelDesignTests.testRefsPanelStatesToPNG had outdated fixture assertions: the loaded state now selects focused today_report, and the hover image uses unselected morning_notes. Current identity, caption, row-count, and unselected checks remain.
2. testHighlightsTabsShowResetsAndLibraryRestoresTheFilter had an invalid query/scope that excluded small_reading before selection. The fixture now uses small + chats and retains exact view, selection, inspector offset 90, and list offset 200 restore checks.
3. testHighlightsKeyFocusPublishesAndReveals and testHighlightsKeyFocusReselectionRearmsAndCtrlDCancels exposed a product bug: the @Published willSet callback reread stale loader content. Focus now evaluates the emitted content snapshot; regression coverage checks event delivery, both content/snapshot arrival orders, rearming, and cancellation.
4. testTabSwitchUsesTheSwitcherPreselectionOnceOnTheNextShow expected ordinary tabs behavior from an ephemeral Highlights session. Coverage now exercises persistent Tabs with one-time preselection and a separate ephemeral-session restore case.
5. testHighlightsKeySelectsCurrentTab exposed a product bug: libraryDidPublish rebuilt RefsTabsListing without currentID. Refresh now preserves a still-listed current ID and clears one outside the refreshed listing; regression coverage exercises both.

Verification:
- just portable-check in bob-mac-capture passed, exit 0, both before and during the final scratch run.
- Initial mac scratch typecheck failed on two test closure argument errors in RefsPanelModelTests.swift (lines 3377 and 3513); those errors were corrected. Final isolated scratch run on SSH alias mac completed ./Scripts/bundle.sh --identity - and just typecheck-tests successfully, exit 0. BobMacCapture, install-helper, CaptureCore, and RefsCore targets reported PASS, and MAC_SCRATCH_CLEANED confirmed deletion. The Mac has Command Line Tools without XCTest, so typecheck-tests used the stub and did not execute XCTest behavior; real XCTest results remain for CI.
- just check in the primary bob-cli workspace failed with exit 101 before tests. The primary checkout was clean at HEAD 36ae0ef0ae4fe4fd49b6916eb04431a2738f4eab. Both baseline StoreWriteParams initializers lack verified: src/native/highlights_ref/create.rs:3566 and src/native/highlights_ref/overwrite/execute.rs:3329. The same state is in the clean base; this is unrelated to RefsPanel. Existing tracking is recorded on bob-cli-cc.10, and plan 202610/fix_store_write_params_verified.md records the later repair as commit e9a955f9225f304a421a2cf755b39c985f9b6800. No new bead is needed.
- sase bead epic-symbols bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2 returned no --epic-symbol entries.

The phase work and available checks are complete. Keep bob-cli-ci, bob-cli-cc, and all ancestors with their landers.

[2026-10-26T18:15:36Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2--4] Closed RefsPanel repair phase after passing portable-check, isolated macOS bundle and test-target typecheck with scratch cleanup, clean-base classification of just check, and an empty epic-symbol scan. macOS XCTest execution remains for CI because the CLT host has no XCTest.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@bdeb4aa`](https://github.com/bobs-org/bob-mac-capture/commit/bdeb4aa176c278a8cfba8c4a0f5463d7c2fcf3b0) | fix(refs): repair Highlights focus and tab state | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2.md) | 2026-10-26 14:16:56 EDT |
