# Bead: bob-cli-1n.2 — Implement \`bob vault-sync\` and its conflict-copy policy

[Bead Pages](../README.md) / [bob-cli-1n](README.md) / bob-cli-1n.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ez](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ez.md) · **Assignee:** `bob-cli-1n.2` · **Size:** medium
**Created:** 2026-08-27 12:48:58 EDT · **Closed:** 2026-08-27 13:13:22 EDT
**Plan:** [202608/vault\_git\_sync.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/vault_git_sync.md)

## Description

vaultsync: add the `bob vault-sync run|status` subcommand implementing the lock-protected reconcile cycle, quarantined conflict copies under `_conflicts/`, the 95 MiB preflight guard, interrupted-merge recovery, and a machine-readable status record.

## Notes

[2026-08-27T17:13:22Z · bob-cli-1n.2] Implemented bob vault-sync run/status with lock-protected Git reconcile, conflict quarantine, large-file preflight, interrupted-merge recovery, status JSON, _conflicts exclusions, docs, and tests; verified no epic symbols remained with sase bead epic-symbols bob-cli-1n.2 and ran just all successfully.

## Dependencies

- **Blocks:** [bob-cli-1n.3](bob-cli-1n.3.md) ✓ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1n.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.2/README.md) | [bob-cli-1n.2](bob-cli-1n.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`eee290a`](https://github.com/bobs-org/bob-cli/commit/eee290ab546820b615de952f9c086f3935cb1f5c) | feat(vault-sync): add git reconcile command | [bob-cli-1n.2](bob-cli-1n.2.md) | 2026-08-27 13:14:12 EDT |
