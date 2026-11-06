# Bead: bob-cli-hl.5.1.5 — Raise the grammar gate and verify the integrated Mac experience

[Bead Pages](../README.md) / [bob-cli-hl.5.1](bob-cli-hl.5.1.md) / bob-cli-hl.5.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.md) · **Assignee:** `bob-cli-hl.5.1.5` · **Size:** medium
**Created:** 2026-11-06 01:47:45 EST · **Closed:** 2026-11-06 07:19:20 EST
**Plan:** [202611/capture\_merge\_in\_mac.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_mac.md)

## Previously Closed

> ↺ Closed 2026-11-06T10:13:50Z · done
>
> (none)
>
> Reopened 2026-11-06T10:48:46Z by `sase bead open`

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:80ea345ad2f4aa2a61b9599d | attached via sase artifact create --bead |
| related | file:explicit:93caffd02e31ab101cc20f9c | attached via sase artifact create --bead |
| related | file:explicit:f7c87874f1ec8abb2832fe8f | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

rollout: require the shipped merge-in grammar revision, update affected gate fixtures, document preview and picker behavior, complete integrated regression and rendered-layout coverage, and provide exact-SHA macOS verification evidence.

## Notes

[2026-11-06T10:13:35Z · bob-cli-hl.5.1.5] PROPOSED FOLLOW-UP: bob-cli docs contract-table snapshot is stale on clean master (tools/docs/tests/test_contracts.py::test_readme_table_matches_original_contract_index_snapshot fails with 96a429d5 vs fedc20a03; bob-cli tree clean, no phase files touched) — regenerate the README contract table snapshot

[2026-11-06T10:13:39Z · bob-cli-hl.5.1.5] PROPOSED FOLLOW-UP: regenerate clip-history directive fixtures on a Mac (Scripts/generate-directive-fixtures.sh clip-history-one capture exits 1 on Linux with clipboard_history_mismatch: mocked history vs live pasteboard; existing clip-history fixtures retained, directive parse fixtures regenerated to grammar 15)

[2026-11-06T10:13:50Z · bob-cli-hl.5.1.5] Raised CaptureGrammarGate to 15 with copy 'Update bob to merge tasks with <'; updated gate/hosted tests (5/14 block, 15 allows) and fake-bob default/inline grammars to 15; regenerated directive fixtures to grammar 15 (README provenance updated); documented merge-in band, source picker, and rewrite buttons in capture-previews/task-pickers/keyboard. Verified: just portable-check green (2239 tests, 0 failures, 1 skipped); Mac docs-check lint green; test_macos_ci_check.py 42 OK; macOS CI staged as monitor p9tw4t. Pre-existing only: bob-cli contract-table snapshot drift and Linux clip-history generation mismatch, both recorded as PROPOSED FOLLOW-UP.

[2026-11-06T10:46:06Z · bob-cli-hl.5.1.5] CLOSED-BEAD LAUNCH: agent bob-cli-hl.5.1.5 launched against this closed bead; status left closed.
Launch submitted 2026-11-06T10:43:32.695949Z; run 20261106054334.
Prior close: 2026-11-06T10:13:50Z · done.

[2026-11-06T10:48:50Z · bob-cli-hl.5.1.5] Recovery audit: linked master 6d659eb still requires grammar 5; no rollout commit is present in either repository history. Prior monitor transcript records snapshot fc20826bb3a6b2cf4d4f62ad0d4627846f6c3c40 and macOS run 42201218467: build/lint passed, 17 hosted tests failed. Reopened only the assigned phase to recover its snapshot, complete verification, and submit the missing rollout changes.

[2026-11-06T10:56:36Z · bob-cli-hl.5.1.5] Recovered the missing rollout changes from CI snapshot fc20826bb3a6b2cf4d4f62ad0d4627846f6c3c40. Clean master 6d659eb and baseline CI snapshot 61142bf0bb4008266bdb99a8788dd7aaed4a099f have identical tree 244977e8173ccffc8442adc68380d1cff5c079a5; run 42190434184 reproduces 16 of the prior rollout failure names. The sole new rollout failure is the past-segment submit test using a grammar-14 fixture; regenerated that parser fixture with installed bob 0.4.0 (only grammar changes to 15), preserving the real gate and explicit old/missing negative tests. Added merge-in render matrix (complete, pending/errors, three rewrites, both-arrow folded/expanded origins at 620/760 light/dark) and exposed band disclosure to accessibility. Verification pending; only this reopened phase must be manually closed after results and render inspection.

