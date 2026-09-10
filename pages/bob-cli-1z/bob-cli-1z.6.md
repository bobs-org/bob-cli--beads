# Bead: bob-cli-1z.6 — Bob Mac Capture toggle preview, highlighting, and documentation

[Bead Pages](../README.md) / [bob-cli-1z](README.md) / bob-cli-1z.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ir](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ir.md) · **Assignee:** `bob-cli-1z.6` · **Size:** medium
**Created:** 2026-09-10 13:19:09 EDT · **Closed:** 2026-09-10 15:43:35 EDT
**Plan:** [202609/capture\_task\_toggle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_task_toggle.md)

## Description

mac-preview: render the before/after toggle preview and destination detail, color the new `task_toggle_*` spans, and document the flow in the app README.

## Notes

[2026-09-10T19:43:13Z · bob-cli-1z.6] PROPOSED FOLLOW-UP: Investigate Linux BobProcessClient process termination tests — `swift test` in bob-mac-capture reproducibly fails `testCancellationTerminatesProcess` and `testRunTerminatesAndThrowsTimedOutWhenProcessOutlivesTheTimeout` on this host, while `swift test --skip BobProcessClientTests` passes the remaining CaptureCore suite.

[2026-09-10T19:43:35Z · bob-cli-1z.6] Implemented Bob Mac Capture task-toggle preview branch, core preview/accessibility presentation strings, tests, and README updates. Verified: sase bead epic-symbols bob-cli-1z.6 has no entries; swift test --filter CaptureTogglePresentationTests passes; swift test --skip BobProcessClientTests passes the remaining Linux CaptureCore suite. Local just format-lint and macOS app build/test were not available because no Apple developer tools are selected; full swift test is blocked by existing BobProcessClient termination timing failures, recorded as a PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-1z.5](bob-cli-1z.5.md) ✓ · ⧖ 2026-09-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1z.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.6/README.md) | [bob-cli-1z.6](bob-cli-1z.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@b979528`](https://github.com/bobs-org/bob-mac-capture/commit/b979528f2764d211ecd5c58c478ebb2110f6ed5e) | feat(capture): render task toggle previews | [bob-cli-1z.6](bob-cli-1z.6.md) | 2026-09-10 15:44:27 EDT |
