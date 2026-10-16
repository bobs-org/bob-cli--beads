# Bead: bob-cli-8l.2 — Accessibility close ladder and graceful quit

[Bead Pages](../README.md) / [bob-cli-8l](README.md) / bob-cli-8l.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.85](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.85.md) · **Assignee:** `bob-cli-8l.2` · **Size:** medium
**Created:** 2026-10-16 14:11:30 EDT · **Closed:** 2026-10-16 14:48:11 EDT
**Plan:** [202610/highlights\_tab\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tab_close.md)

## Description

close-reader: `AXHighlightsTabsReader` implements `close` and `quitIfNoDocuments`. A close first tries the tab's own close button, then the window's close button when the tab is visible, and only then selects the tab, closes it, and restores the previously visible tab. Every close is verified by bounded re-reads, and an unsaved-changes sheet is detected and handed to Bryan. When no documents remain, Highlights quits through `NSRunningApplication.terminate()`. The phase also runs a read-only Mac probe and adds a CI test.

## Notes

[2026-10-16T18:47:56Z · bob-cli-8l.2] PROPOSED FOLLOW-UP: bob-cli-8c Accessibility claim must add close-button presses and no-documents terminate() — pending memory task bob-cli-8c still says Bob Mac Capture AX use is read and select only; this phase adds AXPress on a tab or window close button and NSRunningApplication.terminate() only when a fresh read shows no documents.

[2026-10-16T18:48:11Z · bob-cli-8l.2] Verified close-reader: AXHighlightsTabsReader.close and quitIfNoDocuments on the serial queue with a 2s budget. Ladder is tab AXButton child (probe: 8/8 tabs have one AXButton with nil subrole and no AXCloseButton attribute without hover), then window kAXCloseButtonAttribute (probe: present), then select-close-restore. Verify polls until that title count drops; AXSheet yields needsAttention after activate+raise. Unknown-bundle CI test: close matches read (.notRunning), never the protocol default; quitIfNoDocuments is true and launches nothing. athena just portable-check: 1290 tests passed. Mac scratch copy: Scripts/bundle.sh and just typecheck-tests passed; probe was read-only. No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-8l.1](bob-cli-8l.1.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8l.2/README.md) | [bob-cli-8l.2](bob-cli-8l.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@211c699`](https://github.com/bobs-org/bob-mac-capture/commit/211c6998de6aade5764bd5db1da364fa077cfd38) | feat(refs): add Highlights tab close ladder and graceful quit | [bob-cli-8l.2](bob-cli-8l.2.md) | 2026-10-16 14:49:45 EDT |
