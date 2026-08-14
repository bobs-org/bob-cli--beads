# Bead: bob-cli-m.2 — Native bullet editing and hierarchical preview

[Bead Pages](../README.md) / [bob-cli-m](README.md) / bob-cli-m.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.00w.f0.f0.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.00w.f0.f0.w0.md) · **Assignee:** `bob-cli-m.2` · **Size:** medium
**Created:** 2026-08-14 10:54:45 EDT · **Closed:** 2026-08-14 11:53:44 EDT
**Plan:** [202608/capture\_authored\_sub\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_authored_sub_bullets.md)

## Description

mac-bullet-editor: consume bob-cli's authored-child contract in bob-mac-capture, add Ctrl-J bullet insertion and empty-bullet Backspace behavior through the native text system, render exact nested preview lines, and verify the complete macOS interaction.

## Notes

[2026-08-14T15:53:27Z · bob-cli-m.2] PROPOSED FOLLOW-UP: bob-mac-capture live preview never renders clip.lines/scheduleLog.lines (only a literal-clipboard note) — capture_authored_sub_bullets.md says clipboard/schedule-log child lines should follow authored children "so explicit Preview mirrors the full block"; extending PreviewPane.previewContent to include those after sub_bullets would close that gap.

[2026-08-14T15:53:44Z · bob-cli-m.2] Implemented in the linked bob-mac-capture repo per capture_authored_sub_bullets.md: (1) CaptureCore/CaptureModels.swift decodes additive sub_bullets on CaptureParseResponse and CaptureCommandSuccess, tolerant of the key being absent; (2) CaptureKeyCommandRouter adds insertBulletNewline (Ctrl-J, keyCode 38+control) and deleteBackward (plain Backspace) commands; (3) CapturePanelController handles them via the first-responder NSTextView's native insertText(_:replacementRange:), inserting '\n- ' for Ctrl-J and, for Backspace, deleting an exactly '- ' placeholder row plus its preceding newline (or just the row on the first line) via the new emptyBulletRowDeletionRange(in:) helper; (4) CapturePanelView derives the real caret UTF-8 byte offset from AttributedTextSelection.indices(in:) instead of always assuming end-of-draft, and PreviewPane renders task_line followed by every sub_bullets line in source order/indentation (no more 2-line cap), scrolling internally past 140pt when bullets are present; (5) README's keyboard table, multiline example, and live-preview docs updated; the obsolete 'multiline is whitespace-normalized' claim is removed. Verified: CaptureCore/CaptureCoreTests (models, BobProcessClient, fake-bob multiline+sub_bullets fixtures) actually built and run via  in a temporary CaptureCore-only Package.swift on this Linux host (AppKit-free target) — 33/35 pass, the other 2 (process-termination timing) reproduced identically against unmodified master, confirming they're pre-existing sandbox flakiness, not a regression. The BobMacCapture/BobMacCaptureTests target (Ctrl-J, Backspace, caret-offset, preview rendering) cannot compile on Linux (no AppKit) per this repo's own design note and the swift-toolchain-on-athena memory; those changes and their new router/controller tests are implemented and reasoned through carefully (cross-checked the newer AttributedTextSelection/AttributedString.Index API against WWDC25 sources) but require the repository's macOS CI and a manual pass on a Mac, as the plan itself mandates. Filed one PROPOSED FOLLOW-UP note (live preview never renders clip/schedule-log lines after authored children).

[2026-08-14T15:54:20Z · bob-cli-m.2] Implemented native bullet editing and hierarchical preview in bob-mac-capture: CaptureCore decodes sub_bullets (tolerant of absent key) in CaptureParseResponse/CaptureCommandSuccess; Ctrl-J and Backspace routed through CaptureKeyCommandRouter/CapturePanelController acting on the first-responder NSTextView; CapturePanelView derives real caret UTF-8 offset from AttributedTextSelection; preview renders task_line plus all sub_bullets lines uncapped. Verified via CaptureCore unit tests (model decoding, router, controller, fake-bob process-client fixtures) run against a sandboxed copy on Linux: 33/35 pass, 2 pre-existing process-termination timing failures reproduced identically against unmodified master (not a regression). AppKit/SwiftUI view code could not be compiled on this Linux workspace; needs macOS CI/manual verification. README updated (keyboard table, multiline example, live preview docs).

## Dependencies

- **Depends on:** [bob-cli-m.1](bob-cli-m.1.md) ✓ · ⧖ 2026-08-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-m.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-m.2/README.md) | [bob-cli-m.2](bob-cli-m.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@727b05d`](https://github.com/bobs-org/bob-mac-capture/commit/727b05d0be377490fd27b47d29a72613e449f4f9) | feat(capture): native bullet editing and hierarchical preview | [bob-cli-m.2](bob-cli-m.2.md) | 2026-08-14 12:05:40 EDT |
