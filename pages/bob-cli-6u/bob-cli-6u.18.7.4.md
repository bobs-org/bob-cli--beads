# Bead: bob-cli-6u.18.7.4 — Task-status-cycler and block-id-prompt residual project-blocking fixes

[Bead Pages](../README.md) / [bob-cli-6u.18.7](bob-cli-6u.18.7.md) / bob-cli-6u.18.7.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.land.md) · **Assignee:** `bob-cli-6u.18.7.4` · **Size:** small
**Created:** 2026-10-12 20:32:25 EDT
**Plan:** [202610/prj\_line\_blocking\_land\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_land_audit_fixes.md)

## Description

cycler-blockid: never strip the tag from closed lines on recovery, recover without [unblocked::] on the successor path when ledger v12 is missing, keep residents in step when Alt+] clears a ^prj date, restore lost block-id tests, restore the cycler README row.

## Notes

[2026-10-13T00:57:40Z · bob-cli-6u.18.7.4] Planned cycler-blockid items, all done:
1. Recovery never strips #prj_is_blocked from closed lines (plan builder + apply paths; PDT7). Confirmed via recoverBlockedDependents and applyBlockedDependentRecoveryEdits.
2. Successor apply recovers Blocked→Ready without [unblocked::] when ledger-tools v12 is missing, warning once instead of dropping recoveries. Regression test fails on the old drop-edits guard.
3. Alt+] on a [?] ^prj that clears its last reason recovers open residents in the same gesture (tag strip + Ready + WRITE unblocked); remaining Depends-On keeps tags; closed lines untouched.
4. Restored block-id-prompt resident consumption test and a plugin-level notice-order test (dependency reasons before project date).
5. Cycler README/manifest 1.32.0→1.33.0; block-id-prompt 1.28.0→1.29.0; bob-cli docs in task-status-hooks.md and task-dependencies.md §13.10.
Deployed on this host: bob plugins sync -n -r <opened bob-plugins> -p task-status-cycler and -p block-id-prompt.
npm test: 2533 pass, 6 fail = allowed bob-cli-6v (4 unblocked-glyph), bob-cli-6w (Keep counts once), bob-cli-3w (ranker 17.26ms). just check: only the two bob-cli-6m percent-listen failures.

## Dependencies

- **Blocks:** [bob-cli-6u.18.7.5](bob-cli-6u.18.7.5.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.4/README.md) | [bob-cli-6u.18.7.4](bob-cli-6u.18.7.4.md) | 0 |
