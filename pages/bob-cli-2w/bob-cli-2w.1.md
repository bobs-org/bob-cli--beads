# Bead: bob-cli-2w.1 — Task Status Cycler: versioned dependent-recovery API and cancelled-link guard

[Bead Pages](../README.md) / [bob-cli-2w](README.md) / bob-cli-2w.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ug](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0ug.md) · **Assignee:** `bob-cli-2w.1` · **Size:** small
**Created:** 2026-09-30 13:42:47 EDT · **Closed:** 2026-09-30 13:50:14 EDT
**Plan:** [202609/cancel\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/cancel_task_picker.md)

## Description

tsc-recovery-api: expose `api.recoverBlockedDependents` (version 1) from task-status-cycler. Keep a dependent Blocked while it has a strictly future `scheduled` date. When Ctrl+Enter lands on a Task Link to a Cancelled task, show a notice instead of completing the owning Pomodoro. Bump the version, update the README, add tests, and sync to the vault.

## Notes

[2026-09-30T17:50:14Z · bob-cli-2w.1] tsc-recovery-api done in bob-plugins: frozen api v1 (recoverBlockedDependents, no retire, never throws), future-scheduled dependents stay Blocked on planner+API+close paths, Ctrl+Enter on Cancelled Task Link shows notice and leaves Pomodoro open. Verified: npm test 812/812 pass, npm run validate 6/6 valid, manifest bumped to 1.17.0, README updated, synced to vault (vault manifest 1.17.0). No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-2w.3](bob-cli-2w.3.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-2w.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-2w.1/README.md) | [bob-cli-2w.1](bob-cli-2w.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@80d6647`](https://github.com/bobs-org/bob-plugins/commit/80d66477782fd3d7711c3b967f0620721b991c39) | feat(task-status-cycler): add frozen recovery api with future-schedule and cancelled-link guards | [bob-cli-2w.1](bob-cli-2w.1.md) | 2026-09-30 13:51:55 EDT |
