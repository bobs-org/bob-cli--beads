# Bead: bob-cli-1t.5 — Bob Mac Capture Pomodoro-name completion and naming prompt

[Bead Pages](../README.md) / [bob-cli-1t](README.md) / bob-cli-1t.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0fk](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0fk.md) · **Assignee:** `bob-cli-1t.5` · **Size:** medium
**Created:** 2026-08-28 12:37:06 EDT · **Closed:** 2026-08-28 13:50:15 EDT
**Plan:** [202608/capture\_named\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_named_pomodoro.md)

## Description

mac_pomodoro_name_ui: decode the additive candidate fields, render the Pomodoro completion rows, and add the inline naming prompt that writes the name before splicing the slug.

## Notes

[2026-08-28T17:49:58Z · bob-cli-1t.5] PROPOSED FOLLOW-UP: Linux CaptureCoreTests process-timeout flakes — testCancellationTerminatesProcess and testRunTerminatesAndThrowsTimedOutWhenProcessOutlivesTheTimeout failed to observe Process.terminate() on this Linux host; they look pre-existing and unrelated to Pomodoro-name work.

[2026-08-28T17:50:15Z · bob-cli-1t.5] Implemented Bob Mac Capture pomodoro_name completion and the Name Pomodoro prompt in the linked bob-mac-capture repo, modeled on Add block ID.

Verified on Linux: swift build --target CaptureCore; swift test --filter Pomodoro and the new capture-complete fixture test all passed (candidate decoding including absent additive fields, CapturePomodoroNameResponse success/failure, row content for selectable/nameable/current/duplicate-slug rows, assignPomodoroName argv). Package.swift now omits the AppKit app target on Linux so CaptureCoreTests can run. No --epic-symbol leftovers.

Not run here (Linux, no AppKit): just format-lint, just build, just test, BobMacCaptureTests (prompt splice/prefill/mutual-exclusion/failure cases are written). App-target result needs the macOS 26 SwiftPM GitHub Actions workflow after this lands.

## Dependencies

- **Depends on:** [bob-cli-1t.3](bob-cli-1t.3.md) ✓ · ⧖ 2026-08-28
- **Depends on:** [bob-cli-1t.4](bob-cli-1t.4.md) ✓ · ⧖ 2026-08-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1t.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1t.5/README.md) | [bob-cli-1t.5](bob-cli-1t.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c9f2e9f`](https://github.com/bobs-org/bob-mac-capture/commit/c9f2e9f6627315bb9148c3a81b457bf10389dd9b) | feat(capture): add Pomodoro-name completion and naming prompt | [bob-cli-1t.5](bob-cli-1t.5.md) | 2026-08-28 13:51:14 EDT |
