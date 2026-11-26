# Bead: bob-cli-ph.8.1.4 — Bob-driven star expansion and atomic Backspace

[Bead Pages](../README.md) / [bob-cli-ph.8.1](bob-cli-ph.8.1.md) / bob-cli-ph.8.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.4` · **Size:** medium
**Created:** 2026-11-25 20:56:01 EST · **Closed:** 2026-11-26 01:07:40 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

## Description

star-expansion: a physical `*` asks capture-rewrite for expand_drawer_marker, applies it as one undoable native edit, absorbs a queued star, and deletes an empty `****` as one Backspace.

## Notes

[2026-11-26T06:07:19Z · bob-cli-ph.8.1.4--1] PROPOSED FOLLOW-UP: Diagnose macOS 26 SwiftPM Test-step bare fatalError with no test name and empty test-hang sample; reproduced identically on pre-change clean base 4d9e845 (CI run 45753263190, job 139685800937) and on this phase snapshot e18c852a101b7f54c44b373ab34b9341739417f8 (CI run 45763712398, job 139719471921) - both Lint+Build green, Test red, watchdog "swift test ran longer than 20 minutes; sampling xctest", then bare "error: fatalError" exit 1, no "Test Case ... failed" lines, no files in test-hang/render-fixtures. Same signature as PROPOSED FOLLOW-UP on bob-cli-ph.8.1.3 (runs 45753263190 and 45755244484).

[2026-11-26T06:07:40Z · bob-cli-ph.8.1.4--1] Verified: hosted drawer pipeline (12 new pipeline tests: expansion families, undo/redo, queued star, both Backspace paths, literals, stale/failed/pasted, requirement regression) plus 5 skeleton and 4 response-decoding portable tests; portable-check 2795 tests 0 failures on Athena; Mac check-scripts green (re-observed this turn: 9 + 43 script tests OK); docs-check stages green (prior turn full green; this turn all stages through tutorial+media passed before the wrapper timeout cut the final pytest suite, no failures seen); exact-SHA CI https://github.com/bobs-org/bob-mac-capture/actions/runs/45763712398 (snapshot e18c852a101b7f54c44b373ab34b9341739417f8) Lint+Build green, Test red with bare fatalError identical to clean-base 4d9e845 run 45753263190 (recorded as PROPOSED FOLLOW-UP); mac typecheck unverified (mac offline, CI Build green covers Sources compile)

## Dependencies

- **Depends on:** [bob-cli-ph.8.1.3](bob-cli-ph.8.1.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.5](bob-cli-ph.8.1.5.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.4.md) | [bob-cli-ph.8.1.4](bob-cli-ph.8.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c561b26`](https://github.com/bobs-org/bob-mac-capture/commit/c561b26a0a8d39de5996ec470c5eae3959d09937) | feat(mac-capture): drive drawer star expansion and atomic Backspace through capture-rewrite | [bob-cli-ph.8.1.4](bob-cli-ph.8.1.4.md) | 2026-11-26 00:43:34 EST |
