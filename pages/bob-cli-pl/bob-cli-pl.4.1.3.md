# Bead: bob-cli-pl.4.1.3 — Real-Obsidian acceptance, screenshots, and card documentation

[Bead Pages](../README.md) / [bob-cli-pl.4.1](bob-cli-pl.4.1.md) / bob-cli-pl.4.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.4--1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.4.md) · **Assignee:** `bob-cli-pl.4.1.3` · **Size:** medium
**Created:** 2026-11-24 09:51:09 EST · **Closed:** 2026-11-24 14:04:44 EST
**Plan:** [202611/local\_home\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/local_home_cards.md)

## Description

acceptance: add the disposable-vault home-card e2e and offline wrapper, run its real Obsidian matrix and inspect screenshots, fix phase regressions, document the cards, and complete plugin build, test, docs, and deployment checks.

## Notes

[2026-11-24T17:38:49Z · bob-cli-pl.4.1.3--2] PROPOSED FOLLOW-UP: Check Live Preview Task Card access and editor refresh for project-root tasks — Reproduced on clean bob-plugins base b5f2f6c1b62278b51872298ff99b48e175a02a5c. In the isolated Obsidian Live Preview run, the registered Task Card command opened no card for either an untyped synthetic #task #prj row or the root_plan.md ^prj row; Ctrl+Enter did persist the close and the home card reached DONE, but the immediate active editor getValue() still showed the task open. Investigate the existing nav/task-status Live Preview path separately; the no-card control shows the command failure without a home-card surface, and the ^prj row remains editable and closable. No existing bead specifically tracks this; bob-cli-kg is limited to picker/Task Card display text.

[2026-11-24T18:39:44Z · bob-cli-pl.4.1.3--3] PROPOSED FOLLOW-UP: Fix the existing ledger-tools cache-update regressions — Reproduced on clean bob-plugins HEAD 21bbd30cc7305a8952adfc0280063fd5d66a24f4 after restoring the phase-only acceptance scripts. `scripts/test-ledger-tools-freshness-review-model.cjs` fails “same-array cache updates and Today changes rebuild the memo” at line 435 (actual 2, expected 1); `scripts/test-ledger-tools-note-ready.cjs` fails “a task edit rebuilds through the cache-update handler” at line 1026 (actual 2, expected 3). These are outside this phase’s changed files. No matching task bead was found. Two performance assertions that failed in the loaded full-suite run passed when rerun individually on the same clean HEAD.

[2026-11-24T19:04:44Z · bob-cli-pl.4.1.3--5] Verification: npm run test:perf passed (26/26); npm run docs:check passed (447 passed, 1 skipped; one existing docs word-budget warning); npm run validate passed, including generated plugin build checks (12/12 manifests valid). bob plugins sync completed with 0 copied, 0 skipped, and 34 unchanged. epic-symbols reported no entries. The full unit suite reported 9,258 passed, 5 skipped, and two performance-threshold failures under suite load; those assertions passed in isolated reruns on clean HEAD. The two clean-base cache-update failures are recorded above on this phase bead.

## Dependencies

- **Depends on:** [bob-cli-pl.4.1.2](bob-cli-pl.4.1.2.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.4.1.3.md) | [bob-cli-pl.4.1.3](bob-cli-pl.4.1.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@21bbd30`](https://github.com/bobs-org/bob-plugins/commit/21bbd30cc7305a8952adfc0280063fd5d66a24f4) | test(cards): add local home card acceptance coverage | [bob-cli-pl.4.1.3](bob-cli-pl.4.1.3.md) | 2026-11-24 11:36:30 EST |
| bob-plugins | [`bob-plugins@71cf808`](https://github.com/bobs-org/bob-plugins/commit/71cf808a2cdede5324072f6c3a81a08ee1c4f4d3) | test: correct home-card acceptance assertions | [bob-cli-pl.4.1.3](bob-cli-pl.4.1.3.md) | 2026-11-24 13:42:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.4.1.3--3][1] | Review the phase scope and existing notes before recording clean-base gate failures and closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.4.1.3.md

<!-- sase:referenced-by:end -->
