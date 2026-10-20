# Bead: bob-cli-a8.2 — Capture show, keystroke, and refresh optimizations

[Bead Pages](../README.md) / [bob-cli-a8](README.md) / bob-cli-a8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.9q` · **Assignee:** `bob-cli-a8.2` · **Size:** medium
**Created:** 2026-10-20 15:55:13 EDT · **Closed:** 2026-10-20 18:42:24 EDT
**Plan:** [202610/mac\_capture\_panel\_switch\_and\_perf.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_panel_switch_and_perf.md)

## Description

capture_perf: remove no-op republishes, the per-render executable stat, and repeated view-tree walks; add the fuzzy-matcher fast path and the coalesced show refreshes for targets and templates; add measuring signposts.

## Notes

[2026-10-20T22:42:24Z · bob-cli-a8.2] Implemented capture_perf (coalesce only): 5s show-refresh skip for capture-targets and templates (launch/watcher/recheck always refresh; follow-up template startRefresh still runs); @Published no-op guards on templates/targets/agenda; identityToken skipped when unsupportedGuardFlags empty; editor/filter first-responder cache; FuzzyMatcher greedy subsequence + matchPreFolded; OSSignposts capture-prepare/dismiss/templates-refresh. just portable-check: 1476 tests, 0 failures. Mac scratch: Scripts/bundle.sh compiled production; just typecheck-tests PASS BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, RefsCoreTests after field-lookup test fix. Epic symbols: none. Parent epic left open.

## Dependencies

- **Depends on:** [bob-cli-a8.1](bob-cli-a8.1.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a8.2/README.md) | [bob-cli-a8.2](bob-cli-a8.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1d5735a`](https://github.com/bobs-org/bob-mac-capture/commit/1d5735a67444ceb8a41ca3d81b9dfc7fa3634339) | perf(capture): coalesce show refresh and skip no-op publishes | [bob-cli-a8.2](bob-cli-a8.2.md) | 2026-10-20 18:51:08 EDT |
