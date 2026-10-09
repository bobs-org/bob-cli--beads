# Bead: bob-cli-5s.2 — Hotkey registry and CI render artifacts in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5z.md) · **Assignee:** `bob-cli-5s.2` · **Size:** small
**Created:** 2026-10-08 19:32:40 EDT · **Closed:** 2026-10-08 20:32:18 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

mac-groundwork: replace the single-key HotKeyManager with a HotKeyRegistry that routes by EventHotKeyID, keep Capture's hotkey working through it, add a shared PNG render helper for design tests, and make CI render and upload design fixtures as an artifact.

## Notes

[2026-10-08T23:53:27Z · bob-cli-5s.2] PROPOSED FOLLOW-UP: Add a decision record extending the thin-client rule to Bob Refs (opening never mutates the vault) — skipped per epic auto-decision refs_decision_memory=no; land agent to triage into a task bead.

[2026-10-09T00:30:09Z · bob-cli-5s.2--1] CI watch: run 37862317922 (eea838b) red 3x on pre-existing flaky subprocess-timeout tests, all in untouched CapturePanelModelTests.swift. Attempt1: testClosePendingListPreviewsTrimmedDraftWithCloseDisabled (timeout line 2533). Attempt2 (rerun failed jobs): testLaterBatchTaskIDPromptSuccessSplicesGlobalRangeAndKeepsCaptureContract (timeout line 5309). Attempt3: first test again, same timeout. My diff (838e043..eea838b) touches only ci.yml, README, AppDelegate hotkey wiring, HotKeyManager->HotKeyRegistry, BobMacCaptureTests.swift conflict-test adapt, new HotKeyRegistryTests + RenderFixtureWriter; zero lines in the failing tests path. Run URL: https://github.com/bobs-org/bob-mac-capture/actions/runs/37862317922

[2026-10-09T00:30:46Z · bob-cli-5s.2--1] Render-fixtures artifact verified: downloaded render-fixtures from run 37862317922, contains 149 non-empty PNGs (70 capture-picker-*, 20 pomodoro-block-*, 23 status-item-*, 20 task-block-*, 16 task-complete-*), light+dark pairs at 620/760 widths. HotKeyRegistryTests (8 tests: distinct IDs, routing, rejection, replacement, failure isolation, invalidate, unregister, presets) passed in all 3 CI attempts; AppDelegate registers production .capture through HotKeyRegistry.

[2026-10-09T00:31:33Z · bob-cli-5s.2--1] PROPOSED FOLLOW-UP: Quarantine or raise timeouts on fakeBob subprocess live-preview tests (CapturePanelModelTests/CaptureTaskCompletePanelTests waitUntil timeouts) that intermittently fail on loaded macOS CI runners — same Condition-not-met-before-timeout signature predates this phase (e.g. run 37386102989 on 2026-10-05 failed testBangAutoOpensCompletePickerFromFakeBob, testIDPromptSplicesBobCompleteReplacement, testShiftReturnReopensPickerAfterChaining the same way); land agent to triage into a flake task bead.

[2026-10-09T00:32:18Z · bob-cli-5s.2--1] mac-groundwork done: HotKeyRegistry routes .capture/.refs/.refsHighlightsOpen by EventHotKeyID with AppDelegate registering production .capture through it, covered by 8 green HotKeyRegistryTests; CI renders+uploads render-fixtures artifact verified at 149 non-empty design PNGs (capture-picker/pomodoro-block/status-item/task-block/task-complete, light+dark). CI run 37862317922 red only on pre-existing flaky fakeBob waitUntil timeouts in untouched CapturePanelModelTests (3 attempts failed 3 different-or-rotating tests, all Condition-not-met-before-timeout; identical signature on 2026-10-05 pre-phase run 37386102989); recorded as PROPOSED FOLLOW-UP for land-agent triage. No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-5s.6](bob-cli-5s.6.md) ◐ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.7](bob-cli-5s.7.md) ◐ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.2.md) | [bob-cli-5s.2](bob-cli-5s.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.2.md

<!-- sase:referenced-by:end -->
