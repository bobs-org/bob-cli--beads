# Bead: bob-cli-kd.6.1.3 — Month and queue cards with the daily bank chip

[Bead Pages](../README.md) / [bob-cli-kd.6.1](bob-cli-kd.6.1.md) / bob-cli-kd.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.md) · **Assignee:** `bob-cli-kd.6.1.3` · **Size:** medium
**Created:** 2026-11-11 14:27:33 EST · **Closed:** 2026-11-12 06:21:39 EST
**Plan:** [202611/bank\_obsidian.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_obsidian.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:406f620cf619e73fcdb56669 | attached via sase artifact create --bead |
| related | file:explicit:459723958199a494a5792a15 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

bank-ui-cards: render bob-bank month and queue fences and the daily bob-plan chip using the shared data and action services. Follow the bank-ui-cards section.

## Notes

[2026-11-11T21:46:48Z · bob-cli-kd.6.1.3] Implemented synthetic-fixture month and queue cards plus the daily plan chip. Verified plugin build; 167 bank/day-strip/build regression tests passed; docs inventory and manifest validation passed. Synthetic text captures are attached as file:explicit:406f620cf619e73fcdb56669. Deployment and closure remain blocked by the protected uncommitted bob-ledger-tools build from active author bob-cli-k3.5.1.3; the plugin deployment runbook requires waiting for that author, and no force overwrite was attempted. Docs lint still reports eight word-budget failures; the base docs reproduce the same eight.

[2026-11-12T00:28:28Z · bob-cli-kd.6.1.3--3] Rollout attempt 2026-11-11/12: `npx --yes --package=node@22 -- npm test -- scripts/test-obsidian-startup-smoke.cjs` timed out after 1h (monitor 9enbyvbd39z0, exit -9), while the configured full test list was still progressing at test 1867; no assertion failure was reported. The package test script appends the requested filename to its full explicit test list, so this command does not filter to the smoke unit test. The chain stopped before help, isolated smoke, build check, sync, or deployed smoke; neither `/tmp/obsidian-smoke-isolated.json` nor `/tmp/obsidian-smoke-deployed.json` exists. Retrying with a 2h budget.
PROPOSED FOLLOW-UP: Make the rollout documentation targeted startup smoke test command actually run only `scripts/test-obsidian-startup-smoke.cjs`, or document the full-suite cost; `npm test -- <file>` currently runs the full package test list.

[2026-11-12T02:50:50Z · bob-cli-kd.6.1.3--4] Rollout resume 2026-11-12: fetched origin/master and fast-forwarded the opened bob-plugins checkout to d94c6bb; protected deploy commit d532aad and earlier landed build e8a776e are reachable. Clean sync on the landed checkout passed without force (0 copied, 0 skipped, 3 unchanged); after restoring UI changes, dry-run previewed only bob-ledger-tools, and the final non-force sync copied manifest.json, main.js, and styles.css (3 copied, 0 skipped, 0 unchanged; version 1.111.1). Node 22 checks passed: bank/day-strip tests 119/119, direct startup-smoke unit tests 17/17, build:check, docs inventory, manifest validation 10/10, and smoke help. Isolated smoke /tmp/obsidian-smoke-isolated-final.json passed from d94c6bb: 364 ms layout-ready, all four editor cases, 40.3 MiB heap, no exceptions/rejections/crashes. Post-sync deployed-vault smoke /tmp/obsidian-smoke-deployed-final.json passed: 344 ms, 10/10 plugins synced, zero drift or missing plugins, bob-ledger-tools 1.111.1 synced, all four editor cases, no exceptions/rejections/crashes. npm run docs:check exits 1 on docs/reference/plugins/bob-ledger-tools.md:1 at 6221 words versus cap 6000; prior phase verification established the same word-budget baseline with the original plugin documentation restored. Corrected the rollout guide to run the focused smoke test with node --test and the full suite with npm test. Full npm test is pending monitored verification; earlier pre-refactor runs timed out without assertion failures.

[2026-11-12T06:03:33Z · bob-cli-kd.6.1.3--5] Rollout resume 2026-11-12: npx --yes --package=node@22 -- npm test timed out after 3h 0m 5s; monitor mna01jdbzg58, retained log file:monitor-retained-log:mna01jdbzg58, diagnostics file:monitor-diagnostic-manifest:mna01jdbzg58. Build freshness and docs inventory passed, then test:unit emitted through test 1864 (shared report command remains keyed once by the period id) with no reported assertion failure or TAP summary and did not return; test:perf was not reached. Full-suite gate remains unresolved, so this phase stays in progress. Epic-symbol check reports no entries. PROPOSED FOLLOW-UP: Diagnose why the full bob-plugins unit suite does not exit on the clean base and repair the runner or lingering handle so npm test completes.

[2026-11-12T11:21:09Z · bob-cli-kd.6.1.3] PROPOSED FOLLOW-UP: Fix the existing task-wikilink picker runtime test process that never exits — on both landed bank-card commit 564f3c1 and clean parent 9c79123, Node 22 node --test --test-timeout=5000 scripts/test-block-id-prompt-task-wikilink-picker-runtime.cjs passes all 19 assertions and then reports the identical file-level testTimeoutFailure. The full configured unit diagnostic with concurrency=8 and timeout=15000 passed 6215 tests with zero assertion failures and only this timeout. No bank-card files affect that plugin or test. Evidence: file:explicit:459723958199a494a5792a15. This refines the unresolved full-suite follow-up in note #4; no new task created.

[2026-11-12T11:21:23Z · bob-cli-kd.6.1.3] PROPOSED FOLLOW-UP: Corroborate the existing bob-cli-kb mounted-doc link failure — npm run docs:check (calling just docs-check with this primary checkout) passes lint and generated drift but fails strict Zensical at develop/plugins/validation.md:55:22, ../bob-vim-yank-flash.md#verification: page does not exist. The identical failure reproduces in clean parent 9c79123 and landed 564f3c1. Task bob-cli-kk explicitly routes this third warning to bob-cli-kb rather than its own two anchor repairs. Evidence: file:explicit:459723958199a494a5792a15. No new task created.

[2026-11-12T11:21:39Z · bob-cli-kd.6.1.3] Verified earlier implementation landed at bob-plugins 564f3c1; no source rewrite needed. Node 22 focused bank/plan-host/build tests 92/92, adjacent day-strip/period tests 60/60, perf 5/5, generated build checks and docs inventory pass, 10/10 manifests valid. Bounded run of all configured unit files: 6215 passes, zero assertion failures, only the pre-existing picker process timeout reproduced on clean parent 9c79123. Full docs gate passes lint/drift and reproduces the same existing kb-owned missing-page failure on clean parent; both failures recorded as PROPOSED FOLLOW-UP per close instructions. Current deployment verified 10/10 synced, zero drift/missing; bob-ledger-tools 1.111.1 enabled and synced. Earlier note #3 supplies successful isolated/post-sync smoke evidence, and the existing synthetic capture remains attached. epic-symbols reports no entries. Completion evidence: file:explicit:459723958199a494a5792a15. Closed only this phase; no ancestor closed.

## Dependencies

- **Depends on:** [bob-cli-k3.5.1.3](../bob-cli-k3/bob-cli-k3.5.1.3.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-kd.6.1.2](bob-cli-kd.6.1.2.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.6.1.4](bob-cli-kd.6.1.4.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.1.3.md) | [bob-cli-kd.6.1.3](bob-cli-kd.6.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@564f3c1`](https://github.com/bobs-org/bob-plugins/commit/564f3c1087e3bf1f4a03854a15e905e08c253301) | feat(bob-ledger-tools): render bank cards and daily chip | [bob-cli-kd.6.1.3](bob-cli-kd.6.1.3.md) | 2026-11-12 01:47:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.6.1.3--5][1] | Confirm final rollout blocker note and phase status | 2 |
| read-by | [agent:bob-cli-kd.6.1.4][2] | Need closed cards phase notes to see what already landed for marks to build on | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.1.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.4/README.md

<!-- sase:referenced-by:end -->
