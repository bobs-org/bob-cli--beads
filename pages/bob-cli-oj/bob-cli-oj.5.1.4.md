# Bead: bob-cli-oj.5.1.4 — Preview matrix, real-Obsidian e2e runs, and final deploy for the group rail

[Bead Pages](../README.md) / [bob-cli-oj.5.1](bob-cli-oj.5.1.md) / bob-cli-oj.5.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.md) · **Assignee:** `bob-cli-oj.5.1.4` · **Size:** medium
**Created:** 2026-11-21 12:21:10 EST · **Closed:** 2026-11-21 14:44:58 EST
**Plan:** [202611/group\_rail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/group_rail.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:003cd62b2c9be7f840066a24 | attached via sase artifact create --bead |
| related | file:explicit:0a9da40ecafc983951e90d99 | attached via sase artifact create --bead |
| related | file:explicit:0c04b6ecc8cc4b01ac582292 | attached via sase artifact create --bead |
| related | file:explicit:103e808bc2d179b827062c8e | attached via sase artifact create --bead |
| related | file:explicit:1ea931c37a15f083506627fd | attached via sase artifact create --bead |
| related | file:explicit:1ec8bb4c28bdb584c4e81e31 | attached via sase artifact create --bead |
| related | file:explicit:39b045d399ea333ad0ffd879 | attached via sase artifact create --bead |
| related | file:explicit:52077039e6cb5d268a927c08 | attached via sase artifact create --bead |
| related | file:explicit:588f6662d1ba1439910b3867 | attached via sase artifact create --bead |
| related | file:explicit:6855882619ca7a9c4a4522f2 | attached via sase artifact create --bead |
| related | file:explicit:6b137795cc0d19303166545e | attached via sase artifact create --bead |
| related | file:explicit:7c7eff8370403a857548d434 | attached via sase artifact create --bead |
| related | file:explicit:7c9838586128262f7e2a9214 | attached via sase artifact create --bead |
| related | file:explicit:c68bf7972b322bafe5b01681 | attached via sase artifact create --bead |
| related | file:explicit:c9c47ca3943264ff6b8082a6 | attached via sase artifact create --bead |
| related | file:explicit:cb0873051c5cd643efb970d7 | attached via sase artifact create --bead |
| related | file:explicit:cbcf170c6f24b4d441fcaef5 | attached via sase artifact create --bead |
| related | file:explicit:cff4d9180b258b4d19a9ed3a | attached via sase artifact create --bead |
| related | file:explicit:d064909379895b2cd6dc5822 | attached via sase artifact create --bead |
| related | file:explicit:e636c222123123259bb87f14 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

rail-proof: add scripts/preview-group-rail.cjs over the real card builders, render the contract's fixtures in light and dark at 375px and wide plus grayscale and forced-colors, inspect every image and fix what looks wrong, run the intention-card, record-card, record-walk, and title-block e2e suites on athena, attach every report, pass the gates, and deploy the final tree.

## Notes

[2026-11-21T19:44:15Z · bob-cli-oj.5.1.4] PROPOSED FOLLOW-UP: Intention Card YAML excursion fails in real Obsidian — obsidian-intention-card-e2e yaml-done-returns (Timed out waiting for "reopened after Done") and yaml-invalid-stays-recoverable (no visible refusal notice) fail identically on the pre-epic base bob-plugins 7b44b29 with the same bob binary (report file:explicit:6b137795cc0d19303166545e) and on the final merged tree da0737b (file:explicit:003cd62b2c9be7f840066a24); the Done control click never returns to the card editor. No bead tracks it (sase bead search found none).

[2026-11-21T19:44:22Z · bob-cli-oj.5.1.4] PROPOSED FOLLOW-UP: record-card e2e render-fold-collapse-and-navigation-are-markdown-neutral races Ledger's fingerprint-driven auto `bob projects sync` — in one run (file:explicit:39b045d399ea333ad0ffd879) the scratch vault got commit "projects: sync lifecycles and catalogs (1 notes)" adding a ## Projects catalog to body.md inside the passive window after the suite edits record type/parent; reruns and base 7b44b29 pass 180/180. Pre-seed the fixture catalog or hold projects auto-sync during the passive window.

[2026-11-21T19:44:28Z · bob-cli-oj.5.1.4] PROPOSED FOLLOW-UP: obsidian-record-walk-e2e startup flake — one run failed before any case with "TypeError: Cannot read properties of null (reading openFile)" in openNote (obsidian-record-walk-e2e.cjs:61, via walker-footer CdpClient.evaluate) because no active leaf existed yet; the same tree passed on rerun (3 of 4 runs passed). Wait for a markdown leaf/layout-ready before the first openFile.

[2026-11-21T19:44:33Z · bob-cli-oj.5.1.4] PROPOSED FOLLOW-UP: Same load-only wall-time flake class already recorded on bob-cli-oj.1, bob-cli-oj.5.1.1, and bob-cli-oj.5.1.3 recurred in the parallel full npm test on fb30f8d+rail-proof: test-ledger-tools-frees-marks.cjs:481 (51 ms vs 25 ms) and test-navigation-dependencies-stage-performance.cjs (cubic growth); both pass in isolation and the merged-tree rerun was 8282/0. Corroboration only; move wall-time asserts to the serial perf lane.

[2026-11-21T19:44:58Z · bob-cli-oj.5.1.4] rail-proof done; bob-plugins Ledger Tools 1.154.0 on merged origin/master da0737b (commit via this turn's finalizer). New scripts/preview-group-rail.cjs renders 15 fixtures with the real builders (intentionCardModelFor/BuildDom navRail, recordWalkFor + recordSheetBuildMounted groupRail, albumHeaderBuildEl walks-by pill) inside Obsidian 1.15.1 with Obsidian's own app.css: light/dark x 375px/760px content + grayscale + real forced-colors = 120 renders, manifest/contrast/index; offline scripts/test-preview-group-rail.cjs registered in test:unit. Every image inspected at full size. Fixed in the group-row CSS block: faint ink 45%->50% pull (quarter aqua tint read 4.47:1, now >=4.95:1 light/5.2:1 dark; all states pass 4.5 text / 3 edge), existing group arms no longer boxed under forced colors (border Canvas), ghost item/chip arrows follow GrayText. Updated obsidian-intention-card-e2e display-legacy-daily from "no rail" to the contract's derived step row (calendar prev/parent/next stated, no chips, Week groups day 6 of 7). Final-tree e2e on athena (xvfb, isolated profiles, real bob): intention-card 80/82 (yaml-done-returns + yaml-invalid-stays-recoverable reproduce on pre-epic base 7b44b29, PROPOSED FOLLOW-UP), record-card 180/180, record-walk passed, title-block 65/65 (its earlier 3 fail-open failures reproduced on 7b44b29 and are fixed upstream by 238fa91). Gates: build:check green; npm test 8282 pass/0 fail on merged tree; docs:check fails only on base budgets (nav-hotkeys reference 6247/6000 per bob-cli-oj.5.1.1 note, vault-format 6037/6000 = bob-cli-oc, plugin-apis warning = bob-cli-ob). bob plugins sync deployed Ledger Tools 1.154.0 (list --no-pull: synced; main.js/manifest.json/styles.css hashes match); refused block-id-prompt/task-status-cycler held by bob-cli_13 unlanded 726f9a5 (bob-cli-on.4 running), not forced. ARTIFACTS (final): preview archive file:explicit:1ea931c37a15f083506627fd, inspection note file:explicit:6855882619ca7a9c4a4522f2, e2e intention-card file:explicit:003cd62b2c9be7f840066a24, record-card file:explicit:0c04b6ecc8cc4b01ac582292, record-walk file:explicit:cff4d9180b258b4d19a9ed3a, title-block file:explicit:cb0873051c5cd643efb970d7, e2e screenshots file:explicit:0a9da40ecafc983951e90d99; contrast table file:explicit:1ec8bb4c28bdb584c4e81e31; base 7b44b29 reports: intention-card file:explicit:6b137795cc0d19303166545e, title-block file:explicit:c68bf7972b322bafe5b01681, record-card file:explicit:52077039e6cb5d268a927c08; pre-merge archive file:explicit:d064909379895b2cd6dc5822. 4 PROPOSED FOLLOW-UPs on this bead.

## Dependencies

- **Depends on:** [bob-cli-oj.5.1.2](bob-cli-oj.5.1.2.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-oj.5.1.3](bob-cli-oj.5.1.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.4/README.md) | [bob-cli-oj.5.1.4](bob-cli-oj.5.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@cb70f82`](https://github.com/bobs-org/bob-plugins/commit/cb70f8291aeffa9d8724ea08b51a30ab07671381) | feat(ledger-tools): prove the group rail with a real-builder preview matrix and fix what it found | [bob-cli-oj.5.1.4](bob-cli-oj.5.1.4.md) | 2026-11-21 14:54:59 EST |
