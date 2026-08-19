# Bead: bob-cli-10.5 — \`#\`-triggered task-section completion in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-10](README.md) / bob-cli-10.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.085](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.085.md) · **Assignee:** `bob-cli-10.5` · **Size:** medium
**Created:** 2026-08-19 16:04:39 EDT · **Closed:** 2026-08-19 18:00:11 EDT
**Plan:** [202608/capture\_task\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_task_sections.md)

## Description

mac_app: decode the additive `task_section` context and `sub_bullet_section` span in the linked bob-mac-capture app, open the completion popup as soon as `#` follows a resolved `@route+block-id`, render task-section rows with the parent task and a section-content badge, keep every existing context and the bare `#` Pomodoro-note marker unaffected, and document plus test the behavior.

## Notes

[2026-08-19T22:00:11Z · bob-cli-10.5] Implemented # -triggered task_section completion in bob-mac-capture (span mapping, row content, popup needs, ungrouped list, fake-bob, README). CaptureCore Linux type-check succeeded; CaptureCoreTests for row content, span mapping, and JSON decode passed. App/BobMacCaptureTests were not run here (need macOS/AppKit).

[2026-08-19T22:02:04Z · bob-cli-10.5] CaptureCore Linux type-check and CaptureCoreTests for task-section row content, span mapping, and JSON decode passed. # after resolved @route+block-id opens task_section completion; grouping and Add-block-ID stay task-only; bare # Pomodoro marker and @route# note-section completion unchanged. App/BobMacCaptureTests not run (no Apple toolchain on this host).

## Dependencies

- **Depends on:** [bob-cli-10.4](bob-cli-10.4.md) ✓ · ⧖ 2026-08-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-10.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-10.5/README.md) | [bob-cli-10.5](bob-cli-10.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@17720b3`](https://github.com/bobs-org/bob-mac-capture/commit/17720b39aec1836ba0bbf4c2292eeb3d294ce7bf) | feat(capture): complete task sections after @route+block-id# | [bob-cli-10.5](bob-cli-10.5.md) | 2026-08-19 18:03:22 EDT |