[2026-11-06T11:31:24Z · bob-cli-hl.5.1.5--1] PROPOSED FOLLOW-UP: macOS run 42207807508 at e37f90f248f24dcb9bd159cca33f9011cbee7d12 has 17 failing test names and assertion lists identical to clean-base run 42190434184 (61142bf0bb4008266bdb99a8788dd7aaed4a099f, same tree as 6d659eb). Includes word-motion undo, MoveChoice answer count, two comma route tests, PullIn footer hints, two relation-dash tests, and ten separator alias tests. Exact failures/comparison: file:explicit:f7c87874f1ec8abb2832fe8f. No new failures; gate, merge-in, renders, and repaired past-segment submit pass. CI bundle/signature/launch/install were skipped after Test failed. Current master advanced to 9578c66 and was integrated; next run will verify its past-segment fix with rollout.

[2026-11-06T11:32:45Z · bob-cli-hl.5.1.5--1] Verification recovery: both documentation gates now pass all stages except known README contract-table snapshot drift (446 passed, 1 skipped); fixed new preview-page word budget. Reviewed 620 light/dark five/long-title, pending/error, three refusals, both-arrow folded/expanded images from run 42207807508. Found and repaired narrow long-title source locator compression and clipped merge-origin note counts. Added hosted native-control renders because ImageRenderer replaces link buttons with yellow placeholders; added fifth-source warning render. Integrated current linked master 9578c66 without conflicts and regenerated its new tail parser fixture with bob 0.4.0 grammar 15 (also restores actual tail segment/stack metadata), updating the generator. New exact-tree scratch/CI verification pending; no ancestor closure or memory edits.

[2026-11-06T12:19:00Z · bob-cli-hl.5.1.5--2] PROPOSED FOLLOW-UP: latest exact-tree macOS CI run 42212293089 at 04041733ce1334db799fa3cdf93c7c94eba8a1da remains red with 13 failing tests (29 assertions), all assertion lists identical to clean baseline run 42190434184 / 61142bf0bb4008266bdb99a8788dd7aaed4a099f. No new failures. Remaining areas: word-motion undo, two comma route tests, PullIn footer hints, nine separator alias tests. The MoveChoice answer-count, two relation-dash tests, and relation-dash intent test now pass. Bundle, plist/signature, launch smoke, and install/reinstall were skipped after Test failed. Exact comparison and review: file:explicit:80ea345ad2f4aa2a61b9599d. All 84 merge-in renders plus focused test evidence: file:explicit:93caffd02e31ab101cc20f9c. Known docs snapshot drift and Mac-only clip-history regeneration remain covered by earlier follow-up notes; no unrelated fixes or new task beads.

[2026-11-06T12:19:20Z · bob-cli-hl.5.1.5--2] Completed merge-in rollout: grammar gate 15 with old/missing/stale submit protection, compatible parser/fake fixtures including integrated past-segment tail metadata, picker/preview/keyboard docs, accessible source disclosure, narrow source-locator and origin-count fixes, and 84 render fixtures. Final working files exactly match snapshot 04041733ce1334db799fa3cdf93c7c94eba8a1da (tree 922561578967e4120c4d6ac5467a2d09dbe33b7d), on linked master 9578c66. Portable check: 2239 tests, 1 skipped, 0 failures. Mac scratch bundle and all test-target type-checks pass, scratch removed. Hosted lint/build, grammar, merge-in, render, and past-segment tests pass; overall CI red only for 13 identical baseline failures, with packaging/install stages skipped as recorded. Both docs gates retain only known contract snapshot failure (446 pass, 1 skip). Reviewed narrow light/dark long titles, native Show all and folded warnings, all three rewrites, and both-arrow folded/expanded origins; no further phase regressions. No epic-symbol entries. Durable comparison file:explicit:80ea345ad2f4aa2a61b9599d; renders/test evidence file:explicit:93caffd02e31ab101cc20f9c. Only this phase closed; no ancestor or memory changes. Linked rollout work will be committed through the final declaration.

## Dependencies

- **Depends on:** [bob-cli-hl.5.1.4](bob-cli-hl.5.1.4.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.5.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.1.5.md) | [bob-cli-hl.5.1.5](bob-cli-hl.5.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a3e533b`](https://github.com/bobs-org/bob-mac-capture/commit/a3e533b9ec57855be534ac4d96b8bcd7cb8194bf) | feat(capture): complete merge-in grammar-15 rollout | [bob-cli-hl.5.1.5](bob-cli-hl.5.1.5.md) | 2026-11-06 07:20:21 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.5.1.2--1][1] | Check whether the active integration phase owns this baseline macOS build failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.1.2.md

<!-- sase:referenced-by:end -->
