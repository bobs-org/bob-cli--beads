# Bead: bob-cli-15.5 — Backup exclusion list for regenerable data

[Bead Pages](../README.md) / [bob-cli-15](README.md) / bob-cli-15.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0dy](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.0dy/README.md) · **Assignee:** `bob-cli-15.5` · **Size:** medium
**Created:** 2026-08-26 08:19:52 EDT · **Closed:** 2026-08-26 09:42:36 EDT
**Plan:** [202608/disk\_space\_reclamation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/disk_space_reclamation.md)

## Description

bkexclude: extend the rsync exclude list in backup.sh so build artifacts, agent workspaces, and toolchain caches stop being copied into every backup rotation.

## Notes

[2026-08-26T13:42:36Z · bob-cli-15.5] Extended live backup.sh _run_rsync excludes for Rust targets, node_modules, SASE workspaces, and listed toolchain/session directories. Verified with bash -n, fixture rsync --dry-run copy filtering, fixture rsync --dry-run --delete-excluded cleanup scheduling, df -h / /mnt/hercules before and after, and epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-15.1](bob-cli-15.1.md) ✓ · ⧖ 2026-08-26
- **Blocks:** [bob-cli-15.6](bob-cli-15.6.md) ✓ · ⧖ 2026-08-26
- **Blocks:** [bob-cli-15.7](bob-cli-15.7.md) ✓ · ⧖ 2026-08-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-15.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-15.5/README.md) | [bob-cli-15.5](bob-cli-15.5.md) | 0 |
