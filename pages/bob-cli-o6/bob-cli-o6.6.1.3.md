# Bead: bob-cli-o6.6.1.3 — Complete and inspect the family preview and accessibility matrix

[Bead Pages](../README.md) / [bob-cli-o6.6.1](bob-cli-o6.6.1.md) / bob-cli-o6.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-o6.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.6.md) · **Assignee:** `bob-cli-o6.6.1.3` · **Size:** medium
**Created:** 2026-11-21 08:22:48 EST · **Closed:** 2026-11-21 12:32:50 EST
**Plan:** [202611/title\_block\_final\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/title_block_final_proof.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:1bc72cad5701112893247e79 | attached via sase artifact create --bead |
| related | file:explicit:259cbd73cf16d1b5da1606dc | attached via sase artifact create --bead |
| related | file:explicit:7021dc2b01dac7b9e530753d | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

visual-matrix: compose the existing real card builders into the full eleven-case light/dark by 375px/wide preview matrix, add grayscale and forced-colors species proofs, inspect every image, and fix the owning DOM or CSS. Attach a durable indexed screenshot bundle and inspection record, and rerun the shared Obsidian proof after product changes.

## Notes

[2026-11-21T17:32:38Z · bob-cli-o6.6.1.3] PROPOSED FOLLOW-UP: Title-slot ownership recovery still fails identically after mount/repaint faults (title-slot-insert-failure-recovers, repaint-failure-restores-native, downstream leaf-close-clears-owner). Reran shared obsidian-title-block-e2e on bd8f2d4 under xvfb: 62 pass / same 3 fail as clean-HEAD d8dc11e. Already tracked by the PROPOSED FOLLOW-UP on bob-cli-o6.6.1.2 (report file:explicit:482569fb7e27dee2e605a59e); no new task bead created, no assertions weakened, no product fragments changed by this phase.

[2026-11-21T17:32:50Z · bob-cli-o6.6.1.3] visual-matrix done: new scripts/preview-title-block-matrix.cjs builds all 11 cases with real adopter builders (album/record via property-cards builders, day/period via intentionCardBuildDom, bank via bankSetupBuildEl, broken-album with error report). Matrix 77/77 pass (44 normal light/dark x 375/1280 + 22 grayscale + 11 forced-colors); species contrast min 5.93:1, stripe min 4.71:1; grayscale titles identical; forced-colors CanvasText borders present. Manually reviewed album/broken/bank/today/forced/grayscale/week/legacy/empty/year PNGs, all pass, no DOM/CSS repairs. Evidence: bundle file:explicit:259cbd73cf16d1b5da1606dc, inspection file:explicit:1bc72cad5701112893247e79, manifest file:explicit:7021dc2b01dac7b9e530753d. Offline wrapper 7/7. Shared Obsidian rerun 62 pass / same 3 known recovery failures as clean HEAD (tracked on bob-cli-o6.6.1.2); no new failures, no product changes. New matrix script left untracked in linked bob-plugins checkout for the land/final-gates phases to integrate.

## Dependencies

- **Depends on:** [bob-cli-o6.6.1.2](bob-cli-o6.6.1.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-o6.6.1.4](bob-cli-o6.6.1.4.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-o6.6.1.5](bob-cli-o6.6.1.5.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.3/README.md) | [bob-cli-o6.6.1.3](bob-cli-o6.6.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9a15d52`](https://github.com/bobs-org/bob-plugins/commit/9a15d529cd9e9fd450fb80dc6d0e301345a9c29c) | feat(previews): add real-builder title-block family matrix (bob-cli-o6.6.1.3) | [bob-cli-o6.6.1.3](bob-cli-o6.6.1.3.md) | 2026-11-21 12:33:38 EST |
