# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1 — Keep freshness stamps off Pomodoro ledger lines

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1` · **Size:** large
**Created:** 2026-10-26 12:58:46 EDT
**Plan:** [202610/backlog\_batch14\_ledger\_integrity\_mac\_ci\_and\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md)

## Description

fresh-stamp-ledger-guard: resolve bob-cli-cf by finding the writer that stamped [fresh::] onto a Pomodoro ledger line, guarding every freshness stamper against ledger lines, and repairing the one polluted vault line through a Bryan-approved gate.

## Notes

[2026-10-26T17:10:45Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1] Planning evidence: reproduced the ledger pollution in the existing task-status-cycler host harness on clean bob-plugins c036597c5f05d92a1ee79f821c392c01cfbb5bf0. reopenActivePomodoroTask calls setActiveCheckboxStatus, which calls stampFreshnessOnEditorLine; the real ledger-tools stamper adapted with .line adds fresh to timed, placeholder, and legacy section headlines. Real linked tasks also stamp, so their behavior must be retained. Rust stamp_inner and JS stamp/keep/setRefresh share the missing ledger exclusion. Read-only live Stats still reports 205 worked minutes for 2026-10-25, VIBE 65 plus polluted VIBE 15, and the polluted theme_hues key. No application or live-vault files changed. Authored a medium tale with caller/context guards, canonical Rust/JS guards, regressions, deployment, and the mandatory human-approved repair gate; validation passed with zero warnings. Submitting through sase plan propose for the implementation continuation.

[2026-10-26T18:11:29Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1--3] Implementation, tests, deployment, and live-repair gate status for fresh-stamp-ledger-guard.

Root cause: reopenActivePomodoroTask -> setActiveCheckboxStatus -> stampFreshnessOnEditorLine, with canonical JS/Rust placement helpers accepting any open checkbox. Timed, placeholder, and legacy Pomodoro headlines were eligible; linked task sources were correctly stamped.

Writer inventory (common guards):
- Canonical placement: Rust stamp_inner via is_pomodoro_ledger_line (stamp_fresh, set_refresh, stamp_fresh_preserve_keeps). JS freshnessStampLine / freshnessKeepLine / freshnessSetRefreshLine via freshnessIsPomodoroLedgerLine. Refusals use not_task and are byte-exact, including already-polluted rows. markUnblockedLine unchanged.
- Delegation: cycler 010-core.js applyFreshStampLine; nav 470-keydown-and-freshness.js applyFreshStampLine / applyFreshRefreshLine (line-only plus optional ## Pomodoros section context); block-id-prompt 030-tasks-and-dependencies.js applyFreshStampLine. Injected/older stampers cannot stamp a recognizable ledger body.
- Context-aware: cycler 180/190 isPomodoroLedgerLineInEditor / InSourceText using findPomodorosSectionInLines + isPomodoroTaskLine (covers local, Tasks-command follow-up, fallback rewrite, and legacy headings). Nav callers pass {content, line} into the shared writer (blocks stage, counted batches, lane/link commit, freshness refresh, decay keep/classifyRottenKeepTarget, project subtree, schedule, task-move, etc.).
- Nested real tasks, quoted/indented rows with a time only in prose, and Task Link sources remain eligible.

Revisions:
- bob-cli 6f2f19324083835fdd36f34c25dd4f3fef8d5a6d plus uncommitted docs/freshness.md, src/native/freshness/placement.rs, placement_tests.rs (P19/P20 + rustfmt).
- bob-plugins rebased onto origin/master 241ca2d818eb8381d0c672c877f0415b0b1546f6; uncommitted writer-guard fragment/main.js/test edits.

Tests (this-phase):
- rustfmt on placement_tests.rs was the just-check failure; cargo fmt applied. cargo test --lib native::freshness::placement::placement_tests: 48 passed.
- Focused JS after rebase: 123 passed (reopen, cycler freshness, placement including keep, keeps file, navigation stamps, block-id).
- Repair fixture tests in /tmp/test_repair_pomodoro_fresh_stamp.py: unique repair, second-invocation no-op, drift abort, duplicate abort, CRLF preserved, preview/decline do not write.

Verification gates:
- just check (monitor nyah4w72b3hn): failed cargo fmt --check on placement_tests.rs only; later stages not reached. rustfmt now clean.
- just docs-check / bob-plugins docs:check: BOB_TEST_FIXTURE_PDF undocumented in source_store.rs (bob-cli-cc). See PROPOSED FOLLOW-UP.
- bob-plugins build: pass. validate: pass on the earlier monitor; npm test after rebase has 19 origin/master failures unrelated to this phase (see PROPOSED FOLLOW-UP). Command-mode CLICOLOR_FORCE failure from the monitor did not reproduce after rebase (test-command-mode-runner.cjs 13/13).

Deployment:
- Rebased bob-plugins onto current origin/master (4 commits: command-mode sheet, relation-index coalesce, day-strip bars, managed-only dependencies).
- bob plugins sync --no-pull -r linked checkout -p for block-id-prompt, bob-ledger-tools, bob-navigation-hotkeys, task-status-cycler. Backups: /home/bryan/.local/state/bob-cli/plugin-backups/20261026-140819
- bob plugins list after: 7 synced, 1 drift. Remaining drift is bob-command-mode (disabled in vault); not deployed because this phase did not change it and a full sync would clobber a larger vault copy.

Live evidence before repair (bob stats show worked -a -f json -g day -r 2026-10-25..2026-10-25):
- vault-sync SHA 92c3a71ee3fef1396d100efc49d3c7b039476e1d, in sync.
- 2026/20261025.md session 1020-1035 at reported line 38, name "VIBE [fresh:: 2026-10-25]", 15m, total worked 205.
- theme parts VIBE 65 + "VIBE [FRESH:: 2026-10-25]" 15; theme_hues keys vibe and "vibe [fresh:: 2026-10-25]".
- Expected after unique-line repair: VIBE 80, total 205, session name VIBE.

Repair gate: authored auto=false because the parent plan forbids live-vault mutation without a Bryan-approved /sase_gate turn. Plan approval is not that authorization. Compare-before-write locates the unique headline in 2026/20261025.md (not line 38), holds bob_sync.lock, preserves newline style, no-ops an already-repaired unique CLEAN line, and aborts on missing/ambiguous preimages. Preview is an operation. Repair writes only; successor must inspect vault status and run bob vault-sync if the only dirty path is that daily note. epic-symbols: no --epic-symbol entries. Phase left open for the gate successor to record the human outcome and close.

[2026-10-26T18:11:33Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1--3] PROPOSED FOLLOW-UP: bob-cli-cc source_store / docs-check baseline — just docs-check and bob-plugins docs:check both fail with `src/native/highlights_ref/source_store.rs` undocumented production environment name BOB_TEST_FIXTURE_PDF (workspace line 185; plugins docs-check cached bob-cli line 194). Parent plan assigns this source-store doctor/docs baseline to bob-cli-cc. Monitor nyah4w72b3hn. This phase did not change source_store.rs. Catalog/completion/help tests were not reached in just check because cargo fmt --check failed first on placement_tests.rs (now formatted).

PROPOSED FOLLOW-UP: origin/master bob-plugins test red on 241ca2d — after rebase, npm test reports 19 failures that reproduce on a clean origin/master tree with this phase's edits stashed: 18x scripts/test-dependency-line-migration.cjs `migration requires nav helper parseDependencyLegacyChildDetails`, plus scripts/test-navigation-dependencies-stage-performance.cjs `stage collections reuse one snapshot per parent` (expected null, actual undefined). Introduced by origin `241ca2d feat(navigation): read dependencies from managed lines only`. Focused freshness regressions stay green. Do not treat as this phase's writer-guard regression.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1.md) | 0 |
