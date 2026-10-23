# Bead: bob-cli-an.6.2 — Commit backup rotations when rsync reports only vanished files

[Bead Pages](../README.md) / [bob-cli-an.6](bob-cli-an.6.md) / bob-cli-an.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md) · **Assignee:** `bob-cli-an.6.2` · **Size:** medium
**Created:** 2026-10-23 12:41:09 EDT · **Closed:** 2026-10-23 16:34:54 EDT
**Plan:** [202610/backlog\_batch2\_athena\_hardening\_and\_ref\_ids.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md)

## Description

backup-rotation: resolve bob-cli-1a in the root-owned backup.sh that every tier now sources, keeping genuine rsync failures fatal and proving rotations land again.

## Notes

[2026-10-23T18:38:49Z · bob-cli-an.6.2] Baseline 2026-10-23 14:30 EDT as bryan: newest home/hourly is 04:24 (hourly-2 01:24, -3 23:24, -4 20:24); TOO_SOON is 30 min so the ~3h gaps are discarded rsync-24 runs, matching bob-cli-1a. home/{daily,weekly,monthly} newest are bryan-owned probe stubs (probe.txt=/home plus backup.txt at 12:54/12:59/13:03) from 6.1 pre-change fixtures; real snapshots remain at -2 (daily Oct 18, weekly Sep 26, monthly Apr 23). Root mail/syslog/cron.log are unreadable without privilege. Exit 23 kept fatal: rsync defines 23 as partial transfer due to error (incomplete snapshot); 24 is vanished sources only. Unprivileged work is in tailnet hosts/athena/root-cron: backup.sh commits rsync 24 with a stderr WARNING and discards 23/other; excludes bryan/.sase/axe/lumberjacks/ and agents_sync/cache/; restore_stub_rotations.py quarantines stubs and shifts -2 to newest; summarize_backup_mail.py counts codes without dumping bodies. unittest 19 PASS + 1 root-only SKIP; bash -n all payloads; timestamp/symlink/TOO_SOON guards still pass. Remaining: reviewed sudo batch (mail summary, stub restore, install, verify, exercise, run-parts x4), then two consecutive scheduled hourly advances and a restore sample.

[2026-10-23T19:00:39Z · bob-cli-an.6.2--1] Mail summary (sudo-3a822d33 mail-summary exit 0): scanned 4342; hourly_backup=3109 daily_backup=0 weekly_backup=0 monthly_backup=0. JOB_RETURN_CODES 1=236 (TOO_SOON) 16=2778 (RSYNC_ERROR) 34=73 4=22 (NOT_ATOMIC). RSYNC_CODES 24=2754 dominates hourly vanished-file failures; 23=40 and stays fatal (incomplete transfer). VANISHED_OR_24=2760 OTHER_RSYNC_FAILURE=349 (summarizer CODE_RE also matches "return code N", so non-24 is inflated by job EC flags). Hourly defect matches bob-cli-1a.

[2026-10-23T19:00:43Z · bob-cli-an.6.2--1] PROPOSED FOLLOW-UP: daily/weekly/monthly produced 0 root-mail messages so their live failure mode was not observed (hourly 3109, dominated by rsync 24). After stub restore, lander should confirm those tiers commit on their next scheduled runs. Optional: tighten summarize_backup_mail.py CODE_RE so it does not count "return code N" as an rsync code.

[2026-10-23T19:00:46Z · bob-cli-an.6.2--1] sudo restore-stubs failed EXDEV (errno 18) renaming /mnt/hercules/backup/home/daily -> /var/backups/bob-cli-an.6.2/stub-rotations/daily. First mutation; live tree unchanged (bryan-owned probe stubs still newest; real snapshots still at -2: daily Oct 18, weekly Sep 26, monthly Apr 23). install/verify/exercise/run-parts skipped. Fix: same-volume stub staging then copytree on EXDEV; snapshot shifts stay os.rename. Unprivileged unittest 21 PASS + 1 SKIP (added EXDEV copy + staging recovery). Re-requesting sudo batch without re-running mail-summary.

