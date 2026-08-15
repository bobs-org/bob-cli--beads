# Bead: bob-cli-u.2 — Beautiful stateful macOS selection and prompt

[Bead Pages](../README.md) / [bob-cli-u](README.md) / bob-cli-u.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.02a](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.02a.md) · **Assignee:** `bob-cli-u.2` · **Size:** medium
**Created:** 2026-08-15 10:10:31 EDT
**Plan:** [202608/file\_plus\_any\_task.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/file_plus_any_task.md)

## Description

mac_capture_task_id_prompt: build grouped task presentation, inline ID authoring, reliable state transitions, and end-to-end app coverage.

## Notes

[2026-08-15T14:27:42Z · 02b] RELATED VALIDATION FAILURE: macOS CI has failed since commit 593398a in CapturePanelModelTests.testTaskBlockIDRouteSpanUsesCachedRouteCompletion (Actions run 31884302308, XCTAssertFalse at line 474). This is separate from the just install compile blocker, but it exercises the completion state path owned by this phase and will prevent a clean just test validation after the build is repaired. Preserve/repair the cached-route-versus-process-completion contract while implementing the stateful task-ID prompt.

## Dependencies

- **Depends on:** [bob-cli-u.1](bob-cli-u.1.md) ✓ · ⧖ 2026-08-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-u.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-u.2/README.md) | [bob-cli-u.2](bob-cli-u.2.md) | 0 |
