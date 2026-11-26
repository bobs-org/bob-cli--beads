# Bead: bob-cli-ph.8.1.5 — Drawer title newline and closing-star overtype

[Bead Pages](../README.md) / [bob-cli-ph.8.1](bob-cli-ph.8.1.md) / bob-cli-ph.8.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.5` · **Size:** medium
**Created:** 2026-11-25 20:56:01 EST · **Closed:** 2026-11-26 02:29:36 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

## Description

title-keys: at the end of a Bob-authorized drawer title, newline keys step past the closing `**` into a nested note and a typed `*` steps over the closing pair.

## Notes

[2026-11-26T07:27:22Z · bob-cli-ph.8.1.5--3] PROPOSED FOLLOW-UP: Fix CaptureDrawerPipelineTests.swift test-compilation errors: five references fail with compiler diagnostic cannot find 'model' in scope on both the phase source SHA 7d6e12a7397bbb270a616a06357c58dddaf832f8 (CI snapshot 3b841ce02eac49ffcb9c947b927ed62fc6fb88bb, run 45772531216; lines 261:20, 298:49, 310:49, 320:49, 658:63) and clean base SHA c561b26a0a8d39de5996ec470c5eae3959d09937 (CI snapshot 33d0e8b6b24f686a5dd197cc3215f20bf967700f, run 45774001812; lines 173:20, 210:49, 222:49, 232:49, 364:63). Both macos-ci-check runs pass formatting and build, then fail compiling tests; the clean-base reproduction makes this pre-existing rather than phase-specific. The CI logs include watchdog-script text, but the underlying failure is test compilation, not a test hang.

[2026-11-26T07:29:36Z · bob-cli-ph.8.1.5--3] Verified phase source SHA 7d6e12a7397bbb270a616a06357c58dddaf832f8 is clean. Exact-SHA macOS CI passes format and build but fails compiling CaptureDrawerPipelineTests.swift with five cannot-find-model diagnostics; the identical failure reproduces on clean base c561b26a0a8d39de5996ec470c5eae3959d09937, and the PROPOSED FOLLOW-UP records both runs and locations. sase bead epic-symbols reported no entries. Removed the clean-base worktree; final phase and primary checkout status/diff are clean.

## Dependencies

- **Depends on:** [bob-cli-ph.8.1.4](bob-cli-ph.8.1.4.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.5.md) | [bob-cli-ph.8.1.5](bob-cli-ph.8.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7d6e12a`](https://github.com/bobs-org/bob-mac-capture/commit/7d6e12a7397bbb270a616a06357c58dddaf832f8) | feat(capture): handle drawer title newline and star overtype | [bob-cli-ph.8.1.5](bob-cli-ph.8.1.5.md) | 2026-11-26 01:51:48 EST |
