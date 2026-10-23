# Bead: bob-cli-an.6.6.2 — Prove daily, weekly, and monthly backup rotations advance

[Bead Pages](../README.md) / [bob-cli-an.6.6](bob-cli-an.6.6.md) / bob-cli-an.6.6.2

**Status:** ◎ claimed · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md) · **Assignee:** `bob-cli-an.6.6.2--mon` · **Size:** medium
**Created:** 2026-10-23 17:27:15 EDT
**Plan:** [202610/backlog\_batch3\_rfserver\_backups\_day\_zone\_webclip\_fonts\_ref\_paths.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch3_rfserver_backups_day_zone_webclip_fonts_ref_paths.md)

## Description

backup-tier-freshness: resolve bob-cli-b2 by verifying the first post-fix daily and weekly rotations on Athena, diagnosing and fixing any tier that still fails, and recording monthly evidence.

## Notes

[2026-10-23T21:33:10Z · bob-cli-an.6.6.2] Baseline 2026-10-23 17:33 EDT on athena (pre-rotation): hourly fresh (1792790935, ~5min old, proves rsync-24 fix on hourly); daily marker 1792298910 (2026-10-18 00:48 EDT, 5.78d old) vs daily-2 1791348786 (2026-10-07); weekly 1790399942 (2026-09-26, 27.76d) vs weekly-2 1788632050 (2026-09-05); monthly 1776921321 (2026-04-23, 183.76d), monthly-2 has no backup.txt. Anacron spool mtimes: cron.daily Oct23 00:54, cron.weekly Oct17 01:38, cron.monthly Oct21 01:47 (root-owned, not directly readable). Installed backup.sh at /usr/local/lib/athena-cron/backup.sh contains exit-24 commit path (lines 237-252) plus TOO_SOON guard. Live scripts daily/weekly/monthly/hourly present in /etc/cron.*. Restore-sample method established as bryan-readable: /mnt/hercules/backup/home/<tier>/bryan/.bashrc. Waiting for first anacron pass of 2026-10-24 (~00:30-01:30 EDT) before verifying.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.2.md) | [bob-cli-an.6.6.2](bob-cli-an.6.6.2.md) | 0 |
