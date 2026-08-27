# Bead: bob-cli-1e.3 — Set the device-local exclusion and restore old\_lib in place

[Bead Pages](../README.md) / [bob-cli-1e](README.md) / bob-cli-1e.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0en](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0en.md) · **Assignee:** `bob-cli-1e.3` · **Size:** small
**Created:** 2026-08-27 08:13:35 EDT · **Closed:** 2026-08-27 08:34:38 EDT
**Plan:** [202608/unsync\_old\_lib.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/unsync_old_lib.md)

## Description

exclude: write ignoreFolders via ob sync-config, restore the staging directory to old_lib while sync is still stopped, then resume the service and cron and confirm across several cycles that no old_lib path is re-uploaded.

## Notes

[2026-08-27T12:34:38Z · bob-cli-1e.3] Set ignoreFolders=["old_lib"] via ob sync-config (verified in CLI output and raw config.json). Restored .old_lib_migrating -> old_lib (660 files, 851.1 MB, git diff vs origin/master empty). Resumed ob-sync-bob.service (active) and restored the bob-cli-1e.2-disabled 30 3 * * * bob-nightly crontab line. Watched sync.log for 5 consecutive poll cycles (~2.5 min): each logged 'Excluded folders: old_lib' and zero 'Uploading file old_lib/...' lines. Remote state.db confirms 0 live old_lib entries (0.0 MB). Sync still reports 'Vault limit exceeded' post-restore, expected per plan since attachment version history still counts the just-deleted 851 MB — that recovery check is phase verify's job, not exclude's.

## Dependencies

- **Depends on:** [bob-cli-1e.2](bob-cli-1e.2.md) ✓ · ⧖ 2026-08-27
- **Blocks:** [bob-cli-1e.4](bob-cli-1e.4.md) ✓ · ⧖ 2026-08-27
- **Blocks:** [bob-cli-1e.5](bob-cli-1e.5.md) ✓ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1e.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1e.3/README.md) | [bob-cli-1e.3](bob-cli-1e.3.md) | 0 |
