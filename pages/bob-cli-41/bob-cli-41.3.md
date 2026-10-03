# Bead: bob-cli-41.3 — Verify the combined feature and polish the picker on macOS

[Bead Pages](../README.md) / [bob-cli-41](README.md) / bob-cli-41.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vw.md) · **Assignee:** `bob-cli-41.3` · **Size:** small
**Created:** 2026-10-03 16:24:17 EDT · **Closed:** 2026-10-03 18:28:25 EDT
**Plan:** [202610/plus\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plus_task_picker.md)

## Description

plus_picker_integration: exercise backend and app together in a fixture vault, verify operator and compatibility behavior, inspect native visuals and accessibility on macOS, and correct feature-specific integration issues.

## Notes

[2026-10-03T22:28:12Z · bob-cli-41.3] PROPOSED FOLLOW-UP: macOS CI and live AppKit/VoiceOver inspection blocked by bob-cli-3m (CapturePreviewState.pending compile) and bob-cli-3x (close tests once the suite compiles) — Linux host cannot run xcode-swift; plus-picker design-state/fixture tests were added, but light/dark/narrow-wide/VoiceOver still need a Mac host after those CI blockers.

[2026-10-03T22:28:25Z · bob-cli-41.3] Verified plus-picker integration in a fixture vault: vault-wide catalog excludes scratch/archive/done, keeps Unicode/long/duplicate/queued/ID-less rows; scoped @file+ plus missing/empty notes keep picker+empty catalog; +bank refetch at replacement.start returns empty query and the same token range; scoped accept/suffix, prose-terminal append, leading Ensure Next, later-item and authored-child walks insert once; lone + stays pomodoro_adjust on parse while capture-complete opens task_parent; +2/++/++3/+2=x stay operators. Mac: fake-bob +bank range rewrite, panel test expects full snapshot, fixture-driven presentation tests, Unicode/long and scoped-empty design states, locator comment. cargo fmt --check; 6 parent_tasks unit + 2 complete_parent_task CLI tests pass. Linux cannot run AppKit/xcode-swift; macOS 26 CI remains blocked by bob-cli-3m. epic-symbols had no leftovers. Parent epic bob-cli-41 left open.

## Dependencies

- **Depends on:** [bob-cli-41.1](bob-cli-41.1.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-41.2](bob-cli-41.2.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-41.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-41.3/README.md) | [bob-cli-41.3](bob-cli-41.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a960232`](https://github.com/bobs-org/bob-cli/commit/a960232b2a757046319949f0ad17947af5ac0eec) | test(capture): cover plus-picker catalog and operator walks | [bob-cli-41.3](bob-cli-41.3.md) | 2026-10-03 18:29:50 EDT |
| bob-mac-capture | [`bob-mac-capture@098e67e`](https://github.com/bobs-org/bob-mac-capture/commit/098e67e9861cd52a981d1f89a73a623b74d3bdd5) | test(capture): align plus-picker fixtures with backend refetch | [bob-cli-41.3](bob-cli-41.3.md) | 2026-10-03 18:30:29 EDT |
