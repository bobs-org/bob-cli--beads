# Bead: bob-cli-ln.6 — Areas card folds, chips, tooltips, and add-summary

[Bead Pages](../README.md) / [bob-cli-ln](README.md) / bob-cli-ln.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e2.md) · **Assignee:** `bob-cli-ln.6` · **Size:** medium
**Created:** 2026-11-14 16:33:04 EST · **Closed:** 2026-11-15 06:36:07 EST
**Plan:** [202611/areas\_catalog.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/areas_catalog.md)

## Description

areas-card-chips: add branch folds with per-pane memory, fold-aware project and Today chips, row tooltips, the hover-only add-summary affordance, and narrow-width polish, then deploy.

## Notes

[2026-11-15T11:35:04Z · bob-cli-ln.6] PROPOSED FOLLOW-UP: CI=true Chromium hard-fail in scripts/test-command-mode-sheet-sequence-dom.cjs — env requires Chromium on PATH or CHROMIUM_PATH; reproduces on clean HEAD; already noted on closed bob-cli-lj.2

[2026-11-15T11:35:18Z · bob-cli-ln.6] PROPOSED FOLLOW-UP: Full npm test 25ms flakes under parallel load (event-link-times, frees-marks, keep-moving-marks-surface, off-clock-link-chips, navigation-dependencies-stage ranker 16.12 vs 16ms) — all pass in isolation; cite bob-cli-km, bob-cli-ju, bob-cli-io; keep-moving-marks-surface 2.3s under full suite has no dedicated bead

[2026-11-15T11:35:31Z · bob-cli-ln.6] PROPOSED FOLLOW-UP: docs:check glossary.md drift on clean bob-plugins HEAD (out of date: docs/reference/glossary.md in cached bob-cli clone) — pre-existing, not caused by this phase; later areas-memory owns glossary:area-note

[2026-11-15T11:36:07Z · bob-cli-ln.6] Areas card folds/chips/tooltips/add-summary/narrow CSS landed in bob-ledger-tools 1.118.0; fragments 268/386/285 lines; 9/9 areas catalog tests pass; npm test 6709 pass / 6 fail (Chromium PATH env + parallel 25ms flakes that pass isolated; cite bob-cli-lj.2, bob-cli-km, bob-cli-ju, bob-cli-io); docs lint ok after word trim; docs:check glossary drift reproduces on clean HEAD; epic-symbols none; deployed with bob plugins sync --no-pull -p bob-ledger-tools

## Dependencies

- **Depends on:** [bob-cli-ln.4](bob-cli-ln.4.md) ✓ · ⧖ 2026-11-14
- **Depends on:** [bob-cli-ln.5](bob-cli-ln.5.md) ✓ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ln.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.6/README.md) | [bob-cli-ln.6](bob-cli-ln.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3a41a3e`](https://github.com/bobs-org/bob-plugins/commit/3a41a3e901edac12252458d074e2655225e5b190) | feat(areas): add Areas card folds, chips, tooltips, and add-summary | [bob-cli-ln.6](bob-cli-ln.6.md) | 2026-11-15 06:37:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ln.6][1] | Need remaining notes, earlier-agent work, and full phase details including notes | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.6/README.md

<!-- sase:referenced-by:end -->
