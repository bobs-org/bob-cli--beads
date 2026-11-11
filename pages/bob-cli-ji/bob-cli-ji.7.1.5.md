# Bead: bob-cli-ji.7.1.5 — Highlighted editor, live preview, and save controls

[Bead Pages](../README.md) / [bob-cli-ji.7.1](bob-cli-ji.7.1.md) / bob-cli-ji.7.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) · **Assignee:** `bob-cli-ji.7.1.5` · **Size:** medium
**Created:** 2026-11-10 10:29:45 EST · **Closed:** 2026-11-10 16:58:13 EST
**Plan:** [202611/mac\_event\_note\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_event_note_mode.md)

## Description

editor: add the fixed identity header, recurring scope control, multiline AppKit editor, UTF-8 highlight/error overlays, shared rail, Lands as block, status and footer keys. Wire save, clear, and last-mutation undo to the session model. Complete hosted end-to-end and render tests, including draft/undo restoration and unsupported Bob. Read Editor and acceptance.

## Notes

[2026-11-10T20:52:52Z · bob-cli-ji.7.1.5] PROPOSED FOLLOW-UP: Mac typecheck-tests fails on pre-existing @MainActor XCTestCase.tearDown accessing ledgerSuites in CaptureRelationEqualsAliasTests and CaptureModifierAliasTests — same errors on clean master; CI still runs the tests.

[2026-11-10T21:33:35Z · bob-cli-ji.7.1.5--1] PROPOSED FOLLOW-UP: CaptureAliasTipPanelTests still fail on exact-SHA macOS CI (run 42901006029: testChangedSeparatorReplyDoesNotDisableTheNextTipRequest, testEditBeforeTheReplyDropsTheTip, testFilteringKeepsTheShownTipAnchoredToTheSigil, testOptionTypedHashOpensTheHashTip, testTypingQueryBeforeTheRouteListOpensKeepsTheTip) identically to picker SHA 90b6f9e run 42888193431 and base aafed83/6b6052c (runs 42826766066, 42838952067); same class as flake bead bob-cli-jk — GcalNoteEditorTests races are the only editor-introduced Test failures

[2026-11-10T21:58:13Z · bob-cli-ji.7.1.5--2] SHA 6c177190e3e4626e9829a879e0e58240e202adcd (commit 62a7b70) https://github.com/bobs-org/bob-mac-capture/actions/runs/42906644279 required steps: Set up job ok, Check out repository ok, Check scripts ok, Show toolchain ok, Lint Swift formatting ok, Build ok, Test failure (CaptureAliasTipPanelTests only), Upload render fixtures ok, Upload test hang samples ok, Bundle skipped, Verify plist and signature skipped, Launch smoke test skipped, Upload launch smoke test diagnostics skipped, Install and reinstall skipped, Post Check out repository ok, Complete job ok; GcalNoteEditorTests green (all 11 cases plus GcalNoteEditorDesignTests); athena portable-check 2464 tests green; CaptureAliasTipPanelTests remaining failures reproduce on picker SHA 90b6f9e and base aafed83/6b6052c (bob-cli-jk), already noted as PROPOSED FOLLOW-UP; Mac scratch typecheck unavailable this turn

## Dependencies

- **Depends on:** [bob-cli-ji.7.1.3](bob-cli-ji.7.1.3.md) ✓ · ⧖ 2026-11-10
- **Depends on:** [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.7.1.6](bob-cli-ji.7.1.6.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.7.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.5.md) | [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.7.1.5--1][1] | Need the phase scope and design file after macos-ci-check Test failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.5.md

<!-- sase:referenced-by:end -->
