# Bead: bob-cli-j9.2 — Portable tip model, policy, and ledger

[Bead Pages](../README.md) / [bob-cli-j9](README.md) / bob-cli-j9.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3y.linker.w0.md) · **Assignee:** `bob-cli-j9.2` · **Size:** medium
**Created:** 2026-11-09 12:18:38 EST · **Closed:** 2026-11-09 13:02:07 EST
**Plan:** [202611/capture\_alias\_typing\_tips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_alias_typing_tips.md)

## Description

mac-tip-core: decode the new capture-rewrite fields in CaptureCore and add the lesson map, presentation strings, the pure fade-by-fluency policy, session rules, and the UserDefaults JSON ledger with weekly counts, all unit-tested.

## Notes

[2026-11-09T18:01:37Z · bob-cli-j9.2--1] PROPOSED FOLLOW-UP: macOS record-preview timeouts are pre-existing and out of scope — testDelayedStaleSuccessReplyNeverClobbersCurrentRefusal and testExplicitPreviewOfCompleteDraftIsReadyWithSummary fail identically on clean base 90fa59d (run 42657112529) and on tip-master bd06c21 (run 42666602607) as on snapshot 3633c5ca (run 42666675195); owned by record-preview work (bob-cli-ir.11 commit 2f1d6dd settle attempt still in_progress as run 42668030425)

[2026-11-09T18:01:47Z · bob-cli-j9.2--1] PROPOSED FOLLOW-UP: macOS separator flake testUnchangedAliasReplyLeavesPeriodLiteralWithoutOpeningPicker uses fixed 200ms sleep before reading FAKE_BOB_RECORD_PATH (Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:1112-1120); passed on base 90fa59d and tip-master bd06c21 but failed once on snapshot run 42666675195 — same file already documents fixed-sleep race (rewriteWasForwarded); convert this test to poll the record instead of sleeping

[2026-11-09T18:02:07Z · bob-cli-j9.2--1] mac-tip-core verified: CaptureModels decodes sigil_alias_tip/where/reportsSigilAliasTips/alias, CaptureAliasTip lessons/presentation/policy/session/ledger plus 36 CaptureCoreTests all pass on macOS (runs 42666602607/42666675195) and portable-check green on athena (2381 tests, 0 failures, 1 pre-existing skip); exact-SHA macOS gate red only on pre-existing record-preview timeouts (reproduce on clean base 90fa59d) and one flaky 200ms-sleep separator assertion, both recorded as PROPOSED FOLLOW-UP

## Dependencies

- **Blocks:** [bob-cli-j9.3](bob-cli-j9.3.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j9.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j9.2.md) | [bob-cli-j9.2](bob-cli-j9.2.md) | 0 |
