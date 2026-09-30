# Bead: bob-cli-2y.3 — Install sticky hooks on the MacBook and restore the cron

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.3` · **Size:** small
**Created:** 2026-09-30 16:42:00 EDT · **Closed:** 2026-09-30 17:18:43 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

hooks-resume: reinstall bob on the Mac from master, confirm with a dry run that lanes are kept, and restore the paused cron line byte-for-byte.

## Notes

[2026-09-30T21:17:47Z · bob-cli-2y.3] PROPOSED FOLLOW-UP: Mac was offline (ssh mac timed out 2026-09-30 ~17:16 EDT), so on-Mac install + dry-run + cron-verify still pending for rollout (bob-cli-2y.12): on the Mac, git pull origin/master (>=33d5622 sticky lanes, already pushed) && cargo install --path . (or --locked), then dry-run task-status-hooks --format json expecting cleared/*daily-note-only* and cleared_in_progress=[], then crontab -l must equal /tmp backup bytes incl Mac ~/mac-crontab-backup-20260930T205334.txt (crontab unwritable over ssh per 2y.1: hand-run in Mac Terminal, NOT ssh)

[2026-09-30T21:17:54Z · bob-cli-2y.3] PROPOSED FOLLOW-UP: cron was never actually paused (2y.1: setuid crontab EPERM over ssh), so hooks-resume restore is a no-op verify-bytes step unless Bryan hand-installed ~/mac-crontab-new-20260930T205334.txt before 06:00 2026-10-01 — if he did, restore exact line `*/15 * * * * ~/.cargo/bin/bob task-status-hooks >> /var/tmp/bob_task_status_hooks.log` via Mac Terminal crontab; do NOT add --retry-timeout or alter other two lines

[2026-09-30T21:18:43Z · bob-cli-2y.3] Verified: master build (33d5622) dry-run on scratch next-day vault clears only the daily-note stale [*] with cleared_in_progress=[] vs old installed bob which cleared ordinary+project [*] and project [/]; unit test sticky_lanes_keep passes; Mac offline (ssh timeout) so on-Mac install+dry-run+cron-bytes-verify handed to rollout via 2 PROPOSED FOLLOW-UP notes; cron was never paused so restore is verify-bytes no-op; epic-symbols clean

## Dependencies

- **Depends on:** [bob-cli-2y.1](bob-cli-2y.1.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2y.12](bob-cli-2y.12.md) ◐ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.2](bob-cli-2y.2.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.3/README.md) | [bob-cli-2y.3](bob-cli-2y.3.md) | 0 |
