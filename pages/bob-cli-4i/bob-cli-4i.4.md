# Bead: bob-cli-4i.4 — Execute \`!note:block-id\` through the engine with rich JSON and human output

[Bead Pages](../README.md) / [bob-cli-4i](README.md) / bob-cli-4i.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5a](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5a.md) · **Assignee:** `bob-cli-4i.4` · **Size:** medium
**Created:** 2026-10-05 15:13:24 EDT
**Plan:** [202610/bang\_task\_complete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete.md)

## Description

execute: in bob-cli, plan `TaskComplete` items through the staged batch writer. Resolve the note vault-wide, validate status and recurrence, then run the engine (tree close, scoped ledger retirement, dependent recovery). Emit kind `task_complete` with the `task_complete` object and placement `completed`, report task_blocks roles `completed`/`unblocked`, and print green human output. Update `bob capture --help`, docs/capture.md, README, and CLI tests.

## Dependencies

- **Depends on:** [bob-cli-4i.1](bob-cli-4i.1.md) ✓ · ⧖ 2026-10-05
- **Depends on:** [bob-cli-4i.2](bob-cli-4i.2.md) ✓ · ⧖ 2026-10-05
- **Blocks:** [bob-cli-4i.5](bob-cli-4i.5.md) ◐ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4i.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4i.4/README.md) | [bob-cli-4i.4](bob-cli-4i.4.md) | 0 |
