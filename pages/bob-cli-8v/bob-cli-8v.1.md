# Bead: bob-cli-8v.1 — Unattended Plex upgrades and stale-apt-source alerting (bob-cli-8s)

[Bead Pages](../README.md) / [bob-cli-8v](README.md) / bob-cli-8v.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.110](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.110.md) · **Assignee:** `bob-cli-8v.1` · **Size:** medium
**Created:** 2026-10-17 12:20:28 EDT · **Closed:** 2026-10-17 15:24:53 EDT
**Plan:** [202610/athena\_plex\_autoupdate\_and\_sandbox.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/athena_plex_autoupdate_and_sandbox.md)

## Description

apt-health: reinstall unattended-upgrades with the repo.plex.tv origin, add the root-run apt source health collector, rules, and Alertmanager delivery, fix the expired GitHub CLI apt key the new alert catches, then close bob-cli-8s.

## Notes

[2026-10-17T16:48:22Z · bob-cli-8v.1] Staged collector/units/apt.conf/rules/Alertmanager under ~/ir-athena-20261017/bob-cli-8s (0700). Non-root fixture, promtool, and amtool checks passed. GitHub CLI key downloaded and fingerprint 7F38BBB59D064DBCB3D84D725612B36462313325 is unexpired. Requesting Gate 1 install. Successor: read that staging HANDOFF.md.

[2026-10-17T17:01:03Z · bob-cli-8v.1--1] Gate 1 collector-status exit 3 was a false failure: Type=oneshot finished Result=success ExecMainStatus=0, then systemctl status returned 3 for inactive. Files/timer/first collector pass landed; only cli.github.com is down. Requesting Gate 1b to enable Alertmanager, reload Prometheus, and fire AthenaAlertPipelineTest before the GitHub CLI key rotation.

[2026-10-17T19:23:58Z · bob-cli-8v.1] PROPOSED FOLLOW-UP: /etc/cron.hourly/hourly_jobs and hourly_backup are root-run symlinks into bryan-owned ~/db/bin/cron.jobs/ (same bryan-to-root class as bob-cli-8u item 4).

[2026-10-17T19:24:02Z · bob-cli-8v.1] PROPOSED FOLLOW-UP: Prometheus :9090, pushgateway :9091, and node exporter :9100 listen on all interfaces (ss LISTEN *:9090 *:9091 *:9100); Alertmanager is loopback-only on 127.0.0.1:9093.

[2026-10-17T19:24:05Z · bob-cli-8v.1] PROPOSED FOLLOW-UP: Note on bob-cli-8r that athena.apt alerts and Alertmanager email delivery now exist (postfix/Mailjet to bryanbugyi34@gmail.com, Gmail verified 2026-10-17).

[2026-10-17T19:24:53Z · bob-cli-8v.1] Verified Gate 1/1b/2 already landed (Gate 2 ledger outcome=completed, all four commands exit 0; the gate turn timed out before a successor). unattended-upgrades plex_and_security is live; dry-run Allowed origins include origin=Plex Media Server Repository,label=Plex Media Server Repository,site=repo.plex.tv plus Debian-Security; is_allowed_origin accepts plexmediaserver 1.43.4.10903-e5521bd8c. Collector Result=success ExecMainStatus=0; every athena_apt_source_up=1 including cli.github.com; athena_apt_orphan_list_files=0. Prometheus group athena.apt loaded; promtool check/test rules SUCCESS. Gmail delivered FIRING AthenaAlertPipelineTest, FIRING AthenaAptSourceStale, FIRING AthenaRootDiskSpaceWarning, then RESOLVED AthenaAptSourceStale; email notifications_total=4 failed=0. GitHub CLI key rotated to 7F38BBB59D064DBCB3D84D725612B36462313325 with .expired-2026-09-06 backup. Timers apt-daily, apt-daily-upgrade, athena-apt-source-health scheduled. Copied installed files into tailnet athena/ with runbook. Closed bob-cli-8s. Did not close parent epic bob-cli-8v. No --epic-symbol leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8v.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-8v.1.md) | [bob-cli-8v.1](bob-cli-8v.1.md) | 0 |
