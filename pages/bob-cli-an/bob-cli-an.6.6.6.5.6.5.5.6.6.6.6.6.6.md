# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6 — Backlog batch 14: fresh stamps on Pomodoro ledger lines, red Mac Refs CI, the bob-cli check tool, legacy dependency readers, and relation-index publish storms

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land`
**Created:** 2026-10-26 12:58:46 EDT · **Closed:** 2026-10-26 15:39:06 EDT
**Plan:** [202610/backlog\_batch14\_ledger\_integrity\_mac\_ci\_and\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md

<!-- sase:links:end -->

## Description

Close five existing tasks by keeping freshness stamps off Pomodoro ledger lines, turning bob-mac-capture master CI green again, declaring bob-cli's named check tool, retiring the R8 legacy-child dependency readers, and coalescing relation-index publishes.

## Notes

[2026-10-26T19:05:50Z · bob-cli-ce.land] DISCOVERED ISSUE (from bob-cli-ce.land, triaging bob-cli-ce.11's PROPOSED FOLLOW-UP): phase .4's legacy-reader retirement left red tests on current masters. (1) bob-cli c4922e66: just check fails 1 lib test, native::task_status_hooks::tests::sync::fenced_column_zero_content_does_not_end_dependency_scan (panic at src/native/task_status_hooks/tests/sync.rs:233; lib 3638 passed / 1 failed). Test file last touched by 0f76d558 feat(task-deps): retire legacy child dependency readers. (2) bob-plugins 0bf8920: npm test fails 19/3832. 18 are scripts/test-dependency-line-migration.cjs cases (not ok 423-440: folds embed..., R2 adopts..., parseArgs...) that still need the removed parseDependencyLegacyChildDetails. 1 is scripts/test-navigation-dependencies-stage-performance.cjs 'stage collections reuse one snapshot per parent' at :324, 'managed-only parents never build the legacy identity map' (actual undefined, expected null), after 241ca2d feat(navigation): read dependencies from managed lines only. All other suites pass. No task bead filed because this active epic's lander owns it.

[2026-10-26T19:22:03Z · bob-cli-cn.land] DISCOVERED ISSUE: independently reproduced native::task_status_hooks::tests::sync::fenced_column_zero_content_does_not_end_dependency_scan on clean c4922e66 (stash of unrelated typical-day landing edits). Panic at src/native/task_status_hooks/tests/sync.rs:233: no entry found for key. sase tool run check 5b39829600353f50b5f1635b2fa57123: lib 3639 passed, 1 failed, 1 ignored. Same panic on a second cargo test --lib of that filter. Not Day-strip/typical work; corroborates lander note #1 that 0f76d558 left this red. No new task.

[2026-10-26T19:38:37Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land] LANDER VERIFICATION (batch 14), 2026-10-26. All 5 phases closed; every phase note re-read and each epic commit's source checked: bob-cli d7b87d41 (.3), 0f76d558 (.4), c4922e66 (.1); bob-plugins 7756f51 (.5), 241ca2d (.4), 0bf8920 (.1); bob-mac-capture bdeb4aa (.2); vault 0db2992e (.1 gate repair). DECISIONS honored: theme_field_strip = writers (theme parser untouched; writers guarded); legacy_key = pin (hooks JSON still emits legacy_dependency_children: 0, confirmed by a master dry run).

EPIC-CAUSED DEFECTS FIXED IN THE LANDING: (1) bob-plugins npm test was red on master with 19 failures from .4's 241ca2d: the one-shot migrate-dependency-lines.mjs required the removed parseDependencyLegacyChildDetails helper (18 vectors), and the stage snapshot test asserted the removed identities field. 35bda67 retires the migration script and its tests, keeps the published develop/plugins/dependency-migration page as a retirement note (the URL gate requires it to keep resolving), and rewrites the snapshot test to prove child links outside the managed line are content. npm test 3814/3814, validate green. (2) bob-cli cargo test --lib failed native::task_status_hooks::tests::sync::fenced_column_zero_content_does_not_end_dependency_scan, a legacy-child fixture .4 missed. d7cfa05c converts it to a managed line, which keeps the fenced-scan intent, and drops a duplicated assertion. (3) macOS CI on bdeb4aa: .2's new testHighlightsKeyFocusUsesContentCachedBeforeTheTabsSnapshot delivered the focus twice, because the snapshot handler re-armed after selectedID's didSet had already fired. d05f5a5 removes the redundant re-arm. portable-check passed, the mac scratch bundle and typecheck-tests passed (scratch deleted), and CI run 40383389151 passed every bob-cli-ci test plus the new one.

INTEGRATION: no concurrent commit since 12:58 (bob-cli 36ae0ef0, a170b1b3, c0489557, 3f417646, e9a955f9, 60eb7812, bd9c7a8c, 534138dd, 97edc438; bob-plugins 5790364, b70cb00, 6f8f1c5, 6b1b6ec, cc5d045) calls a freshness stamper, reads dependency children, or publishes the relation index. A concurrent bob-ledger-tools deploy had silently replaced .1's ledger guard in the vault. The lander re-synced every plugin from master 35bda67: bob plugins list shows 8 synced, 0 drift, and the guards plus scheduleRelationIndexPublish are present in the vault copies. A vault-wide grep finds 0 fresh-stamped Pomodoro ledger lines. just check via `sase tool run check` passes on master d7cfa05c (run 6fc96252).

TARGET TASKS closed done with evidence: bob-cli-cf, bob-cli-ci, bob-cli-91, bob-cli-3o, bob-cli-a5.

FOLLOW-UP TRIAGE: .1 #3 (BOB_TEST_FIXTURE_PDF docs lint) and .4 #1 (same): caused by cc.3 and fixed by the bob-cli-cc landing 534138dd (environment_ignore entry), so declined with no task. .1 #3 (19 bob-plugins npm failures): caused by this epic and fixed in the landing (35bda67). .1 #5 (cc catalog/completion/help/source_store just-check baseline): resolved on master (just check green), declined. .5 LIMITATIONS (separate async-turn publishes; renderer cost unmeasured) are recorded limitations, not proposals, so declined. Decision-mandated legacy-key removal (phase .4 recorded no follow-up): filed bob-cli-cq (feature, small), snoozed until a release contains 0f76d558. Lander discoveries: testQueuedCodeKeyCopiesWhenCatalogReturns, from cc.9 c7a5f37, is now the only red test on bob-mac-capture master CI; cc closed without recording it, so filed as bob-cli-cr (ci, large). The just docs-check published-URLs gate fails on two links to the nonexistent /bob-command-mode/, from bob-cli-ce's docs; ce is closed, so filed as bob-cli-cs (ci, small). Epic symbols: none. No just symvision recipe.

[2026-10-26T19:39:06Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land] Verified all 5 phases against source and commits; decisions theme_field_strip=writers and legacy_key=pin honored. Fixed the epic-caused regressions in the landing, which also covers DISCOVERED ISSUE notes #1 (bob-cli-ce.land) and #2 (bob-cli-cn.land): bob-plugins 35bda67 (migration script retired, snapshot test updated; npm test 3814/3814), bob-cli d7cfa05c (fenced-scan lib test on a managed line), bob-mac-capture d05f5a5 (Highlights-key focus fired once; CI 40383389151 passes all bob-cli-ci tests). Re-synced plugins from master: 0 drift, with guards present in the vault. just check green on master d7cfa05c. Target tasks cf, ci, 91, 3o, a5 closed done. Follow-ups: cq (legacy-key removal, snoozed), cr (cc.9 code-key XCTest), cs (docs URL gate); the others were declined as resolved or not proposals (see note #3). No epic symbols.

[2026-10-26T19:46:06Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land] CONTINUATION: the successor batch-15 epic plan (scratch sase_plan_backlog_batch15_vault_safety_pdf_moves_and_red_gates.md, expected archive plan:202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md, parent_bead this epic) is authored, validated (--explain then plain, 0 warnings), and submitted through sase plan propose right after this note. Ownership transfers to the batch-15 lander on approval. It assigns existing beads cj (-b pre-syncs the default vault, medium), az (coordinate rename/move, id stamp, create --force PDF writes; c9 has landed, large, after cj), cu (plugin sync overwrites another agent's uncommitted deploy, large; filed by this lander from the batch-13 cb and batch-14 cf recurrences), cr (last red Mac XCTest, large), and cs (docs URL gate, small). Decision: deploy_guard (default refuse). Additional follow-up filed during the audit: bob-cli-cu (bug, large; no duplicate, no causal active epic). Landing commits: bob-cli d7cfa05c, bob-plugins 35bda67, bob-mac-capture d05f5a5, plans b844ad5 (batch-14 status done). Fresh no-limit enumeration: 120 unresolved (115 ready, 5 snoozed: 6q, aa, ah, cp, cq). 8r and 9x remain separate large launches; 8q/b9 stay with 3j (no open phases, unlanded); 58 waits for 87's land.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d7cfa05`](https://github.com/bobs-org/bob-cli/commit/d7cfa05c16c4e760df0c885f845cd55260c2edfe) | test(task-deps): scan fenced dependents through the managed line | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) | 2026-10-26 15:26:25 EDT |
| bob-cli--plans | [`bob-cli--plans@b844ad5`](https://github.com/bobs-org/bob-cli--plans/commit/b844ad56d7006eaf0b524dd2db2fc8ed0b986f65) | chore(plans): mark backlog batch 14 done | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) | 2026-10-26 15:39:23 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2--4][1] | Verify the assigned phase parent epic remains open after closing only its phase | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land][2] | Need the epic scope, children, and linked plan file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
