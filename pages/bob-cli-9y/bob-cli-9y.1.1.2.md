# Bead: bob-cli-9y.1.1.2 — Integrate the guarded task-move command

[Bead Pages](../README.md) / [bob-cli-9y.1.1](bob-cli-9y.1.1.md) / bob-cli-9y.1.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-9y.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9y.1.md) · **Assignee:** `bob-cli-9y.1.1.2` · **Size:** medium
**Created:** 2026-10-19 16:37:59 EDT · **Closed:** 2026-10-19 18:16:36 EDT
**Plan:** [202610/task\_move.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_move.md)

## Description

move-command: expose the planner as bob task move with human/JSON output, dry run, bounded locking and retries, guarded writes, scoped commits, vault-sync integration, help/completion, integration tests, and documentation; leave ancestor closure to land.

## Notes

[2026-10-19T22:16:36Z · bob-cli-9y.1.1.2--3] Verified: just check passes. Exposed the planner through bob task move with human/JSON output, dry run, locking/retries, guarded writes, scoped commits, vault-sync integration, completion/help, tests, and docs. The interface builds VaultSnapshot::from_notes and passes MoveRequest/MoveSelector to plan_task_move to produce MovePlan; removed the temporary test-only module gate for production dispatch.

## Dependencies

- **Depends on:** [bob-cli-9y.1.1.1](bob-cli-9y.1.1.1.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9y.1.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9y.1.1.2.md) | [bob-cli-9y.1.1.2](bob-cli-9y.1.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8b0f378`](https://github.com/bobs-org/bob-cli/commit/8b0f3782b0eeb994adce908f78876ea943cd9bdc) | feat(task-move): expose guarded task move command | [bob-cli-9y.1.1.2](bob-cli-9y.1.1.2.md) | 2026-10-19 18:17:11 EDT |
