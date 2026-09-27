# Bead: bob-cli-28.4 — Bob Mac Capture active-task picker and link/start preview

[Bead Pages](../README.md) / [bob-cli-28](README.md) / bob-cli-28.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0t3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0t3.md) · **Assignee:** `bob-cli-28.4` · **Size:** medium
**Created:** 2026-09-27 10:38:09 EDT · **Closed:** 2026-09-27 12:51:49 EDT
**Plan:** [202609/active\_task\_link.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/active_task_link.md)

## Description

mac-capture: decode the new context, candidates and kind in bob-mac-capture, render an active-task picker, preview and notify link/move/start outcomes, and cover everything with fake-bob tests and macOS CI.

## Notes

[2026-09-27T16:51:35Z · bob-cli-28.4] PROPOSED FOLLOW-UP: BobProcessClientTests.testCancellationTerminatesProcess and testRunTerminatesAndThrowsTimedOut fail on Linux, reproduce identically on clean base tree (process-termination semantics), unrelated to mac-capture phase

[2026-09-27T16:51:40Z · bob-cli-28.4] PROPOSED FOLLOW-UP: linked bob-mac-capture work left uncommitted in workspace; land agent must commit, push, and confirm the macOS 26 SwiftPM CI run (app target cannot compile on Linux, so CapturePanelModel/NotificationService/CapturePanelView changes are parse-checked only)

[2026-09-27T16:51:49Z · bob-cli-28.4] mac-capture done in linked bob-mac-capture: active_task decode/picker (queued-first rows, Now/Planned/Not-queued badges), pomodoro_link preview/footer/notifications via new CapturePomodoroLinkPresentation, fake-bob fixtures for ^/accept/link/start/near-miss/solo-@. Verified: CaptureCore swift test 204/206 (2 failures reproduce on clean base tree, noted as follow-up); app-target files parse-checked (macOS-only compile). No epic-symbol entries. Push + macOS CI confirmation left for land agent (noted as follow-up).

## Dependencies

- **Depends on:** [bob-cli-28.3](bob-cli-28.3.md) ✓ · ⧖ 2026-09-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-28.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-28.4/README.md) | [bob-cli-28.4](bob-cli-28.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@9e61a77`](https://github.com/bobs-org/bob-mac-capture/commit/9e61a773eff320c748e160107e17f0b5f92b9cf6) | feat(capture): active-task pomodoro link completion, preview and notifications | [bob-cli-28.4](bob-cli-28.4.md) | 2026-09-27 12:53:44 EDT |
