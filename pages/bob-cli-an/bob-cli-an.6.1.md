# Bead: bob-cli-an.6.1 — Move daily, weekly, and monthly root cron onto root-owned code

[Bead Pages](../README.md) / [bob-cli-an.6](bob-cli-an.6.md) / bob-cli-an.6.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md) · **Assignee:** `bob-cli-an.6.1` · **Size:** medium
**Created:** 2026-10-23 12:41:09 EDT
**Plan:** [202610/backlog\_batch2\_athena\_hardening\_and\_ref\_ids.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md)

## Description

periodic-cron: resolve bob-cli-au by extending the reviewed tailnet root-cron installation to every daily, weekly, and monthly root entrypoint and verifying their complete executable chains.

## Notes

[2026-10-23T17:05:26Z · bob-cli-an.6.1] Baseline 2026-10-23 as bryan: /etc/cron.{daily,weekly,monthly} 5 entrypoints are symlinks to bryan:bryan 0755 files (daily_jobs, daily_backup, weekly_jobs, weekly_backup, monthly_backup); live hourly pair byte-identical to tailnet hosts/athena/root-cron (dbb7368). Chain: backup tiers source bryan backup.sh; jobs tiers source bryan jobs.sh which sources $HOME/.profile (anacron sets HOME=/home/bryan, so root sources bryan profile as root) and evals bryan-PATH helpers; clean_filesystem self-escalates via sudo. sudo requires password (sudo -l prompts; 00-bryan-password-required), so jobs die at first sudo under cron (daily log shows only chown_log_files started). Hourly marker 8.5h stale, daily 5.5d, weekly 27.5d, monthly 183.5d: freshness is bob-cli-1a scope, verifier reports it without failing.

[2026-10-23T17:05:37Z · bob-cli-an.6.1] Prepared fix in tailnet hosts/athena/root-cron (uncommitted, same-turn commit via final declaration): 3 hardened backup entrypoints (logic byte-identical to bryan originals modulo env pinning, absolute lib source, #!/usr/bin/bash normalization); 2 drop-priv wrappers (root runs only bash+sudo -u bryan; vendoring rejected as wider trust surface; user-crontab rejected: loses anacron catch-up/logs/mail). Installer/verifier/exercise extended to 7 entrypoints + 4 tiers; verifier checks wrapper drop-only shape with tamper negative controls; rotation staleness informational (bob-cli-1a/6.2 owns advancement). Nonpriv validation all green: bash -n x9, py_compile x3, pre-install verifier exit 1 with exactly the 15 expected FAILs (5 symlinks x entrypoint/content/denial), content probes 5/5 PASS with 3/3 negative rejections, scratch backup tiers exit 0 with rotations (incl forced-January yearly), sim install/reinstall/rollback + both baseline guards verified. Remaining: privileged gate (install, verify incl nobody probes, run-parts x4, exercise), then close.

## Dependencies

- **Blocks:** [bob-cli-an.6.2](bob-cli-an.6.2.md) ◐ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.1.md) | [bob-cli-an.6.1](bob-cli-an.6.1.md) | 0 |
