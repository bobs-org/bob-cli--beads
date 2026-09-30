# Bead: bob-cli-2y.1 — Pause the MacBook's hooks cron before the first 2026-10-01 pass

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.1` · **Size:** small
**Created:** 2026-09-30 16:41:59 EDT · **Closed:** 2026-09-30 16:55:50 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

cutover-pause: best-effort, backed-up pause of the Mac's task-status-hooks crontab line so tomorrow's first pass cannot demote the current [/] and [*] tasks.

## Notes

[2026-09-30T20:55:12Z · bob-cli-2y.1] cutover-pause result 2026-09-30 ~16:55 EDT: Mac REACHABLE (ssh mac true OK) but hooks cron NOT paused — crontab is not writable over ssh. `crontab` (setuid root) fails identically via stdin, via file arg, and with a clean env: `crontab: tmp/tmp.PID: Operation not permitted` (sandbox/TCC denial writing /var/at/tabs, which is drwx------ root). No passwordless sudo (sudo -n fails). Backups saved: /tmp/mac-crontab-backup-20260930T205334.txt (apollo) and ~/mac-crontab-backup-20260930T205334.txt (Mac). Exact original hooks line: `*/15 * * * * ~/.cargo/bin/bob task-status-hooks >> /var/tmp/bob_task_status_hooks.log` (note: live tab uses */15 for all three jobs and no --retry-timeout flag, unlike docs/vault-git-sync.md). Prepared paused tab is staged on BOTH sides: /tmp/mac-crontab-new-20260930T205334.txt (apollo) and ~/mac-crontab-new-20260930T205334.txt (Mac) — single-line change prefixing `#PAUSED retire-now cutover: `. Bryan hand-step (Mac Terminal, NOT ssh): `crontab ~/mac-crontab-new-20260930T205334.txt && crontab -l`, ideally tonight before 06:00. No demotion has occurred: 2026/20261001.md does not exist on the Mac yet and recent log passes show 0 cleared / 0 cleared_in_progress (cron pid 589 running, last passes in sync). Nothing else changed on the Mac.

[2026-09-30T20:55:22Z · bob-cli-2y.1] PROPOSED FOLLOW-UP: crontab is not writable over `ssh mac` (sandbox EPERM on /var/at/tabs); rollout/Bryan checklist should include the one-line Mac-Terminal hand-install `crontab ~/mac-crontab-new-20260930T205334.txt` before 06:00 2026-10-01, and hooks-resume restore will hit the same wall remotely.

[2026-09-30T20:55:50Z · bob-cli-2y.1] Mac reachable but crontab NOT paused: setuid crontab fails over ssh with Operation not permitted (sandbox denial on /var/at/tabs) via stdin, file, and clean-env attempts; no passwordless sudo. Verified: live tab read and backed up twice (apollo /tmp/mac-crontab-backup-20260930T205334.txt, Mac ~/mac-crontab-backup-20260930T205334.txt); exact hooks line recorded; paused tab staged on both sides incl. Mac ~/mac-crontab-new-20260930T205334.txt for Bryan hand-install via Mac Terminal before 06:00 2026-10-01. Verified no demotion yet: no 20261001.md on Mac, recent log passes 0 cleared/0 cleared_in_progress, highlights+projects lines untouched. Epic-symbols clean; follow-ups recorded on bead.

## Dependencies

- **Blocks:** [bob-cli-2y.3](bob-cli-2y.3.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.1/README.md) | [bob-cli-2y.1](bob-cli-2y.1.md) | 0 |
