# Bead: bob-cli-hz.1 — Mac relation label card flips direction

[Bead Pages](../README.md) / [bob-cli-hz](README.md) / bob-cli-hz.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.198](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.198.md) · **Assignee:** `bob-cli-hz.1` · **Size:** medium
**Created:** 2026-11-06 12:50:20 EST · **Closed:** 2026-11-06 14:48:59 EST
**Plan:** [202611/relation\_equals\_alias\_and\_direction\_flips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_equals_alias_and_direction_flips.md)

## Description

card-flip: in the Mac relation label card, `~`/`=` flip the relation in choose mode, edit the token, re-fetch catalog and verdicts, and support a fast `==` literal escape. Also adds teaching keycaps and fixes Escape from a Shift-Return card. Mac only.

## Notes

[2026-11-06T19:48:46Z · bob-cli-hz.1--2] PROPOSED FOLLOW-UP: bob-mac-capture master macOS Test is red — SHA 11dcba764bda3490bbc31d886a756aa1fe2fd645 run https://github.com/bobs-org/bob-mac-capture/actions/runs/42268256300 fails word-motion, comma rewrite, and separator-alias tests. Snapshot f1a0649adefc258f27535279f407e8ce3d399de1 run https://github.com/bobs-org/bob-mac-capture/actions/runs/42278074963 matched that set plus 5s waitUntil flakes testArmedDashEqualsFlipsInsteadOfRestoring (dash rewrite picker open before equals), testSlowSlashDoubleTapClosesMenuWithOneLiteralSlash, and testUndoAfterHashAliasRestoresLiteralWithoutRetriggering. All CaptureRelationPanelTests, CaptureEqualsGestureTests, pipe-suffix, and other FlipAlias tests passed.

[2026-11-06T19:48:59Z · bob-cli-hz.1--2] Verified card-flip: just portable-check 2257 tests; just docs-check; Mac scratch bundle.sh + just typecheck-tests TYPECHECK_OK; macos-ci-check snapshot f1a0649adefc258f27535279f407e8ce3d399de1 (base cbb50dc) lint+build green. Test step failed the master-red set (11dcba7 run 42268256300) plus 5s waitUntil flakes; every CaptureRelationPanelTests including Escape restore, Return-during-refetch, Tab-until-catalog, flip/==, OutOfOrder, plus testEmptyLabelReturnWithFollowingTailDropsOnlyPipeSuffix and testDependencyTailCommitPreservesSuffixByteForByte passed. No leftover --epic-symbol entries. Parent epic untouched. Memory records stay with bob-cli-hz.5.

## Dependencies

- **Blocks:** [bob-cli-hz.3](bob-cli-hz.3.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hz.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.1.md) | [bob-cli-hz.1](bob-cli-hz.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hz.1--1][1] | Need the phase scope, design file, and notes after macos-ci-check failed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.1.md

<!-- sase:referenced-by:end -->
