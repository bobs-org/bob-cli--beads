# Bead: bob-cli-41.2 — Present scoped and vault-wide plus task pickers in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-41](README.md) / bob-cli-41.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vw.md) · **Assignee:** `bob-cli-41.2` · **Size:** medium
**Created:** 2026-10-03 16:24:17 EDT · **Closed:** 2026-10-03 18:03:17 EDT
**Plan:** [202610/plus\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plus_task_picker.md)

## Description

plus_picker_mac: connect both plus scopes to the shared picker lifecycle and fuzzy presentation, including keys, focus, snapshot guards, ID naming, compatibility fallback, accessible visuals, and macOS tests.

## Notes

[2026-10-03T22:02:56Z · bob-cli-41.2] PROPOSED FOLLOW-UP: Linux Swift 6.0.3 cannot type-check CapturePomodoroClosePresentation.swift:609/625 (unable to type-check this expression in reasonable time) — reproduces identically on clean origin/master with `swiftc -typecheck Sources/CaptureCore/*.swift` and `swift test`; ParentTaskPickerPresentation.swift itself typechecks. Not bob-cli-1u (Linux BobProcessClient termination tests, closed) or bob-cli-3x (close tests after compile) or bob-cli-3m (CapturePreviewState.pending). AppKit/xcode-swift checks cannot run on this Linux host; they belong to existing macOS 26 CI (.github/workflows/ci.yml) and bob-cli-1x (watch bob-mac-capture CI after push).

[2026-10-03T22:03:17Z · bob-cli-41.2] Present scoped @file+ and vault-wide leading/prose-terminal + parent-task pickers in Bob Mac Capture against the phase-1 contract: decode picker descriptor/query/parent_replacement; shared card with Append/Select Task identity, + locator, All capture notes / note-file capsules, no Link & Start or pulls_forward; local fuzzy ranking; snapshot refetch, exact-match suppression, chip reopen, trigger_removal_range Backspace; lone-+ operator continuation (digit/second + once, empty filter only) with numeric filter/paste staying in the filter; ID prompt parentTaskPicker with vault parent_replacement or scoped returned ID; older Bob @file+ stays inline. CaptureCore typecheck of new files is clean; full CaptureCore swift test cannot compile on Linux Swift 6.0.3 because CapturePomodoroClosePresentation.swift:609/625 times out on clean origin/master (PROPOSED FOLLOW-UP). AppKit/xcode-swift panel, key-router, and design PNG tests are written but were not executed here; they run on existing macOS 26 CI. Parent epic bob-cli-41 left open. No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-41.1](bob-cli-41.1.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-41.3](bob-cli-41.3.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-41.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-41.2/README.md) | [bob-cli-41.2](bob-cli-41.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e9b5f81`](https://github.com/bobs-org/bob-mac-capture/commit/e9b5f811e0bf09b3e5a3464c905f7816ee57b648) | feat(capture): present scoped and vault-wide plus task pickers | [bob-cli-41.2](bob-cli-41.2.md) | 2026-10-03 18:04:28 EDT |
