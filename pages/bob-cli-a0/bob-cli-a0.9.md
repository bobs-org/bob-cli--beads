# Bead: bob-cli-a0.9 — Concept pages

[Bead Pages](../README.md) / [bob-cli-a0](README.md) / bob-cli-a0.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.md) · **Assignee:** `bob-cli-a0.9` · **Size:** large
**Created:** 2026-10-19 18:55:42 EDT · **Closed:** 2026-10-20 02:06:58 EDT
**Plan:** [202610/bob\_public\_docs\_site.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_public_docs_site.md)

## Description

concepts: write the remaining concept pages from the contracts and decision records, and point the homepage's Bob day strip at them.

## Notes

[2026-10-20T05:46:51Z · bob-cli-a0.9] PROPOSED FOLLOW-UP: Freshness decision context still lists an obsolete review roster — already tracked by bob-cli-5q and bob-cli-3y. During concept-page planning, docs/freshness.md sections 2/4 and src/native/freshness/state.rs Tier confirmed PRE → NEW → PROJECTS → PENDING → NEXT → RECURRING → TICKLER → ROTTEN → POST, with references using ordinary task freshness; decisions:review-walk-is-tiered still lists REFERENCES and omits RECURRING. tests/cli/freshness.rs covers recurring rows and ordinary references. Concept pages will describe the current contract and use the decision for its structural-tier rationale only; no memory edits are part of this phase.

[2026-10-20T06:06:49Z · bob-cli-a0.9] Verification evidence: wrote six concept pages (tasks-and-lanes 717w, today-and-the-pomodoro-ledger 597w, freshness-and-the-review-walk 742w, projects-and-dependencies 616w, reference-library 557w, why-the-vault-syncs-through-git 513w; all within 500-900 target, descriptions <=87 chars). Wired Understand nav, refreshed concepts index (273w) and homepage strip (303w) to concept anchors, added 12 reader: banner links (verified in built HTML for all 12 contract stems), added 6 concept-title search_smoke queries. Gates on final tree: bob-docs lint ok; just docs-check passed (409 passed, 1 skipped); just docs-build (Zensical strict) ok; just docs-build-material ok. Rendered banner links resolve to intended reader pages; lane stateDiagram renders as SVG with no parse-error panel on both builders at 360px/1280px in light/dark with zero overflow and zero page errors (scratch report at target/docs/concept-visual/report.txt). Base revision 928c1955 was clean (lint ok before edits); no baseline failures. No memory edits; no new tests pinning prose.

[2026-10-20T06:06:58Z · bob-cli-a0.9] Implemented six concept pages and reader routing; verified lint ok, docs-check passed (409 passed, 1 skipped), Zensical and Material strict builds ok, 12 contract banner links resolve to intended reader pages, lane diagram renders as SVG with no parse-error panel at 360px/1280px light/dark with zero overflow, six search-smoke queries added; no baseline failures.

## Dependencies

- **Blocks:** [bob-cli-a0.12](bob-cli-a0.12.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.6](bob-cli-a0.6.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.9.md) | [bob-cli-a0.9](bob-cli-a0.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d6795bd`](https://github.com/bobs-org/bob-cli/commit/d6795bdec2fd0ad1defbc16bedf2c9550e2cd578) | feat(docs): complete Bob concept pages and reader routing | [bob-cli-a0.9](bob-cli-a0.9.md) | 2026-10-20 02:08:48 EDT |
