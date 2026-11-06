# Bead: bob-cli-hl.5.1.4 — Fold merge landing groups and remove duplicate target blocks

[Bead Pages](../README.md) / [bob-cli-hl.5.1](bob-cli-hl.5.1.md) / bob-cli-hl.5.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.md) · **Assignee:** `bob-cli-hl.5.1.4` · **Size:** medium
**Created:** 2026-11-06 01:47:45 EST · **Closed:** 2026-11-06 04:46:36 EST
**Plan:** [202611/capture\_merge\_in\_mac.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_mac.md)

## Description

landing: fold contiguous merge-target rows by Bob's origin identity for both arrows, preserve authored children and source tombstones, and show each created target's exact block once. Verify keyboard disclosure and narrow layouts.

## Notes

[2026-11-06T09:46:30Z · bob-cli-hl.5.1.4--4] PROPOSED FOLLOW-UP: Stabilize the Mac Capture keyboard/alias CI failures — current exact-SHA run 42190434184 (snapshot 61142bf0bb4008266bdb99a8788dd7aaed4a099f) and clean-base e30a2f4 with only the required .mergeIn compile fix, run 42194918104 (snapshot a9f71ff440d304c0616fb7c6054d492297014bd9), share 16 failed test names; the one unmatched failure differs (current: CaptureMoveChoiceModelTests.testMoveThenPullInBackAndInboxCarryOneAnswerAndSeed; clean base: CaptureSeparatorToggleTests.testUndoAfterSlashAliasRestoresLiteralWithoutRetriggering). Investigate the shared baseline failures and varying test outcome.

[2026-11-06T09:46:36Z · bob-cli-hl.5.1.4--4] Verified just portable-check passed (2,239 tests, 1 skipped). Exact-SHA Mac run 42190434184 passed lint and build but failed 17 tests; clean base e30a2f4 with only the required .mergeIn compile fix built and failed tests in run 42194918104, reproducing 16 of 17 names with one differing failure. Epic-symbol audit was clear; recorded the baseline CI follow-up.

## Dependencies

- **Depends on:** [bob-cli-hl.5.1.3](bob-cli-hl.5.1.3.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hl.5.1.5](bob-cli-hl.5.1.5.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.1.4.md) | [bob-cli-hl.5.1.4](bob-cli-hl.5.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@6d659eb`](https://github.com/bobs-org/bob-mac-capture/commit/6d659eb244653c22fcc095914556e008ab311153) | feat(capture): fold merge targets in previews | [bob-cli-hl.5.1.4](bob-cli-hl.5.1.4.md) | 2026-11-06 04:47:39 EST |
