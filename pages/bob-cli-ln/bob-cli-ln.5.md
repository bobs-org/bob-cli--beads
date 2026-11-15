# Bead: bob-cli-ln.5 — bob-ledger-tools Areas card shell

[Bead Pages](../README.md) / [bob-cli-ln](README.md) / bob-cli-ln.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e2.md) · **Assignee:** `bob-cli-ln.5` · **Size:** medium
**Created:** 2026-11-14 16:33:04 EST · **Closed:** 2026-11-15 06:07:07 EST
**Plan:** [202611/areas\_catalog.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/areas_catalog.md)

## Description

areas-card: in bob-plugins, add the display-only `[!areas]` card - report service, Reading and Live Preview painting, family chrome, hue dots, health line with sync and retry, and the root card's unplaced-areas notice - then deploy.

## Notes

[2026-11-15T03:51:41Z · bob-cli-ln.5--1] PROPOSED FOLLOW-UP: Clean-base docs-check still fails because docs/reference/json-outputs.md is 6002/6000 words; this independent reference-page cap issue was already recorded in bob-cli-lj.5 note #3 and needs a docs budget trim.

[2026-11-15T11:00:49Z · bob-cli-ln.5] PROPOSED FOLLOW-UP: Clean-base plugin docs gate fails on generated glossary drift — BOB_CLI_DIR pointing to bob-cli 49231b37 and unchanged bob-plugins 6615a3f, npm run docs:check exits 1 at generated drift: docs/reference/glossary.md is out of date; run the docs generator in the landing workflow. This precedes all changes in this verification run.

[2026-11-15T11:03:29Z · bob-cli-ln.5] PROPOSED FOLLOW-UP: Unchanged bob-plugins 6615a3f full npm test has six unrelated failures — 6700/6709 unit tests pass (3 skipped), five timing budgets fail in task-link-marks-live, task-link-marks, off-clock-link-chips, off-clock-link-chips-e2e, and relation-index startup storm, plus the MN click relation-chips cursor/focus timing test. test:perf passes all 5. Baseline log: /tmp/bob-cli-ln5-plugin-tests.log; collected before editing source, tests, or generated main.js. New Areas tests all passed on that baseline.

[2026-11-15T11:03:50Z · bob-cli-ln.5] Verification: landed shell found in bob-plugins commit 6615a3f (v1.117.0). npm run validate passed all 11 plugins. Real Obsidian smoke command npm run smoke:obsidian -- --deployed-vault /home/bryan/bob --report /tmp/bob-cli-ln5-obsidian-smoke.json exited 2 unrun because /snap/bin/obsidian is unavailable on apollo; no Electron rollout pass is claimed. Found and reproduced initial failure retry loop (4 list attempts with no new events, another pending); correcting it and restoring the required layers icon in the replacement header.

[2026-11-15T11:04:20Z · bob-cli-ln.5] Correction to the preceding full-suite follow-up: exact baseline failures were event-link-times:1069, frees-marks:481, keep-moving-marks-surface:486, off-clock-link-chips:355 (four timing budgets), note-ready:1154 (expected 2 startup scans, now 3), and relation-chips:1131 (MN-click cursor/focus timing). The startup scan assertion belongs to this phase: the new Areas relevance seed intentionally adds one linear scan. Updating that assertion as part of this work; only the other five failures remain proposed follow-up candidates. The earlier guessed test filenames were incorrect; the baseline log has the exact evidence.

[2026-11-15T11:06:32Z · bob-cli-ln.5] Implementation verified: reused landed bob-plugins 6615a3f/v1.117.0; fixed failed-report polling and concurrent-wait retry behavior using attempted generations, restored the visible layers header icon, and updated the startup scan assertion for Areas relevance. npm run build regenerated only ledger-tools; all 51 focused Areas + note-ready tests pass (10 Areas tests, including three new retry regressions); docs inventory passes. npm test was run on the unchanged landed tree (6700 passed, 6 failed, 3 skipped; all 5 test:perf passed); one of those six was the startup assertion now fixed and verified, with the other five recorded for land-agent triage. Deployment succeeded without -F using the documented clean-sync proving-commit recovery, then restoring and syncing the fixes (2 copied, 1 unchanged). Post-sync real Obsidian smoke remains unrun (exit 2, missing Electron binary), not a pass. No memory edits.

[2026-11-15T11:07:07Z · bob-cli-ln.5] Verified landed Areas shell in bob-plugins 6615a3f; completed bounded failed-refresh retries and visible layers icon, regenerated main.js, and corrected Areas startup-scan coverage. All 51 focused tests pass; full clean-base npm test failures and docs drift are recorded as proposed follow-ups, with the in-scope startup assertion fixed. Deployed without force using proving-commit recovery; bob plugins list confirms v1.117.0 enabled and synced. No epic-symbol entries remain. Real Obsidian smoke is explicitly unrun on apollo because Electron is absent. Only this phase is closed.

## Dependencies

- **Depends on:** [bob-cli-ln.3](bob-cli-ln.3.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-ln.6](bob-cli-ln.6.md) ✓ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ln.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.5/README.md) | [bob-cli-ln.5](bob-cli-ln.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5023787`](https://github.com/bobs-org/bob-plugins/commit/5023787e4064941477fdf0d7cc78f8fbd5db8a48) | fix(areas): bound failed refresh retries and restore card icon | [bob-cli-ln.5](bob-cli-ln.5.md) | 2026-11-15 06:08:39 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ln.5][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-ln.5--2][1] | Need the phase scope, epic decisions, design file, and prior notes before closing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ln.5.md

<!-- sase:referenced-by:end -->
