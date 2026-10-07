# Bead: bob-cli-5k.7.1.3 — Reversible --write path, rollback runbook, and scope caveat

[Bead Pages](../README.md) / [bob-cli-5k.7.1](bob-cli-5k.7.1.md) / bob-cli-5k.7.1.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-5k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.7.md) · **Assignee:** `bob-cli-5k.7.1.3` · **Size:** medium
**Created:** 2026-10-07 16:18:00 EDT
**Plan:** [202610/zorg\_ref\_migration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/zorg_ref_migration.md)

## Description

writer: add `-w/--write`. Under bob_sync.lock it pre-syncs, re-plans, and refuses existing targets. It then writes new files only, verifies them through the index and coverage, and deletes its own files on any failure. Then one scoped commit and a post-sync. Test it against temp git vaults, document the rollback, and update the coverage.scope caveat.

## Dependencies

- **Depends on:** [bob-cli-5k.7.1.2](bob-cli-5k.7.1.2.md) ◐ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-5k.7.1.4](bob-cli-5k.7.1.4.md) ◐ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.3/README.md) | [bob-cli-5k.7.1.3](bob-cli-5k.7.1.3.md) | 0 |
