# Bead: bob-cli-pl.1 — Retire the second frontmatter writers on project notes (bob-plugins + vault)

[Bead Pages](../README.md) / [bob-cli-pl](README.md) / bob-cli-pl.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5y.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5y.linker.w1.md) · **Assignee:** `bob-cli-pl.1` · **Size:** medium
**Created:** 2026-11-22 20:56:40 EST
**Plan:** [202611/area\_project\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_cards.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:18af8a410edfdba7f8a5506b | attached via sase artifact create --bead |
| related | file:explicit:5c8a64dd5b630b4d7f26d2e5 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

one-writer: remove the bob-project-tasks count writer and the project-creation processFrontMatter call, sweep the retired count keys out of the vault through bob props, and update projects.base and project.md, retiring status waiting.

## Notes

[2026-11-23T02:01:12Z · bob-cli-pl.1] Blocked by epic launch precondition: bob-cli-pf remains in_progress (audited read on 2026-11-23). The plan requires stopping, recording this note, and changing no files until bob-cli-pf is closed. Workspace tree was clean at 3e480e4a.

[2026-11-23T02:09:18Z · bob-cli-pl.1] Launch precondition rechecked: bob-cli-pf is still in_progress. Earlier phase notes confirm no implementation was attempted; this checkout remains clean. Added an explicit dependency on bob-cli-pf and am staging a prerequisite monitor to resume this phase after it closes. No source, vault, or memory files changed.

[2026-11-24T14:52:00Z · bob-cli-pl.1--1] IMPLEMENTATION: pf resolved done. Both plugin writers removed; focused plugin tests pass 59/59. Landed props still protects task_count/open_task_count, so this phase also removes those two obsolete derived roles and tests guarded removal plus byte-exact undo on project, area, and archived notes. This is needed to run the required sweep independently of pl.2; pl.2 still owns the additive legacy flag/grouping. Landed property-editor key is bare +, so docs and vault use + instead of planned =+.

[2026-11-24T14:54:44Z · bob-cli-pl.1--1] CHECKPOINT: All implementation edits are ready; 59 focused plugin tests plus 9 rerun new tests pass, cargo fmt and both diff checks pass. Full npm test, Rust props suites/build, and docs gate are next under a monitor. Apollo deployment succeeded for bob-project-tasks 1.2.0 and bob-navigation-hotkeys 2.107.1 (no force). Audit is in plugins docs/bob-project-tasks.md; no processFrontMatter call remains, snapshot commands/methods preserved exactly. No live note/Base edits or real vault sweep yet: after build, set BOB_BIN to its debug/bob, prove fixture dry-run/apply/idempotence, sweep ~/bob dry-run then apply with before/after byte verification, edit projects.base/project.md per design (bare +), verify Base rendering, recheck epic-symbols and close only pl.1. Earlier installed-bob trial correctly refused retired keys because its role table predates this patch. No follow-up bead needed; remaining work clearly fits one coder.

[2026-11-24T15:26:19Z · bob-cli-pl.1--2] ACCEPTANCE CHECKPOINT: Fresh monitor build located at /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws16-261124_094256/debug/bob. Rust props 54/54 and CLI props 20/20 passed. Real Bob scratch archived CRLF project: dry-run byte-identical; apply removes exactly two count lines; repeat no-op. Live 106 notes/212 keys snapshotted locally under .git/pl1-acceptance/vault-before (including four conflict copies, no archived counts). Initial live preview was interrupted with exit 143 before completion and made no writes; one 30s Bob timeout prompted raising the cleanup subprocess bound to 120s. Guarded full preview/apply with exact local byte checks is prepared in .git/pl1-acceptance/live-cleanup.py, not yet run. Vault projects.base/project.md edits are done and vault-sync owns their commits; bare + is documented. All three Base views verified in isolated real Obsidian on athena: Active WIP only, Closed done/canceled only, All four fixture statuses, no Tasks columns. Highlights commands/methods byte-identical to plugin HEAD b1413ba9. No processFrontMatter calls remain (only explanatory comments). Apollo sync rechecked both changed plugins up to date; athena and Mac still require bob plugins sync. epic-symbols reports none.

[2026-11-24T15:27:28Z · bob-cli-pl.1--2] PROPOSED FOLLOW-UP: Stabilize existing plugin timing tests under the full npm test load. Original monitor h4h9fsfwsst5 failed event-link-times.cjs:1069 (63.8ms / 25ms), frees-marks.cjs:481 (120ms / 25ms), and task-links-api-performance.cjs:155 typed p95 (14ms / 12ms). All 44 tests in those three files pass on unchanged working source in isolation. A git archive of clean bob-plugins b1413ba9311f90c544be850525aaa433f737ec93 reproduced the two exact unit timing failures under full npm test: event-link 37.5ms and frees 117ms; ToolRun 319d4ebf60eae77cec6532da9a00298d. Its perf suite passes 26/26, typed p95 10.99ms; a separate clean-base isolated run also passes 26/26. Another unchanged clean-base run failed session open 50.9ms / 50ms. These test files and both tested plugins are byte-identical to HEAD. The clean archive also had two missing bob-cli fixture paths caused by its nested location, not product failures; the original full working-tree run passed those checks. Follow-up belongs to the land agent for triage; no task bead created.

[2026-11-24T15:29:47Z · bob-cli-pl.1--2] VERIFICATION DETAIL: Real Obsidian Base screenshot is file:explicit:18af8a410edfdba7f8a5506b (also attached to this phase); all three view assertions and local screenshots are in .git/pl1-acceptance/. Navigation docs briefly exceeded the 6000-word cap when creation instructions were added; shortened equivalent prose to 5998 words without removing behavior. Clean-base performance reproduction is recorded in the phase-only PROPOSED FOLLOW-UP note. Initial dry-run interruption was read-only: all 106 count-note preimages remained byte-identical after exit 143. The full guarded cleanup needs a monitor due to whole-vault ownership discovery per Bob call.

[2026-11-24T15:36:02Z · bob-cli-pl.1--2] GATES PASSED: npm run docs:check (which delegates to just docs-check) completed successfully, including lint, strict site build, published URLs, offline fragments, edit links, search smoke, executable first-day tutorial, and Typst checks; ToolRun ae4a600fc5acf4362c65b53b6b93b917, exit 0. Navigation docs are 5998 words. Generated plugin bundles and documentation inventory are current; both diff checks pass. Only the monitored live cleanup, final byte evidence review, and phase close remain. No remaining source work is planned.

[2026-11-24T16:22:36Z · bob-cli-pl.1--3] LIVE RECOVERY: monitor 2cs8tw51atd0 dry-run passed 106 notes/212 keys; apply removed 210 keys from 105 notes and skipped sase_dyn_agent_fam_e2e.md for lock_busy. All 105 successful transactions are independently proved in vault-sync history to remove exactly the two count lines (.git/pl1-acceptance/live-original-transaction-proof.json). A stale Mac writer then restored the keys through vault-sync: commit 48c5a395a is concrete evidence. Current files match original bytes after excluding count lines except one independent sase.md task edit, which will be preserved. Evidence: file:explicit:5c8a64dd5b630b4d7f26d2e5. Both changed plugins remain up to date on Apollo. The frozen plan explicitly anticipates stale hosts restoring counts until athena/Mac run bob plugins sync. Prepared live-cleanup-retry.py takes separate retry-preimages, temporarily quiesces only Apollo sync between transactions, reruns guarded dry-run/apply/no-op with the fresh binary, verifies exact bytes and zero keys, and restores sync in finally plus a timed fallback. Original preimages/logs retained. No source or memory changes and no new beads. epic-symbols still empty. Phase remains open until the controlled acceptance report passes.

## Dependencies

- **Depends on:** [bob-cli-pf](../bob-cli-pf/README.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.9](bob-cli-pl.9.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.1.md) | [bob-cli-pl.1](bob-cli-pl.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fn--code][1] | Check whether retiring project-note frontmatter writers covers the requirement close Undo guard | 1 |
| read-by | [agent:fx][2] | Research whether the pl epic's dependency on pf is necessary | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.1fn.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
