# Bead: bob-cli-q7.6 — End-to-end verification and docs closeout

[Bead Pages](../README.md) / [bob-cli-q7](README.md) / bob-cli-q7.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g6.md) · **Assignee:** `bob-cli-q7.6` · **Size:** small
**Created:** 2026-11-25 15:25:24 EST · **Closed:** 2026-11-26 03:37:48 EST
**Plan:** [202611/caret\_address\_goto\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/caret_address_goto_capture.md)

## Description

closeout: verify every acceptance case against the real vault read-only, confirm plugin deploy and green macOS CI on the landed SHAs, reconcile cross-repo docs, and write the decision record only if approved.

## Notes

[2026-11-26T08:28:57Z · bob-cli-q7.6] Closeout verification: workspace CLI at 1c23bce7 (built by docs-check; grammar 33) passes real-vault read-only cases on athena: @bob^intention-rollovers => bob.md:79 task; @bob^use-list-for-reflections => done/bob_done.md:2165 archived task; @bob^intention-rolovers => missing_block_id with the correct near suggestion; @q7-missing-note^missing => missing_note; @taxes^z-250414-15 => taxes.md:17 notebook_note. Bare-address --dry-run returns T5/exit 2; Fix it @bob^new-id dry-run preserves task text and authored ID. @bob^int completion has eligible Go To payload with 799 rows including archives; /bob^intention returns 4 candidates including intention-rollovers. git status --porcelain on the real vault is identical and empty before and after. Installed bob is older (grammar 31, no block_id.goto); validation used the workspace binary, without replacing the installed CLI or changing versions.

[2026-11-26T08:29:14Z · bob-cli-q7.6] Deployment/CI evidence: bob plugins sync --no-pull --repo <opened bob-plugins checkout> --plugin bob-navigation-hotkeys deployed clean e82bd9328781baae85122e337617c8a2e404216e (contains plugin-refind 1e726f3a); repeat sync reports 0 copied / 3 unchanged / 0 skipped. Targeted goto-task-uri and open-task-jump tests: 41 passed. Original landed Mac card fc0d45515c8d86a33ab8b4ca46452f837eb3c490 run 45718395853 failed only SimilarTasksActionsTests.testOpenKeepsDraft; caret Go To suites passed. Landed browse e6b22ed2709713be4444c2667dea0c1dd8652b2d run 45750284777 failed only three drawer expectation assertions; all three caret Go To suites passed. These historical failures were fixed by 1e85be26 and 4c36dd02. Confirmed green macOS CI at landed descendant 5d50d5a6ddf46b4aa35efefbb83739734b6094f2 containing both q7 commits: https://github.com/bobs-org/bob-mac-capture/actions/runs/45760949969 (lint, build, tests, bundle, signature, launch, install/reinstall all success). Do not describe the two original commit runs as green.

[2026-11-26T08:29:32Z · bob-cli-q7.6] Docs reconciled in bob-cli docs/capture.md and opened bob-mac-capture docs/{capture-panel,protocol,task-pickers}. Added reciprocal destination-card/scoped-browse links, corrected top-level goto wire wording, and made grammar 31 an introduction version rather than a current-version claim. All modified Mac pages remain below 6000 words; edited-tree lint and git diff --check pass. Initial full bob-cli docs-check passed all gates (447 documentation tests, 1 optional-font skip); final edited-tree gates for bob-cli and both linked repos remain to run. No implementation remainder or child epic needed: only verification and closure remain. No memory changed (reviewer declined the decision strand). epic-symbols reports no entries. Final report must include manual Mac/Obsidian checks for Bryan: paste @bob^intention-rollovers and Return, then <C-o> back; @bob. scoped browse; typo to did-you-mean replacement; archived badge; heading landing after inserting lines above it. These GUI checks are explicitly manual and were not run on athena.

[2026-11-26T08:37:48Z · bob-cli-q7.6--1] Final documentation verification passed: monitor nhaqtmnnck25 / tool run 2d6df94a7931ca6ce32b36838d897462 completed exit 0 for bob-cli just docs-check, linked bob-mac-capture just docs-check, and linked bob-plugins npm run docs:check with explicit source paths. Gates include lint, generated drift, strict site build, links, search, tutorial, media determinism, and 447 documentation tests with one optional font dependency skip. Inherited CLI and Mac documentation diffs pass git diff --check; no source or memory changes. Prior notes retain live-vault acceptance with unchanged clean status, 41 plugin navigation tests, clean e82bd932 deployment, and green full macOS CI run 45760949969 at landed descendant 5d50d5a6 containing both q7 Mac phases; original phase runs had unrelated failures subsequently fixed. Installed athena bob lacks scoped browse, so acceptance used the workspace binary. GUI checklist remains manual for Bryan: paste-and-Return and Ctrl-O back, @bob. browse, typo suggestion replacement, archived badge, and heading landing after inserting lines above. No epic-symbol entries remain. Only q7.6 is closed; parent q7 is left to its land agent.

## Dependencies

- **Depends on:** [bob-cli-q7.3](bob-cli-q7.3.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q7.5](bob-cli-q7.5.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q7.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.6.md) | [bob-cli-q7.6](bob-cli-q7.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8ee8d03`](https://github.com/bobs-org/bob-cli/commit/8ee8d03ca7e50f33cdf07f7b1d408a399e4da4bc) | docs(capture): reconcile caret Go To contract and Mac links | [bob-cli-q7.6](bob-cli-q7.6.md) | 2026-11-26 03:38:51 EST |
| bob-mac-capture | [`bob-mac-capture@b7a3b4e`](https://github.com/bobs-org/bob-mac-capture/commit/b7a3b4e001552278d61766ea827c82538a8a362b) | docs(capture): document caret Go To card and scoped browse | [bob-cli-q7.6](bob-cli-q7.6.md) | 2026-11-26 03:39:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.1.1.land][1] | Check q7 closeout phase scope for docs budget and lint | 1 |
| read-by | [agent:bob-cli-q7.6--1][2] | Need the phase scope and design file; review prior verification notes before final closure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.6.md

<!-- sase:referenced-by:end -->
