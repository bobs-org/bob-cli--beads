# Bead: bob-cli-ld.9.1.2 — Projects catalog card in Reading view and Live Preview

[Bead Pages](../README.md) / [bob-cli-ld.9.1](bob-cli-ld.9.1.md) / bob-cli-ld.9.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ld.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ld.9.md) · **Assignee:** `bob-cli-ld.9.1.2` · **Size:** medium
**Created:** 2026-11-13 15:29:28 EST · **Closed:** 2026-11-13 16:30:09 EST
**Plan:** [202611/projects\_catalog\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/projects_catalog_card.md)

## Description

projects-card: render the hued projects card, live chips, per-pane folds, nested children, recovery actions, and responsive layout with focused UI tests.

## Notes

[2026-11-13T21:29:28Z · bob-cli-ld.9.1.2] PROPOSED FOLLOW-UP: full bob-plugins npm test flakes two 25ms wall-clock budget tests under 300-file concurrency (keep-moving-marks-surface + off-clock-link-chips 200-link/50-target builds, e.g. 654ms vs 25ms); both pass alone and paired and the same tree passed test:unit green once. Related: bob-cli-ju, bob-cli-io, bob-cli-gd, bob-cli-g8.

[2026-11-13T21:29:39Z · bob-cli-ld.9.1.2] PROPOSED FOLLOW-UP: bob-plugins npm run docs:check fails lint word budgets on 3 reference pages (json-outputs 6025, plugins/bob-ledger-tools 6115, plugins/bob-navigation-hotkeys 6019 vs 6000 cap); the ledger-tools page was already over before this phase (my required description sentence adds ~22 words). Related: bob-cli-jz, bob-cli-il.

[2026-11-13T21:29:48Z · bob-cli-ld.9.1.2] PROPOSED FOLLOW-UP: bob-cli just check on the untouched tree fails native::gcal sync_args_read_last_n_days_aliases_and_default_to_none deterministically (tracked by bob-cli-l2) plus 2 capture complete_themes tests that pass in isolation (possible bob-cli-g8 flake); the run also exceeds 9min so just check never completes in one turn here.

[2026-11-13T21:30:09Z · bob-cli-ld.9.1.2] Projects catalog card done: 241ac model (states/markers/tally/reasons/sort/folds/copy/scan), 241ad DOM (keyed paint, Closed peek, nested children, anchors, H1 tooltips), 241ae lifecycle (Reading postprocessor + Live Preview ViewPlugin, per-pane folds, clipboard copy), wired fragments/310/170/exports/styles/test-list; manifest 1.115.0 with docs inventory regen. Verified: new test-ledger-tools-projects-catalog.cjs 22/22 pass; full test:unit 6568 pass 0 fail; npm run validate ok; bob plugins sync deployed 1.115.0 to vault. Pre-existing/environmental failures recorded as 3 PROPOSED FOLLOW-UP notes (timing-budget flakes, docs word budgets, untouched-tree just-check failures); epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-ld.9.1.1](bob-cli-ld.9.1.1.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.9.1.3](bob-cli-ld.9.1.3.md) ◐ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.9.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.9.1.2/README.md) | [bob-cli-ld.9.1.2](bob-cli-ld.9.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@274f1db`](https://github.com/bobs-org/bob-plugins/commit/274f1dbf0adda86cbb6d52d39947edfc9dbcc2f5) | feat(bob-ledger-tools): render projects catalog card in Reading and Live Preview \[bob-cli-ld.9.1.2\] | [bob-cli-ld.9.1.2](bob-cli-ld.9.1.2.md) | 2026-11-13 16:32:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ld.9.1.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.9.1.2/README.md

<!-- sase:referenced-by:end -->
