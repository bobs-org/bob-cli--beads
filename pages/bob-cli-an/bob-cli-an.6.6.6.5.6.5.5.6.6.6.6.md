# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6 — Backlog batch 12: capture-related perf baseline, FakeNode assert OOM, Day strip new-tab and legend overflow, and the BLOCKS-line ! notice

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land`
**Created:** 2026-10-26 08:32:06 EDT · **Closed:** 2026-10-26 10:22:33 EDT
**Plan:** [202610/backlog\_batch12\_perf\_baseline\_fakenode\_daystrip\_blocks\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch12_perf_baseline_fakenode_daystrip_blocks_notice.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch12_perf_baseline_fakenode_daystrip_blocks_notice.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch12_perf_baseline_fakenode_daystrip_blocks_notice.md

<!-- sase:links:end -->

## Description

Close five backlog tasks by making the capture_related lib perf gates load-tolerant, making failing FakeNode asserts report instead of exhausting the heap, letting a modified click on the Day strip open a new Stats tab, keeping long Day strip legend labels from painting over each other, and refusing ! on a generated BLOCKS line with the documented notice.

## Notes

[2026-10-26T13:57:19Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land] LANDER VERIFICATION (steps 1-2), 2026-10-26. All 5 phases are closed. I re-read every phase note and the source of each epic commit. bob-cli: 7b8c5ddb (.1), 3633a10a (.4 docs). bob-plugins: 0ccb3ac (.3), d9823d1 (.2), 8866540 (.4), abb6ea6 (.5).
(1) capture-related-perf-baseline: both lib gates share synthetic_perf_vaults() + assert_paired_perf_gate(), following the 0e75ca56 design. Lander just check on master 01f7ec97 at load average 21-25: exit 0, both gates ok. bob-cli-ca closed done.
(2) blocks-line-bang-notice: ! and N! refuse BLOCKS lines with BLOCKS_GENERATED_LINE_NOTICE and a test. Vault nav 2.56.4 is byte-identical to the repo. bob-cli-8z closed done.
(4) day-strip-new-tab: newLeaf skips the reuse branch, with host tests for both directions and the docs/stats.md rewording. bob-cli-c6 closed done.
(5) day-strip-legend-overflow: the fit fix was pre-landed by concurrent agent 14i (bob-plugins 41f2093; bob-cli 69dfd7e8 docs). The phase added the item-level harness check and deployed it. Vault ledger-tools 1.73.0 main.js, styles.css, and manifest are byte-identical to master. bob-cli-c8 closed done.
(3) fakenode-inspect: INCOMPLETE. Plan steps 2-3 (restore assert.equal; regression proving a failing assert.equal on two live nodes reports within seconds under 1 GB) were not met. The deviation's evidence covered only descriptors, but non-enumerable bookkeeping fields do fix it: lander probe 256 ms vs OOM, details on bob-cli-c7. bob-cli-c7 stays open, and the remaining work is planned as a tale.
DECISIONS honored: deploys only via bob plugins sync; no version or CHANGELOG edits in bob-cli; no live vault edits.
Integration since 08:32: bob-cli 564168f3, af416080 (c9 highlights) and 01f7ec97 (cc.1 .bob walker) do not touch this epic's files. 14i's 41f2093 + 69dfd7e8 legend work is the c8 fix; docs/stats.md legend and Interaction text matches the deployed behavior. Phase .4's 8866540 rebased cleanly onto 41f2093, and 1.73.0 carries both. Epic symbols: none.
FOLLOW-UP TRIAGE: .3 note #1 (future Day strip DOM asserts must use the === + nodeNote form) is declined as a new task. It was in-epic guidance for phases .4/.5, which added no assert.equal on live nodes. The remaining c7 tale removes the trap at its root, so no separate task is warranted. No other PROPOSED FOLLOW-UP notes exist.
BACKLOG at this audit: 117 unresolved tasks (113 ready, 4 snoozed: 3o, 6q, aa, ah). This becomes 116 once c7 closes.

[2026-10-26T14:01:07Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land] LANDER HANDOFF: the epic stays open. Remaining work is the incomplete fakenode-inspect outcome (bob-cli-c7). It is proposed as the lander-authored tale sase_plan_backlog_batch12_land_fakenode_assert_and_closeout.md (tier tale, size medium). Its coder will: hide FakeNode back-references and bookkeeping as non-enumerable in every cyclic ledger-tools fake; restore the plan-host assert.equal checks; make the regression exercise a failing assert.equal and deepEqual under 1 GB; then close bob-cli-c7. It then finishes this landing: epic-symbols, a normal close, just symvision if present, the plan status done edit, and a parent check (batch 11 is already closed). It commits bob-plugins and the plans sidecar with /sase_git_commit and, as the effective batch-12 lander, authors and proposes batch 13 (parent_bead this epic) with the continuation contract copied verbatim.

[2026-10-26T14:22:33Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land] All five phases and target tasks are verified. The prior lander closed ca, 8z, c6, and c8 after paired perf gates and BLOCKS notice tests passed, the Day strip tests/docs matched, just check passed on master 01f7ec97 under load, vault plugins matched master, integration review found no conflicts, the .3 follow-up was declined, and epic-symbols was empty. This landing closed c7 after hiding FakeNode back-references/logs and restoring assert.equal/notEqual plan-host checks: with fields enumerable the Node 22.14 regression aborted at 7,964 ms (exit 134); hidden fields made equal/deepEqual report both nodes in 68/65 ms, and a deliberately broken plan-host assert reported in 469 ms. Touched suites 201/201, npm test 3,693/3,693, npm run validate, and docs:check (447 passed, 1 skipped) passed; bob plugins list reports 0 drift. No just symvision recipe exists. Batch 11 and batch 10 ancestors were rechecked closed.

[2026-10-26T14:41:22Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land] CONTINUATION: successor plan plan:202610/backlog_batch13_vault_integrity_and_perf.md is authored, validated, and committed. Ownership transfers to the batch-13 lander after proposal approval. Fresh no-limit enumeration after batch-12 closure: 117 unresolved tasks (113 ready, 4 snoozed: 3o, 6q, aa, ah; zero open/claimed/in_progress). Batch 13 assigns existing beads cd, cb, 5o, 67, and 6k. The higher-priority 8r hostile-process and 9x vault-sync alerts remain separate large planned launches per the continuation contract.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@24bfdb2`](https://github.com/bobs-org/bob-plugins/commit/24bfdb2a1a7cfd44964b42b23976bb4a686e8237) | test(ledger-tools): bound failing FakeNode assert diffs | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.md) | 2026-10-26 10:38:41 EDT |
| bob-cli--plans | [`bob-cli--plans@74eb763`](https://github.com/bobs-org/bob-cli--plans/commit/74eb763d63c8736e36b40d1cdf136d737bac7ab6) | docs(plan): mark batch 12 done and author batch 13 | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.md) | 2026-10-26 10:39:54 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2--1][1] | Need parent epic decisions governing the assigned phase | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3][2] | parent epic decisions | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4][3] | Need governing epic decisions before phase implementation | 2 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5][4] | Need epic DECISIONS | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land][5] | Landing: check plan-ancestor closure status | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land][6] | Need the parent link | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
