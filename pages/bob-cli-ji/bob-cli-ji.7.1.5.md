# Bead: bob-cli-ji.7.1.5 — Highlighted editor, live preview, and save controls

[Bead Pages](../README.md) / [bob-cli-ji.7.1](bob-cli-ji.7.1.md) / bob-cli-ji.7.1.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) · **Assignee:** `bob-cli-ji.7.1.5` · **Size:** medium
**Created:** 2026-11-10 10:29:45 EST
**Plan:** [202611/mac\_event\_note\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_event_note_mode.md)

## Description

editor: add the fixed identity header, recurring scope control, multiline AppKit editor, UTF-8 highlight/error overlays, shared rail, Lands as block, status and footer keys. Wire save, clear, and last-mutation undo to the session model. Complete hosted end-to-end and render tests, including draft/undo restoration and unsupported Bob. Read Editor and acceptance.

## Notes

[2026-11-10T20:52:52Z · bob-cli-ji.7.1.5] PROPOSED FOLLOW-UP: Mac typecheck-tests fails on pre-existing @MainActor XCTestCase.tearDown accessing ledgerSuites in CaptureRelationEqualsAliasTests and CaptureModifierAliasTests — same errors on clean master; CI still runs the tests.

[2026-11-10T21:33:35Z · bob-cli-ji.7.1.5--1] PROPOSED FOLLOW-UP: CaptureAliasTipPanelTests still fail on exact-SHA macOS CI (run 42901006029: testChangedSeparatorReplyDoesNotDisableTheNextTipRequest, testEditBeforeTheReplyDropsTheTip, testFilteringKeepsTheShownTipAnchoredToTheSigil, testOptionTypedHashOpensTheHashTip, testTypingQueryBeforeTheRouteListOpensKeepsTheTip) identically to picker SHA 90b6f9e run 42888193431 and base aafed83/6b6052c (runs 42826766066, 42838952067); same class as flake bead bob-cli-jk — GcalNoteEditorTests races are the only editor-introduced Test failures

## Dependencies

- **Depends on:** [bob-cli-ji.7.1.3](bob-cli-ji.7.1.3.md) ✓ · ⧖ 2026-11-10
- **Depends on:** [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.7.1.6](bob-cli-ji.7.1.6.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.7.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.5.md) | [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@5bf8907`](https://github.com/bobs-org/bob-mac-capture/commit/5bf8907e6071f4f364a86b90f28a25cd8957ed09) | feat(capture): add Event Note editor, highlights, and save controls | [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) | 2026-11-10 16:01:17 EST |
| bob-mac-capture | [`bob-mac-capture@62a7b70`](https://github.com/bobs-org/bob-mac-capture/commit/62a7b70fb8d217e6afcdeb7cff0062019ac65524) | fix(capture): publish Event Note preview and show updates atomically | [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) | 2026-11-10 16:35:31 EST |
