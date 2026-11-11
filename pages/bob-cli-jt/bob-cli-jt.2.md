# Bead: bob-cli-jt.2 — Bob Mac Capture double-tap, tips, and docs

[Bead Pages](../README.md) / [bob-cli-jt](README.md) / bob-cli-jt.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b1.md) · **Assignee:** `bob-cli-jt.2` · **Size:** medium
**Created:** 2026-11-10 15:05:11 EST · **Closed:** 2026-11-10 19:02:38 EST
**Plan:** [202611/backslash\_percent\_alias.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backslash_percent_alias.md)

## Description

mac-directive-alias: generalize the app's backslash/slash double-tap arm and probe to a `%` reply, add the `%` tip trigger and directive_menu lesson, refresh fixtures, tests, and docs, and land through macOS CI.

## Notes

[2026-11-10T21:27:42Z · bob-cli-jt.2] PROPOSED FOLLOW-UP: Bring the bob-docs reference pages under the 6,000-word cap — docs-check reports the same five over-budget pages on this phase tree and a clean base snapshot (capture-panel, capture-previews, keyboard, protocol, bob-navigation-hotkeys).

[2026-11-10T22:00:08Z · bob-cli-jt.2--1] PROPOSED FOLLOW-UP: Stabilize four pre-existing CaptureAliasTipPanelTests CI failures — exact-SHA run 42887591461 on clean base 90b6f9e reproduced testEditBeforeTheReplyDropsTheTip, testFilteringKeepsTheShownTipAnchoredToTheSigil, testOptionTypedHashOpensTheHashTip, and testTypingQueryBeforeTheRouteListOpensKeepsTheTip; the phase run repeated the same four. Adjacent alias-tip XCTest timing flake bob-cli-jk tracks a different test in the same class, not these failures.

[2026-11-10T23:06:58Z · bob-cli-jt.2--4] PROPOSED FOLLOW-UP: Stabilize unrelated fast-double-equals alias timing test — exact-SHA macOS CI run 42916862918 (snapshot 0a08ca1e65976107f56406d3def75b97013ea56e) again failed CaptureRelationEqualsAliasTests.testFastDoubleEqualsBeforeReplyCollapsesToOne; clean-base run 42887591461 passed it, while the same failure was observed on an earlier phase run. This is outside the backslash-to-percent change.

[2026-11-10T23:37:32Z · bob-cli-jt.2--5] PROPOSED FOLLOW-UP: Investigate unrelated CaptureRelationPanelTests.testRelationCardRenameMergeArmsAndApplies failure — exact-SHA macOS CI run 42921174259 at 56af1e26f9af96fed12c6b80e9267c78fefdf95c failed this relation-panel test; no relation-panel code or tests are part of this phase diff.

[2026-11-11T00:02:24Z · bob-cli-jt.2--6] PROPOSED FOLLOW-UP: Stabilize unrelated CaptureSeparatorToggleTests.testOlderBobMoveAliasReplyLeavesLiteralWithoutOpeningPicker — exact-SHA CI runs 42916862918 (snapshot 0a08ca1e) and 42925346886 (snapshot 8028dbf) failed only the assertion that capture-rewrite --cursor 20 appeared after a 200 ms wait; clean-base run 42887591461 and phase run 42921174259 passed it. The test and move-alias response path were unchanged in this phase, so this appears to be process/timing flakiness.

[2026-11-11T00:02:38Z · bob-cli-jt.2--6] Verified on exact tree 8028dbfe160301fda48dc49ee64cfb7c1505ff54: just portable-check passed (2,454 tests, 1 skipped), and macOS CI run 42925346886 passed the phase-required % directive-tip and backslash double-tap tests. The run retained only the three documented clean-base alias-tip failures and the separately recorded move-alias timing follow-up. The clean-base docs-check cap issue is recorded. Epic symbol audit found no leftovers.

## Dependencies

- **Depends on:** [bob-cli-jt.1](bob-cli-jt.1.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-jt.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-jt.2.md) | [bob-cli-jt.2](bob-cli-jt.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@df8045f`](https://github.com/bobs-org/bob-mac-capture/commit/df8045f1faa90828d128b1e8a0cade59980109e8) | feat(capture): add percent directive alias support | [bob-cli-jt.2](bob-cli-jt.2.md) | 2026-11-10 19:03:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-jt.2--6][1] | Need the phase scope, design, and accumulated verification notes before closing or fixing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-jt.2.md

<!-- sase:referenced-by:end -->
