# Bead: bob-cli-15.6 — Hardlinked backup rotations via --link-dest

[Bead Pages](../README.md) / [bob-cli-15](README.md) / bob-cli-15.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0dy](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.0dy/README.md) · **Assignee:** `bob-cli-15.6` · **Size:** medium
**Created:** 2026-08-26 08:19:52 EDT · **Closed:** 2026-08-26 09:49:07 EDT
**Plan:** [202608/disk\_space\_reclamation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/disk_space_reclamation.md)

## Description

bklinkdest: make each rotation an incremental hardlink snapshot instead of a full independent copy, which is the single largest structural win on the array.

## Notes

[2026-08-26T13:49:07Z · bob-cli-15.6] Added --link-dest to _run_rsync in /home/bryan/Sync/bin/cron.jobs/backup.sh: _backup() now passes --link-dest=${to} (the still-in-place previous newest rotation) automatically for every tier, and daily/weekly/monthly/yearly cron scripts pass additional most-recent-first cross-tier --link-dest hints (e.g. daily links against hourly, weekly against daily+hourly, etc.) via backup()'s existing extra-args passthrough. Documented the hardlink-corruption constraint (no in-place edits of files under BACKUP_DIR) in _run_rsync(). Verified: bash -n on backup.sh + all 4 modified cron scripts; a fixture test (scratch source/dest, not the live array) proving (1) same-tier rotations hardlink unchanged files (stat -c %h reports 2, shared inode), (2) cross-tier linking works even on a brand-new tier with no same-tier history, and (3) a changed file gets a fresh inode while the old rotation's content is untouched (no false hardlinking, no corruption). Atomic mv-chain block and ETBB/too-soon guard logic untouched. No live rsync/backup.sh process was running or disturbed. df -h recorded: / 54% (400G avail), /mnt/hercules 95% (528G avail) - space savings accrue progressively as future rotations cycle, same as the bkexclude phase.

## Dependencies

- **Depends on:** [bob-cli-15.5](bob-cli-15.5.md) ✓ · ⧖ 2026-08-26
- **Blocks:** [bob-cli-15.7](bob-cli-15.7.md) ✓ · ⧖ 2026-08-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-15.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-15.6/README.md) | [bob-cli-15.6](bob-cli-15.6.md) | 0 |
