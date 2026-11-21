# Bead: bob-cli-oj.1 — Group-link grammar, one resolver, and the \[N / \]N commands

[Bead Pages](../README.md) / [bob-cli-oj](README.md) / bob-cli-oj.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.1` · **Size:** medium
**Created:** 2026-11-21 07:41:35 EST · **Closed:** 2026-11-21 09:46:30 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

## Previously Closed

> ↺ Closed 2026-11-21T13:12:36Z · done
>
> (none)
>
> Reopened 2026-11-21T13:19:51Z by `sase bead open`

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:f0588487197e47234e4910fc | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

nav-grammar: in bob-navigation-hotkeys, tighten the `[n`/`]n` matcher so doubled arrows never step, recognize `«`/`»` (typed `<<`/`>>`) group links on link-only nav lines, build the one resolver (authored, then the Ledger Tools provider), add the group commands with the creation guard and repeat guard, route `[{`/`]}` on family `n`, publish `walkMode.links` v7, and map `[N`/`]N` in the vault vimrc.

## Notes

[2026-11-21T13:12:08Z · bob-cli-oj.1] Vault scan before matcher change: 0 live-vault notes use «/»/<<</>> link labels (only the research source doc holds plan-example « Part 2 / Part 4 » labels); nothing regresses.

[2026-11-21T13:12:15Z · bob-cli-oj.1] PROPOSED FOLLOW-UP: just docs-check lint fails on docs/reference/vault-format.md (6016 words, cap 6000) on the clean base tree; untouched by this phase.

[2026-11-21T13:12:19Z · bob-cli-oj.1] PROPOSED FOLLOW-UP: bob plugins sync refuses bob-ledger-tools (foreign uncommitted build from workspace bob-cli_11); nav-hotkeys 2.96.0 deployed, ledger left untouched per no -F rule.

[2026-11-21T13:12:23Z · bob-cli-oj.1] PROPOSED FOLLOW-UP: skipped memory change per decision memory_decision_group_stops=no (decisions-web record that group stops are derived on Bob notes and authored only on nav lines).

[2026-11-21T13:12:36Z · bob-cli-oj.1] nav-grammar done: doubled-arrow matcher, link-only nav-line group links with conflict/dedup, one resolver (authored then api.navGroups) with legacy step fill-in, openGroupLink with creation guard and repeat guard, [{/]} on family n, walkMode.links v7, [N/]N vimrc maps. Verified: npm run build, build:check, docs:gen, inventory:check green; 75 nav tests + plugin-build + walker-footer (141 total) pass; bob-navigation-hotkeys.md 5983 words within budget; manifest 2.96.0 committed (merge 726f9a5) and synced to vault (vault shows 2.96.0). Pre-existing docs-check failure on vault-format.md and foreign ledger-tools sync refusal recorded as follow-ups.

[2026-11-21T13:17:22Z · bob-cli-oj.1] CLOSED-BEAD LAUNCH: agent bob-cli-oj.1 launched against this closed bead; status left closed.
Launch submitted 2026-11-21T13:16:31.634870Z; run 20261121081632.
Prior close: 2026-11-21T13:12:36Z · done.

[2026-11-21T13:19:55Z · bob-cli-oj.1] Recovery: prior run closed the phase before its finalizer refused local-only commit 726f9a5c653164a6219b7bdd6eef5a9f2715b55f in workspace 13. Fetched origin/master lacks nav-grammar. Recovering the existing implementation instead of reimplementing it.

[2026-11-21T13:34:02Z · bob-cli-oj.1] Recovery implementation restored in the linked bob-plugins checkout: strict doubled-arrow grammar, link-only authored group stops, shared authored/provider resolver, guarded group commands and step fallback, walkMode v7, repeat plans, jump history, docs and regression tests. The prior local-only commit 726f9a5 is absent from both its old checkout and origin; previous finalizer error is recorded in chat gh_bobs_org__bob_cli-tmp_261121_074352-workflow_tmp_261121_074352_main_ERROR-261121_074357. Vault mappings independently verified already landed as beba6bb7a in bbugyi200/bob (no vault edits needed). Initial focused suite: 105/106 pass; obsolete no-uppercase expectation updated afterward, full rebuild/tests pending. Current docs:check now reports only pre-existing vault-format.md 6016/6000 error (bob-cli-oc); plugin-apis.md 8131/8000 is a pre-existing warning. New navigation docs pass budget. Navigation deployment is still protected by the old clean 726f9a5 build (2.96.0); do not force it without required approval. Current restored source version 2.96.1.

[2026-11-21T13:40:37Z · bob-cli-oj.1--1] PROPOSED FOLLOW-UP: Two unchanged Ledger Tools timing tests flaked in monitor mm8qgy3tenjs — test-ledger-tools-event-link-times.cjs:1095 took 28.5 ms and test-ledger-tools-frees-marks.cjs:509 took 26 ms against 25 ms budgets. Both files and plugins/bob-ledger-tools are byte-identical to clean base 1a95b29 (git diff --exit-code clean); both test files pass together on an unchanged-tree rerun (40 tests). All other full-suite tests passed: 8080 pass, 2 timing failures, 4 skipped; the separate performance lane passed 11/11. Consider moving these wall-time assertions to the serial performance lane.

[2026-11-21T13:44:04Z · bob-cli-oj.1--1] Verification complete for restored navigation 2.96.1: rebuilt after fetching and fast-forwarding bob-plugins to 6debb63; 204/204 tests pass across group-links, period-links, bracket-repeat, bracket-mode-indicator, plugin-build, walker-footer, jump-history, and Ledger nav-groups. Added createEligible to the v7 result and explicit v2-shape/pre-adoption tests. docs:gen and inventory:check pass; git diff --check passes. docs:check remains blocked only by untouched vault-format.md 6016/6000 (bob-cli-oc), with plugin-apis.md 8165/8000 warning after upstream changes. No epic-symbol entries remain. Scoped bob plugins sync refuses the abandoned clean navigation 2.96.0 build at lost 726f9a5. Fetched again: no incoming navigation commits and old commit still absent. Prior recovery agent is DONE; staging a human gate to replace only this protected navigation build with the verified 2.96.1 source, then verify sync and close this phase.

[2026-11-21T14:32:00Z · bob-cli-oj.1] Recovery in this run found the repository clean at 3860513 with the prior navigation work absent. Recovered all 22 source/test/docs files from the earlier provider edit logs, rebuilt, and confirmed exact approval-pinned SHA256s: main.js b005cfda5996caa36225930bfe7f67bef0fc7fb5d7e62393cc53a17eb6453da8; manifest.json ed94cd481e4bf6297bb3ddf7873a4a35c91835a643e12898fde35c032805f37b; styles.css cbb720334979ed5f8ea15e316d508d61ace90fdd14e2631f4d3e3fae3d0af027. Focused 204 tests pass, build/docs inventory/diff checks pass, vimrc maps confirmed in beba6bb7a. Docs lint retains only the already-recorded vault-format.md failure (bob-cli-oc) and plugin-apis warning. No epic symbols. Existing gate custom-231911ba-9d6a-4c7f-83d1-5911bcf25361 explicitly records Bryan accepted replace via TUI; its original deployed 726f9a5 stamp is unchanged. The remaining step is host commit before resuming this existing approval; no new human approval is needed.

[2026-11-21T14:39:23Z · bob-cli-oj.1--1] Deployment monitor evrv7xeqrjtk failed because finalizer commit 51cf930da624ffaa5f0c950464ad55db1556e77a contained only package.json; all other 21 recovered files remained dirty. Verified all 22 files byte-for-byte against audited durable snapshot file:explicit:f0588487197e47234e4910fc, plus all three approval-pinned managed-file hashes. The inherited baseline was excluding the identical recovered source as pre-existing dirt. Explicitly staged the 21 remaining verified files for host finalization without changing content or runtime baseline metadata. Refreshed final context now lists all 21 under bob-plugins repo-739fb42d644b with no protected paths, so the next commit declaration covers the implementation. No incoming navigation commits after fetch; only this recovery agent is live; no epic symbols. Existing TUI replace approval remains accepted_failed, not revoked; retry will retain its exact source and deployed-build guards.

[2026-11-21T14:46:30Z · bob-cli-oj.1--2] Verified final recovery and deployment: bob-plugins HEAD and freshly fetched origin/master both equal 983076e6882c744f36e6fa513e9c2853bd160c36 (ahead/behind 0/0), with a clean index/worktree and all 22 recovered source/test/docs/package files committed across 51cf930 and 983076e; the latter contains the 21 previously omitted files. Approved gate custom-231911ba-9d6a-4c7f-83d1-5911bcf25361 completed successfully in monitor fsfj8byf6sta (ToolRun 4158dc05f830f5a7d550167c10e168fe; file:monitor-retained-log:fsfj8byf6sta). Fresh bob plugins list --no-pull reports bob-navigation-hotkeys version 2.96.1, sync=synced, deployment.status=clean, source_head=983076e6882c744f36e6fa513e9c2853bd160c36. Source and deployed SHA256s match the approved main.js b005cfda5996caa36225930bfe7f67bef0fc7fb5d7e62393cc53a17eb6453da8, manifest.json ed94cd481e4bf6297bb3ddf7873a4a35c91835a643e12898fde35c032805f37b, styles.css cbb720334979ed5f8ea15e316d508d61ace90fdd14e2631f4d3e3fae3d0af027. No code changed this turn; prior 204/204 focused tests and build/docs inventory/diff checks remain valid. Previously documented vault-format.md lint baseline, plugin-apis warning, and two unchanged Ledger timing flakes remain recorded above. Vault [N/]N mappings were already verified in beba6bb7a. No duplicate phase worker is running. sase bead epic-symbols bob-cli-oj.1 reports no entries. Closed only this phase; parent bob-cli-oj remains in_progress.

## Dependencies

- **Blocks:** [bob-cli-oj.5](bob-cli-oj.5.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.6](bob-cli-oj.6.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.1.md) | [bob-cli-oj.1](bob-cli-oj.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@51cf930`](https://github.com/bobs-org/bob-plugins/commit/51cf930da624ffaa5f0c950464ad55db1556e77a) | feat(navigation): restore group-link commands and guarded repeats | [bob-cli-oj.1](bob-cli-oj.1.md) | 2026-11-21 09:33:34 EST |
| bob-plugins | [`bob-plugins@983076e`](https://github.com/bobs-org/bob-plugins/commit/983076e6882c744f36e6fa513e9c2853bd160c36) | feat(navigation): land group-link resolver and guarded group jumps | [bob-cli-oj.1](bob-cli-oj.1.md) | 2026-11-21 09:42:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.1--1][1] | Need the phase scope and design file and recorded remaining deployment work | 1 |
| read-by | [agent:bob-cli-oj.5.1.1][2] | Check recorded load-sensitive timing failures to cite for a perf flake | 1 |
| read-by | [agent:bob-cli-oj.6][3] | Need sibling phase statuses so I do not redo landed work or collide with group-rail | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md

<!-- sase:referenced-by:end -->
