# Bead: bob-cli-kj.2 — Mounted reference pages back under the word cap

[Bead Pages](../README.md) / [bob-cli-kj](README.md) / bob-cli-kj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.2` · **Size:** medium
**Created:** 2026-11-11 17:20:03 EST · **Closed:** 2026-11-11 18:19:52 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

## Description

docs-trims: trim the four bob-mac-capture pages and one bob-plugins page that fail the 6000-word reference budget, keeping contract facts, and verify with each repo's docs gate plus bob-cli just docs-check (beads bob-cli-h9, bob-cli-jz).

## Notes

[2026-11-11T22:57:28Z · bob-cli-kj.2] Docs verification: all 5 pages trimmed to <=5800 words (protocol 6294->5787, capture-panel 6265->5785, capture-previews 6244->~5791, keyboard 6083->5644, nav-hotkeys 6200->5771; counts via bob_docs.markdown.count_words). bob-cli just docs-check: lint ok, generated drift ok. Same in mac-capture and plugins gates. Strict Zensical build still fails on 3 pre-existing link warnings in files untouched by this phase (validation.md->bob-vim-yank-flash.md#verification, keep-moving-marks.md->task-dependencies.md anchor, vault-git-sync.md->gcal.md#events); no headings added/removed, no links added except image-zoom.md, panel#inline-completion, panel#live-preview-and-clipboard-semantics, previews#close-card, protocol#timeouts-and-guards, all verified to exist.

[2026-11-11T23:18:55Z · bob-cli-kj.2] CI observation (macOS run 43115678317, exact SHA 2007294): Lint Swift formatting green, Build green (ka 4a69ed2 break already fixed on master). Test red from pre-existing causes only: the jx trio PASSED this run; failures were testEditBeforeTheReplyDropsTheTip (tracked intermittent) plus testNotebookCreateSectionUsesDottedUnderlineAndExistingClearsIt, testAcceptingDrawerCandidateInsertsSlugAndLandsCaret, testNotebookNewSectionUsesDottedPurpleUnderlineAndRepaintClearsIt, plus the 15-minute watchdog kill. Parent-commit run 43112612175 (clean base) failed 6 tests including 3 of the same 4 plus 2 more alias-timing flakes — reproduces on base, docs-only change cannot affect Swift tests. Bundle/Launch/Install skipped behind red Test as usual.

[2026-11-11T23:19:02Z · bob-cli-kj.2] PROPOSED FOLLOW-UP: strict Zensical build (just docs-check build step) still fails on 3 link warnings in files untouched by this phase: develop/plugins/validation.md:48 links ../bob-vim-yank-flash.md#verification (page missing), keep-moving-marks.md:274 links task-dependencies.md#1217-lp--leaf-vectors (anchor missing), vault-git-sync.md:271 links gcal.md#events (anchor missing). Owned elsewhere (likely active k3/ka epics); cite, do not adopt.

[2026-11-11T23:19:52Z · bob-cli-kj.2] docs-trims done and verified. Final counts (count_words): protocol 5787, capture-panel 5785, capture-previews 5791, keyboard 5644 (all were 6000+ over budget), nav-hotkeys 5771 at land (later work trimmed further to 5606). Landed mac-capture 2007294 and bob-plugins cb32d8d; both commits intact ancestors of current master, no headings added/removed, all added links verified. bob-cli/mac-capture/plugins docs gates: lint ok + generated drift ok in all three. Strict-build 3 link warnings are pre-existing in untouched files (recorded as PROPOSED FOLLOW-UP). macOS CI run 43115678317 on exact SHA: Lint+Build green, Test red only from pre-existing causes (jx trio passed this run; tracked intermittent + flakes reproduce identically on parent-commit run 43112612175); Bundle/Launch/Install skipped behind red Test as usual.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.2.md) | [bob-cli-kj.2](bob-cli-kj.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kj.2][1] | Need phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.2.md

<!-- sase:referenced-by:end -->
