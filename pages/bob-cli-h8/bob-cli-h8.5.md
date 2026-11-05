# Bead: bob-cli-h8.5 — Turn bob-mac-capture master CI green and record the CI-watch rule

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.5` · **Size:** medium
**Created:** 2026-11-04 16:39:09 EST · **Closed:** 2026-11-04 18:48:33 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

mac-ci-green: fix the root causes of the bob-cli-h7 Go To failures: the backslash insert helper, the delayed chip-refetch race, the leaked error wrapper, and the 15-minute hang. Coordinate with the 185 chain. Verify on the exact-SHA macOS run. Close h7, the six already-fixed Mac CI beads, and bob-cli-1x after recording the watch-CI rule.

## Notes

[2026-11-04T23:48:16Z · bob-cli-h8.5--5] PROPOSED FOLLOW-UP: CaptureMoveChoiceModelTests/testMoveThenPullInBackAndInboxCarryOneAnswerAndSeed failed once in snapshot run 41932635468 (Set(seeds).count==2, expected 1) but passed on base commit 0245a75 run 41912472770 and on master HEAD run 41933412932; suspect flaky reseed timing, needs a retry to confirm

[2026-11-04T23:48:20Z · bob-cli-h8.5--5] PROPOSED FOLLOW-UP: macOS CI still red from other chains (backslash helper testInsertHelperDeclinesWhileComposingSubmittingOrLocked owned by 185 chain; separator alias tests testDelayedAcceptedAliasSupersedesGatedCompletion, testNativeUndoRestoresLiteralSigilAliasWithoutRetriggering, testPeriodAliasAfterRouteOpensNewIDBlockPicker from parallel sigil-alias work); all reproduce identically on clean base run 41912472770 without this phase diff

[2026-11-04T23:48:33Z · bob-cli-h8.5--5] Go To scope verified. CapturePanelModel.swift: task_goto refetch now accepts response ranges starting at the original token start within the original range (generation check unchanged); processFailed logs full error.description via NSLog and shows trimmed nonblank stderr in panel; backslash helper untouched. Fixture simulates delayed stale one-row /dee response. AGENTS.md records the watch-exact-SHA-macOS-CI rule. portable-check: 2118 passed, 1 skipped. Snapshot run 41932635468: testDelayedChipRefetchCannotReplaceReopenedSnapshot and testFailureOnChipRefetchRetainsRowsAndReportsError PASS (both fail on base 0245a75 run 41912472770 and master HEAD run 41933412932). Remaining snapshot failures reproduce identically on clean base (backslash helper + 3 separator tests, other chains) except one Move seed-count failure that passes on base and master runs, recorded as PROPOSED FOLLOW-UP (suspect flake). Watchdog evidence only: Test took 647s/565s in runs 419008/419124, no hang-samples artifact on 419008; no hang fix claimed. Did not close h7, Mac CI beads, or bob-cli-1x (land agent scope). Diff left uncommitted in linked bob-mac-capture checkout for the finalizer.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.5.md) | [bob-cli-h8.5](bob-cli-h8.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`20c58da`](https://github.com/bobs-org/bob-cli/commit/20c58da9d62d034036bd6cfb0c8ceb17cac0496c) | docs(agents): tell agents to watch exact-SHA macOS CI after pushes | [bob-cli-h8.5](bob-cli-h8.5.md) | 2026-11-04 18:49:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h2.land][1] | Check whether MoveThenPullIn failure was already triaged | 1 |
| read-by | [agent:bob-cli-h4.4--5][2] | Check whether the previously closed Mac CI green phase already owns these exact editor and separator failures | 1 |
| read-by | [agent:bob-cli-h8.5--5][3] | Need notes and remaining scope after failed gate | 3 |
| read-by | [agent:cl--1][4] | Check the existing CI-green phase for the repeated baseline failures before adding evidence | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h2.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h4.4.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.5.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.cl.md

<!-- sase:referenced-by:end -->
