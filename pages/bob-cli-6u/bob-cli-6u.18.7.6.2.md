# Bead: bob-cli-6u.18.7.6.2 — Navigation-hotkeys move walk-through, reversal rewrite failures, and wiring tests

[Bead Pages](../README.md) / [bob-cli-6u.18.7.6](bob-cli-6u.18.7.6.md) / bob-cli-6u.18.7.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.land.md) · **Assignee:** `bob-cli-6u.18.7.6.2` · **Size:** medium
**Created:** 2026-10-12 22:09:27 EDT · **Closed:** 2026-10-12 22:31:05 EDT
**Plan:** [202610/prj\_line\_blocking\_final\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_final_audit_fixes.md)

## Description

nav-fixes: walk through a [?] ^prj on move promotion, report post-write reversal link-rewrite failures and keep the project note, add schedule-tag and recovery-writer wiring tests that fail on the old code, drop dead exports.

## Notes

[2026-10-13T02:31:05Z · bob-cli-6u.18.7.6.2] nav-fixes done. 1) Move promotion (215): ^prj walk-through now runs before the ? gate, so a [?] ^prj never promotes itself but its open Depends-On targets still rise; closed lines still return 0. New test 'walks through a [?] ^prj to its open prerequisite' failed on old build (no R.md change) and passes now. 2) Reversal (665+new 666 fragment, registered in fragments.json): post-write rewrites that throw or find changed content count planned links as failed; any failure keeps the project note with 'Restored the task in <parent>, but N links could not be updated; <note> was kept' plus the Pomodoro suffix when the daily rewrite failed. New tests (linking-note-changed, daily-rewrite-failure) fail 2/24 on old code, pass now. 665 stays under 1000 lines (979). 3) Schedule-tag: new update/delete tests with resident recovery missing (own open Depends-On, ^prj closed history) strip the tag while resident stays [?]; exactly those 2 fail on a7fafed code. 4) Wiring: plugin-level test through applyCountedLocalTaskDependency and Task Link batch test through deleteLinkPickerPropertyValue, both asserting [unblocked::] via fake freshness API; each fails when its markUnblockedLine wiring is removed (2 fail, 41 pass with both removed). 5) Dropped dead projectPrjKeepsDependsOnReason/projectResidentRecoveryClears defs+exports; added countPlannedRewriteLinksByPath/applyPlannedBlockIdLinkRewrites exports. Manifest 2.26.0->2.27.0, README nav row bumped + keep-notice phrase, bob-cli docs/task-dependencies.md §13.10 keep-sentence. Verify: npm run build ok, npm test 2556/2561 (only allowed bob-cli-6v x4 + bob-cli-6w x1), npm run validate 6/6, bob plugins sync -p bob-navigation-hotkeys deployed on this host (2 copied), bob-cli just check fails only the allowed bob-cli-6m percent-listen x2. Tree left uncommitted in both repos for the land agent to stitch; epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-6u.18.7.6.4](bob-cli-6u.18.7.6.4.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.6.2/README.md) | [bob-cli-6u.18.7.6.2](bob-cli-6u.18.7.6.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`178dc21`](https://github.com/bobs-org/bob-cli/commit/178dc21ce51e562f11a42d5e816b121d158a818e) | docs(task-deps): document nav-fixes for project blocking, reversal, and schedule writes | [bob-cli-6u.18.7.6.2](bob-cli-6u.18.7.6.2.md) | 2026-10-12 22:32:51 EDT |
| bob-plugins | [`bob-plugins@5d8975b`](https://github.com/bobs-org/bob-plugins/commit/5d8975bcab2d39e7ed57305a9ee3dbc21e1e9968) | fix(nav-hotkeys): project move, reversal, and schedule-write nav fixes with tests | [bob-cli-6u.18.7.6.2](bob-cli-6u.18.7.6.2.md) | 2026-10-12 22:34:13 EDT |
