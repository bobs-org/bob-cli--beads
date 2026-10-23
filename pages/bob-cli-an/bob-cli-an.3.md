# Bead: bob-cli-an.3 — Restrict monitoring endpoints to verified clients

[Bead Pages](../README.md) / [bob-cli-an](README.md) / bob-cli-an.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12v.md) · **Assignee:** `bob-cli-an.3` · **Size:** medium
**Created:** 2026-10-21 12:58:23 EDT · **Closed:** 2026-10-23 12:00:23 EDT
**Plan:** [202610/backlog\_security\_and\_durability.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_security_and_durability.md)

## Description

monitoring: resolve bob-cli-97 after inventorying scrapes, pushers, dashboards, and firewall policy; retain apt alerts and email delivery.

## Notes

[2026-10-23T13:25:30Z · bob-cli-an.3] Phase progress 2026-10-23: endpoint-to-client matrix verified by config + read-only probes. Scrapes all local-static (no discovery): prometheus/node/pushgateway/rfserver via 127.0.0.1, clipster_server 127.0.0.1:9102 DOWN (no listener; clipster binary absent, no X). Push clients: none (pushgateway API empty). Dashboards: none (no grafana, only established conns are loopback scrapes). Alertmanager 127.0.0.1:9093 active, config intact; apt-health textfiles fresh (today) and athena_apt_health_last_run_timestamp_seconds present. State: 9090/9091/9100 already loopback via systemd drop-ins installed 2026-10-22 (processes run with --web.listen-address=127.0.0.1). NEW change by this agent: rfserver /metrics :9101 was 0.0.0.0 (prometheus_client default) exposing unauthenticated metrics; edited /home/bryan/db/bin/main/rfuncs/server.py to pc.start_http_server(9101, addr=127.0.0.1) and restarted tools:rfserver via user supervisorctl (new pid 3181265); ss confirms 127.0.0.1:9101, prometheus target rfserver UP, local 200, tailnet/LAN probes refused on 9090/9091/9100/9101/9093. Rollback: revert that one line and restart tools:rfserver (no sudo needed). promtool: config valid, 13 rules valid. md5 baselines recorded for prometheus.yml, alertmanager.yml, both rules files, three drop-ins, server.py. Remaining: privileged firewall-policy read + daemon-reload via sase_sudo gate.

[2026-10-23T13:25:38Z · bob-cli-an.3] PROPOSED FOLLOW-UP: Remove or repair the perpetually-down clipster_server :9102 Prometheus scrape job — clipster binary is not installed and no X session exists so nothing can ever listen on 9102.

[2026-10-23T13:25:42Z · bob-cli-an.3] PROPOSED FOLLOW-UP: Decide the access boundary for rfserver function port :23401 (token-authed /sendmail) — still 0.0.0.0 because RFSERVER_HOSTNAME=bbugyi.ddns.net (public DDNS) so loopback-binding may break local pymail callers; needs client inventory + firewall stance before any rebind.

[2026-10-23T16:00:23Z · bob-cli-an.3--1] Verified 2026-10-23 post-sudo: daemon-reload exit 0, all four units active/running NeedDaemonReload=no; ss 9090/9091/9100/9101/9093 on 127.0.0.1 only no IPv6 wildcards (:23401 still 0.0.0.0 intentional); nft athena_monitoring lo-accept else drop; curl 200 loopback x5, 000 refused on 100.87.31.114 and 192.168.1.156 x5; targets node/prometheus/pushgateway/rfserver UP (clipster DOWN known stale); athena_apt_health present; no emails sent; verification note added to bob-cli-97 (left open), parent epic left open.

## Dependencies

- **Depends on:** [bob-cli-an.2](bob-cli-an.2.md) ✓ · ⧖ 2026-10-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.3.md) | [bob-cli-an.3](bob-cli-an.3.md) | 0 |
