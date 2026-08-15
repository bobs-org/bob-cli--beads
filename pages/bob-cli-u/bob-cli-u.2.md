# Bead: bob-cli-u.2 — Beautiful stateful macOS selection and prompt

[Bead Pages](../README.md) / [bob-cli-u](README.md) / bob-cli-u.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.02a](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.02a.md) · **Assignee:** `bob-cli-u.2` · **Size:** medium
**Created:** 2026-08-15 10:10:31 EDT · **Closed:** 2026-08-15 11:21:49 EDT
**Plan:** [202608/file\_plus\_any\_task.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/file_plus_any_task.md)

## Description

mac_capture_task_id_prompt: build grouped task presentation, inline ID authoring, reliable state transitions, and end-to-end app coverage.

## Notes

[2026-08-15T14:27:42Z · 02b] RELATED VALIDATION FAILURE: macOS CI has failed since commit 593398a in CapturePanelModelTests.testTaskBlockIDRouteSpanUsesCachedRouteCompletion (Actions run 31884302308, XCTAssertFalse at line 474). This is separate from the just install compile blocker, but it exercises the completion state path owned by this phase and will prevent a clean just test validation after the build is repaired. Preserve/repair the cached-route-versus-process-completion contract while implementing the stateful task-ID prompt.

[2026-08-15T15:21:49Z · bob-cli-u.2] Implemented macOS @route+ missing-ID prompt/client/UI/tests/docs. Verified git diff --check, bash -n Tests/Fixtures/fake-bob, fake-bob all-task completion and capture-task-id success/failure JSON, and swift build --target CaptureCore. macOS just format-lint/build/test/bundle were attempted but blocked by this Linux workspace lacking selected Apple developer tools (exit 69).

[2026-08-15T15:23:22Z · bob-cli-u.2] Verified linked bob-mac-capture Add block ID implementation: git diff --check passed; fake-bob syntax/direct contract checks passed; swift build --target CaptureCore passed; full macOS just recipes blocked here by missing Xcode/Apple developer tools.

## Dependencies

- **Depends on:** [bob-cli-u.1](bob-cli-u.1.md) ✓ · ⧖ 2026-08-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-u.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-u.2/README.md) | [bob-cli-u.2](bob-cli-u.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@dff08a7`](https://github.com/bobs-org/bob-mac-capture/commit/dff08a7ffaa3e9ba1547566a5806ed7d75a8c471) | feat(capture): add task ID assignment prompt | [bob-cli-u.2](bob-cli-u.2.md) | 2026-08-15 11:24:13 EDT |