[2026-10-23T19:06:03Z · bob-cli-an.6.2--2] sudo-09d589ad (EXDEV retry) all 9 commands exit 0. restore-stubs: RESTORED home/{daily,weekly,monthly} from former -2; stubs at /var/backups/bob-cli-an.6.2/stub-rotations/{daily,weekly,monthly} (each still has probe.txt=/home). Live newest now root:root 0755, contain bryan/, no probe.txt; markers daily=1792298910 (Oct 18), weekly=1790399942 (Sep 26), monthly=1776921321 (Apr 23). install+verify 129/129; payload /usr/local/lib/athena-cron/backup.sh matches reviewed source (cmp+sha256 fc0f1d6f5569d72280bfa7d3100ae9ccdccf0b5e1cffaf2fe318f4423b21a53c). exercise EXERCISE_OK (RESTORE_SAMPLE_OK, wrappers uid=1000, scratch daily/weekly/monthly/yearly). boundary-tests 22 OK (24 commits+WARNING, 23/11/missing-source discard, EXDEV copy, staging recovery, TOO_SOON/symlink/timestamp guards). run-parts lists hourly_backup, daily_backup, weekly_backup, monthly_backup. Hourly markers still pre-change 04:24/01:24 (1792743843/1792733060, gap 10783s); .bash_logout sample currently matches the old hourly. Next: wait for two consecutive scheduled cron.hourly (17 * * * *) rotations after install; do not run a live /home backup.

[2026-10-23T20:34:34Z · bob-cli-an.6.2--3] Hourly proof after sudo-09d589ad install: monitor 007h2mxsmv08 exit 0 in 1h22m. home/hourly/backup.txt=1792787347 (2026-10-23 16:29:07 EDT), hourly-2=1792783743 (15:29:03 EDT); both newer than pre-change 1792743843 (04:24:03); gap=3604s (~1.001h, inside 1800-5400s consecutive cron.hourly, not the old 10783s discard gap). Restore sample matches: /home/bryan/.bash_logout == /mnt/hercules/backup/home/hourly/bryan/.bash_logout (sha256 26882b79471c25f945c970f8233d8ce29d54e9d5eedcd2884f88affa84a18f56, 220 bytes). Live /usr/local/lib/athena-cron/backup.sh still byte-identical to tailnet source (sha256 fc0f1d6f5569d72280bfa7d3100ae9ccdccf0b5e1cffaf2fe318f4423b21a53c). daily/weekly/monthly newest remain restored real snapshots (root:root 0755, bryan/, no probe.txt; markers 1792298910/1790399942/1776921321); probe stubs still quarantined under /var/backups/bob-cli-an.6.2/stub-rotations with probe.txt. epic-symbols clean.

[2026-10-23T20:34:54Z · bob-cli-an.6.2--3] Verified rsync-24 commit on live Athena: sudo-09d589ad restore-stubs/install/verify/exercise/boundary-tests/run-parts all exit 0 (129/129; live backup.sh sha256 fc0f1d6f matches tailnet source). Real home/{daily,weekly,monthly} snapshots restored from -2 (root-owned, bryan/, no probe.txt); probe stubs quarantined under /var/backups/bob-cli-an.6.2/stub-rotations (EXDEV copy). Boundary 22 OK (24 commits with WARNING; 23/11/missing-source discard; TOO_SOON/symlink/timestamp guards). Two consecutive scheduled hourly commits after install: 1792787347 (16:29:07 EDT) and 1792783743 (15:29:03 EDT), gap 3604s, both newer than pre-change 1792743843 (04:24); .bash_logout restore sample matches. epic-symbols clean. Did not close parent epic, bob-cli-an.6, or bob-cli-1a.

## Dependencies

- **Depends on:** [bob-cli-an.6.1](bob-cli-an.6.1.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.2.md) | [bob-cli-an.6.2](bob-cli-an.6.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.1--1][1] | need rotation phase scope to split ownership vs advancement | 1 |
| read-by | [agent:bob-cli-an.6.2--3][2] | Confirm close recorded before final declaration | 2 |
| read-by | [agent:bob-cli-an.6.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.2.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md

<!-- sase:referenced-by:end -->
