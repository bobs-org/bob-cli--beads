# Bead: bob-cli-an.6.6.6.5.6.5.5.6.3 — Find and fix the stray ref show in the Mac hidden-library refresh test

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.3` · **Size:** medium
**Created:** 2026-10-25 08:44:09 EDT · **Closed:** 2026-10-25 09:00:04 EDT
**Plan:** [202610/backlog\_batch9\_epipe\_listen\_publish\_refresh\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md)

## Description

mac-hidden-refresh-flake: resolve bob-cli-c0 by finding which code path spawns ref show during testHiddenLibraryRefreshDoesNotHydrateInspector and fixing the model or test ordering without weakening the assertion.

## Notes

[2026-10-25T12:59:53Z · bob-cli-an.6.6.6.5.6.5.5.6.3] Root cause: prepareForPresentation() calls inspectorRequested() unconditionally (RefsPanelModel.swift:862), which schedules a 120ms-debounce load in RefsInspectorLoader.schedule(); the loader had no visibility check, so the task fired ref show even while hidden. refreshInspectorAfterLibraryRefresh() was already guarded by panelIsVisible(), so the stale prepare-time task was the only stray path. Fix: loader gains shouldHydrate (default true), checked at fire time at top of load(); model wires it to panelIsVisible. Production show() still hydrates because the check runs 120ms later when the panel is visible. Test unchanged, assertion at full strength. Local evidence: just portable-check exit 0 (1648 Linux tests pass); mac scratch copy bundle.sh + just typecheck-tests PASS, scratch removed. Watch SHA: current bob-mac-capture master 8fda38d + this fix; flaky test testHiddenLibraryRefreshDoesNotHydrateInspector to be confirmed on macOS CI.

[2026-10-25T13:00:04Z · bob-cli-an.6.6.6.5.6.5.5.6.3] Fixed hidden-panel inspector guard: RefsInspectorLoader.shouldHydrate wired to panelIsVisible, checked at fire time. Verified: just portable-check exit 0 (1648 tests), mac bundle.sh + just typecheck-tests PASS. No test changes; target task bob-cli-c0 left open for lander. Watch macOS CI for testHiddenLibraryRefreshDoesNotHydrateInspector on landed SHA.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.3](bob-cli-an.6.6.6.5.6.5.5.6.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.3/README.md

<!-- sase:referenced-by:end -->
