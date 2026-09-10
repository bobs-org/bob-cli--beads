# Bead: bob-cli-1z.5 — CaptureCore models, presentation model, and panel wiring

[Bead Pages](../README.md) / [bob-cli-1z](README.md) / bob-cli-1z.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ir](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ir.md) · **Assignee:** `bob-cli-1z.5` · **Size:** medium
**Created:** 2026-09-10 13:19:09 EDT · **Closed:** 2026-09-10 15:30:54 EDT
**Plan:** [202609/capture\_task\_toggle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_task_toggle.md)

## Description

mac-core: decode the additive toggle fields in CaptureCore, add a Linux-testable toggle presentation model, and route completion, the footer verb, status text, announcements, and notifications through it.

## Notes

[2026-09-10T19:30:32Z · bob-cli-1z.5] PROPOSED FOLLOW-UP: CaptureTogglePresentation wording for statusText/voiceOverAnnouncement/notificationTitle/notificationBody is my own judgment call (not spec'd byte-exactly like chips/addedLinkText/removedLinksText, which do mirror print_human_task_toggle_success). Worth a UX pass once mac-preview (bob-cli-1z.6) renders the live preview end-to-end, to confirm the spoken/notification copy reads well in practice.

[2026-09-10T19:30:54Z · bob-cli-1z.5] mac-core phase complete in the linked bob-mac-capture repo (working tree left uncommitted for /sase_final):

- CaptureModels.swift: decode all additive task_toggle fields on CaptureCommandSuccess
  (toggleDirection, previousTaskLine, statusSymbol/Name, previousStatusSymbol/Name,
  pomodoroName, createsPomodoro, pomodoroAlreadyLinked, removedPomodoroLinks,
  removedScheduled, pomodoroSelectorUnused) via decodeIfPresent; previewBlockLines
  already worked correctly for a toggle result without changes (sub_bullets/clip stay
  omitted, scheduleLog still appends).
- New Sources/CaptureCore/CaptureTogglePresentation.swift: pure, failable presentation
  type (nil for non-toggle results) exposing before/after task lines+markers,
  route/day-file destination labels, dayFileChanged, added/removed link text, dim chips
  (byte-matching print_human_task_toggle_success's wording/order), primaryActionTitle
  ("Set Next"/"Set Open"), statusText, voiceOverAnnouncement, and notification
  title/body. 13 new unit tests in CaptureCoreTests.
- CompletionRowContent.swift: mapped task_toggle_route/_block_id/_pomodoro_name span
  kinds to .route/.blockID/.section; covered in CompletionRowContentTests.
- CapturePanelModel.swift: added togglePresentation/primaryActionTitle computed
  properties (previewResults.count==1 gate); completeSubmit/completePreview route
  statusText through the presentation (voiceOverAnnouncement on commit, statusText on
  preview) falling back to existing captureStatus() for non-toggle/batch; uniqueTargetURLs
  now also opens the day file when dayFileChanged, for Command-Return; added
  pomodoro_name to shouldRequestCompletion's needs and span-kind sets alongside the three
  task_toggle_* kinds.
- NotificationService.swift: successPresentation routes a single toggle capture through
  CaptureTogglePresentation's title/body; target paths now include the day file when the
  toggle changed it (mirrors Command-Return); added "task_toggle" to friendlyKindLabel.
- CapturePanelView.swift: one-line touch (Button("Capture") -> Button(model.primaryActionTitle))
  so the footer verb actually changes in the running app; no toggle string literals were
  added to the view itself.

Verified: `swift build` and `swift test` for CaptureCore pass on this Linux host (145
tests, all green except 2 pre-existing BobProcessClientTests process-termination/timeout
failures confirmed present on unmodified master too via git stash -u — a sandbox
process-signal limitation, unrelated to this change). Sources/BobMacCapture and
Tests/BobMacCaptureTests are macOS-only (#if os(macOS) in Package.swift) and cannot be
built or run on Linux; those edits (CapturePanelModel.swift, NotificationService.swift,
CapturePanelView.swift, and the two new BobMacCaptureTests files) were manually reviewed
against existing patterns but rest on macOS CI for compilation/test verification, per the
plan's own note about this phase's Linux/macOS split.

epic-symbols: none for this phase.

## Dependencies

- **Depends on:** [bob-cli-1z.3](bob-cli-1z.3.md) ✓ · ⧖ 2026-09-10
- **Blocks:** [bob-cli-1z.6](bob-cli-1z.6.md) ◐ · ⧖ 2026-09-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1z.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.5/README.md) | [bob-cli-1z.5](bob-cli-1z.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@9cce339`](https://github.com/bobs-org/bob-mac-capture/commit/9cce339ab8608eada48447bca5d90f20efeeac5d) | feat(capture-core): decode task\_toggle fields, add CaptureTogglePresentation, wire panel/notification | [bob-cli-1z.5](bob-cli-1z.5.md) | 2026-09-10 15:31:24 EDT |
