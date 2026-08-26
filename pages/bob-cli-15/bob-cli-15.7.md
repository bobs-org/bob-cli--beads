# Bead: bob-cli-15.7 — Monitoring, alerting, and regression guards

[Bead Pages](../README.md) / [bob-cli-15](README.md) / bob-cli-15.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0dy](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.0dy/README.md) · **Assignee:** `bob-cli-15.7` · **Size:** small
**Created:** 2026-08-26 08:19:52 EDT · **Closed:** 2026-08-26 10:03:24 EDT
**Plan:** [202608/disk\_space\_reclamation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/disk_space_reclamation.md)

## Description

guardrails: add Prometheus disk alerts, recurring cleanup jobs, and a documented steady-state baseline so neither filesystem silently refills.

## Notes

[2026-08-26T14:02:58Z · bob-cli-15.7] PROPOSED FOLLOW-UP: Configure Alertmanager receiver for disk alerts — Prometheus rules are loaded and evaluating, but prometheus-alertmanager is inactive and /etc/prometheus/alertmanager.yml still contains sample receivers, so alerts do not leave the box yet.

[2026-08-26T14:02:59Z · bob-cli-15.7] PROPOSED FOLLOW-UP: Install or choose Cargo target sweeping tool — weekly cleanup calls skip safely because cargo-sweep is not installed; decide whether to install cargo-sweep or replace it with another supported target-prune command.

[2026-08-26T14:03:24Z · bob-cli-15.7] Verified: no epic-symbol entries; Prometheus live config and athena disk rule file pass promtool; Prometheus reloaded and reports athena.disk-space rules healthy; custom textfile metrics expose / and /mnt/hercules, with Hercules utilization query returning 95.24% and warning/critical alerts pending; live hourly/weekly cron scripts and collector pass bash -n; df baseline captured (/ 54%, /mnt/hercules 95%).

## Dependencies

- **Depends on:** [bob-cli-15.2](bob-cli-15.2.md) ✓ · ⧖ 2026-08-26
- **Depends on:** [bob-cli-15.4](bob-cli-15.4.md) ✓ · ⧖ 2026-08-26
- **Depends on:** [bob-cli-15.5](bob-cli-15.5.md) ✓ · ⧖ 2026-08-26
- **Depends on:** [bob-cli-15.6](bob-cli-15.6.md) ✓ · ⧖ 2026-08-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-15.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-15.7/README.md) | [bob-cli-15.7](bob-cli-15.7.md) | 0 |
