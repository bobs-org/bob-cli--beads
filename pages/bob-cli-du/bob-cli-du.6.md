# Bead: bob-cli-du.6 — Obsidian relation writer folds the Done into the source write

[Bead Pages](../README.md) / [bob-cli-du](README.md) / bob-cli-du.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.aw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.aw.md) · **Assignee:** `bob-cli-du.6` · **Size:** large
**Created:** 2026-10-28 14:49:53 EDT · **Closed:** 2026-10-28 16:27:50 EDT
**Plan:** [202610/relation\_complete\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_complete_labels.md)

## Description

nav-complete-writer: load closing labels with the both-lists rule, add planRelationCompleteEffects, fold the cycler's Done line into the source write, gate stale commits, run the post-Done pass after the stage closes, compose one notice, and settle the walk once.

## Notes

[2026-10-28T19:48:02Z · bob-cli-du.6] PROPOSED FOLLOW-UP: Reconcile cycler API v3 with the accepted cycler-done-api contract — bob-plugins 3c84ee3 exposes completeTaskLineText as an unchecked string rewrite, not {ok,lineText}/{ok:false,reason}; direct calls on Cancelled and [repeat:: daily] task lines both return [x] with a new completion date. Reproduced through scripts/task-status-cycler-harness.cjs using date 2026-10-28. The complete-vectors test does not call the API for refused/already-closed cases. finalizeClosedTasks likewise returns reopened and successors rather than the planned recovered/offered/picked fields. nav-complete-writer can safely consume the shipped API behind its own required verdict gate; the land agent should triage the API contract mismatch without reopening phase .5 here. Searched existing bug tasks and the last-week bug sweep; no semantic duplicate found (bob-cli-3k concerns Alt status cycling instead).

[2026-10-28T20:27:50Z · bob-cli-du.6--1] Implemented the relation completion writer and shared close preview. Stable .7 seam: planRelationCompleteEffects(args) returns frozen sources/completes/refusals/refuse; relationClosePreviewForChanges(args) returns cancel/complete plans plus closeEffects and expectedCloseEffects; applyRelationEdit accepts expectedCloseEffects and returns closeEffects, committed completedIdentities, closingRows, and stale status; finalizeRelationCompleteOutcome owns picker close, one cycler finalizeClosedTasks pass, notice composition, and one review settlement. Validation: isolated npm run docs:check passed (exit 0; all implemented gates passed, 447 passed/1 skipped); post-sync git diff --check passed; canonical and plugin relation_complete/vectors.json files are byte-identical; bob plugins sync --repo deployed bob-navigation-hotkeys from this checkout (1 copied); sase bead epic-symbols bob-cli-du.6 reports no entries. Preserved the existing cycler API mismatch PROPOSED FOLLOW-UP for parent triage.

## Dependencies

- **Depends on:** [bob-cli-du.5](bob-cli-du.5.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-du.7](bob-cli-du.7.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.6.md) | [bob-cli-du.6](bob-cli-du.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7c088a5`](https://github.com/bobs-org/bob-plugins/commit/7c088a54a2127a922048fbddb7964dd9d55cc561) | feat(navigation): complete relation writer effects | [bob-cli-du.6](bob-cli-du.6.md) | 2026-10-28 16:37:37 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-du.6--1][1] | Review the assigned implementation epic before recording validation evidence and closing it | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.6.md

<!-- sase:referenced-by:end -->
