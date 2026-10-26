# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2 — Turn bob-mac-capture master CI green on the RefsPanel Highlights-key tests

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2` · **Size:** large
**Created:** 2026-10-26 12:58:46 EDT
**Plan:** [202610/backlog\_batch14\_ledger\_integrity\_mac\_ci\_and\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md)

## Description

mac-refs-ci-red: resolve bob-cli-ci by deciding, per failing RefsPanel test, whether 1311536 regressed the product or outdated the expectation, and fixing the side that is wrong without weakening assertions.

## Notes

[2026-10-26T17:08:53Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2] Planning evidence before source edits: no prior-work notes or remaining-work handoff; choose tale/medium. Inspected 1311536, d8a828f and fetched c7a5f37 (cc.9); read CI logs 40225855522 and 40358201800. Per-test classification: (1) Design renderTabsLoaded expects old previous-tab morning_notes; current contract selects today_report. Hover fixture likewise must target a different open row while retaining XCTAssertNotEqual. (2) Tabs restore test query keep + papers filters out kept chat/small_reading before select, so its nil selection/90 offset failures are invalid fixture setup, not evidence to relax restore behavior. (3-4) Focus publish and reselection tests expose a product bug: inspectorLoader.$content emits in willSet, but tryFireHighlightsKeyFocus rereads inspectorLoader.content and sees old data; use the emitted map and test one-shot delivery. (5) TabSwitch test opens an ephemeral Highlights session then expects the next library show to stay in Tabs, contrary to 1311536 documented restore contract; split ordinary-Tabs consumption coverage from ephemeral restoration. (6) CurrentTab failure at 1311536 line 3125 is specifically currentID=nil while selected/preselected assertions passed; libraryDidPublish reconstructs RefsTabsListing without currentID, so preserve the field and force a refresh regression. c7a5f37 retains both product defects. cc coordination note records the Copy restore fixture issue and leaves Copy-specific changes to cc. epic-symbols currently reports no entries. No implementation or XCTest execution yet.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2.md) | 0 |
