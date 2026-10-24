# Bead: bob-cli-an.6.6.2 — Prove daily, weekly, and monthly backup rotations advance

[Bead Pages](../README.md) / [bob-cli-an.6.6](bob-cli-an.6.6.md) / bob-cli-an.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md) · **Size:** medium
**Created:** 2026-10-23 17:27:15 EDT · **Closed:** 2026-10-24 03:53:41 EDT
**Plan:** [202610/backlog\_batch3\_rfserver\_backups\_day\_zone\_webclip\_fonts\_ref\_paths.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch3_rfserver_backups_day_zone_webclip_fonts_ref_paths.md)

## Description

backup-tier-freshness: resolve bob-cli-b2 by verifying the first post-fix daily and weekly rotations on Athena, diagnosing and fixing any tier that still fails, and recording monthly evidence.

## Notes

[2026-10-23T21:33:10Z · bob-cli-an.6.6.2] Baseline 2026-10-23 17:33 EDT on athena (pre-rotation): hourly fresh (1792790935, ~5min old, proves rsync-24 fix on hourly); daily marker 1792298910 (2026-10-18 00:48 EDT, 5.78d old) vs daily-2 1791348786 (2026-10-07); weekly 1790399942 (2026-09-26, 27.76d) vs weekly-2 1788632050 (2026-09-05); monthly 1776921321 (2026-04-23, 183.76d), monthly-2 has no backup.txt. Anacron spool mtimes: cron.daily Oct23 00:54, cron.weekly Oct17 01:38, cron.monthly Oct21 01:47 (root-owned, not directly readable). Installed backup.sh at /usr/local/lib/athena-cron/backup.sh contains exit-24 commit path (lines 237-252) plus TOO_SOON guard. Live scripts daily/weekly/monthly/hourly present in /etc/cron.*. Restore-sample method established as bryan-readable: /mnt/hercules/backup/home/<tier>/bryan/.bashrc. Waiting for first anacron pass of 2026-10-24 (~00:30-01:30 EDT) before verifying.

[2026-10-24T07:53:32Z · bob-cli-an.6.6.2--1] VERIFY 2026-10-24 ~03:45 EDT (now=1792827734, post first anacron pass, no live backup run by hand). Markers: daily 1792816971 (2026-10-24 00:42:51 EDT, age 10763s=2.99h) vs daily-2 1792298910 (2026-10-18, equals pre-fix baseline daily: old daily preserved as daily-2); weekly 1792819164 (2026-10-24 01:19:24 EDT, age 8570s=2.38h) vs weekly-2 1790399942 (2026-09-26, equals baseline weekly); hourly 1792826900 (03:28, ~14min old, fresh); monthly 1776921321 (2026-04-23, unchanged as expected, next @monthly anacron pass ~2026-11-21); monthly-2 has no backup.txt (unchanged). Dir mtimes: home/daily Oct24 00:42, home/daily-2 Oct18 00:48, home/weekly Oct24 01:19, home/weekly-2 Sep26 01:19. Restore samples (bryan-readable): daily/bryan/.bashrc and weekly/bryan/.bashrc md5 e7e695a33633f083fbce13c4ea87659d IDENTICAL to live ~/.bashrc (faithful capture). Rotation content differs: weekly .bashrc readlink db/home/.bashrc vs weekly-2 Sync/home/.bashrc (live dotfiles repointed Oct 12; weekly-2 preserves Sept state); daily bryan/ has 99 entries mtime Oct24 00:33 vs daily-2 98 entries mtime Oct18 00:36. Shared commit path: /usr/local/lib/athena-cron/backup.sh lines 237-252 commit rotation on rsync exit 0-or-24 (exit 23 stays fatal); /etc/cron.{daily,weekly,monthly}/daily_backup weekly_backup monthly_backup all source it (installed Oct 23 15:02); /etc/anacrontab MAILTO=bryanbugyi34@gmail.com. Scratch monthly-shaped exercise as bryan (BACKUP_DIR=/tmp scratch, same backup() fn): run1 commits+marker, immediate rerun refuses TOO_SOON EC=1, rerun after src change rotates (probe=new v2, probe-2=old v1, marker updated); scratch dirs removed. Monthly accepted on shared-path evidence, no tier-specific change needed, no residual check required. Tailnet checkout sase/repos/external/projects/tailnet was empty stub on 2026-10-23; live files above are source of truth. No new beads created.

[2026-10-24T07:53:41Z · bob-cli-an.6.6.2--1] Verified first post-fix anacron rotations 2026-10-24: daily marker 1792816971 (00:42 EDT, ~3h old, newer than daily-2 1792298910) and weekly marker 1792819164 (01:19 EDT, ~2.4h old, newer than weekly-2 1790399942); restore samples md5-identical to live ~/.bashrc; rotation content differs (weekly symlink target, daily entry counts/mtimes); shared backup.sh exit-24 commit path confirmed + scratch rotation/TOO_SOON exercise passed; monthly unchanged as expected (next due ~2026-11-21) accepted on shared-path evidence; no epic-symbol leftovers; parent epic untouched

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.2.md) | [bob-cli-an.6.6.2](bob-cli-an.6.6.2.md) | 0 |
