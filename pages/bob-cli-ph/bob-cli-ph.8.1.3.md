# Bead: bob-cli-ph.8.1.3 — Semibold drawer titles and dimmed delimiters in the draft editor

[Bead Pages](../README.md) / [bob-cli-ph.8.1](bob-cli-ph.8.1.md) / bob-cli-ph.8.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.3` · **Size:** medium
**Created:** 2026-11-25 20:56:00 EST · **Closed:** 2026-11-25 23:39:06 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

## Description

draft-styling: paint drawer_bullet titles semibold in the section family and drawer_marker delimiters in tertiary ink that returns to full ink at the caret, through a portable span helper the typing phases reuse.

## Notes

[2026-11-26T04:21:26Z · bob-cli-ph.8.1.3] Implemented Bob-span-driven draft styling: drawer titles use the section color and semibold monospaced font; delimiters use tertiary ink away from the caret and primary ink when touched; repaint clears inherited font attributes. Added a portable CaptureCore drawer span adapter for subsequent typing phases. Verified: Athena just portable-check passed (2,785 tests, 1 skipped); Mac scratch Scripts/bundle.sh and just typecheck-tests passed. Exact-SHA Scripts/macos-ci-check remains required before close.

[2026-11-26T04:38:38Z · bob-cli-ph.8.1.3--1] PROPOSED FOLLOW-UP: Diagnose macOS 26 SwiftPM Test-step fatalError during test-target compilation; reproduced on pre-change clean base 4d9e845 (CI 45753263190) and styling snapshot acfbfe9 (CI 45755244484), with no test name or hang sample and Build/Lint passing.

[2026-11-26T04:39:06Z · bob-cli-ph.8.1.3--1] Verified styling: Athena just portable-check passed (2,785 tests, 1 skipped); macOS scratch Scripts/bundle.sh and just typecheck-tests passed; exact-SHA CI passed Lint and Build. CI Test ended in fatalError without a test name or hang sample; the same Test failure is present on pre-change clean base 4d9e845 (run 45753263190), recorded as a PROPOSED FOLLOW-UP. Epic-symbol check found no entries.

## Dependencies

- **Depends on:** [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.4](bob-cli-ph.8.1.4.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.3.md) | [bob-cli-ph.8.1.3](bob-cli-ph.8.1.3.md) | 0 |
