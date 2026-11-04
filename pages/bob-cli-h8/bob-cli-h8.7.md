# Bead: bob-cli-h8.7 — Alert on hostile CPU, writable-dir execution, and mining egress on athena

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.7

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.7` · **Size:** medium
**Created:** 2026-11-04 16:39:09 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

athena-hostile-alerts: in the tailnet repo, add per-user CPU telemetry (process-exporter on loopback), a textfile collector for writable-dir and deleted-binary execution plus nft mining-port egress counters, and Prometheus rules with promtool tests and staleness alerts. Route them through the existing Alertmanager email path. Deploy through /sase_sudo, prove that synthetic alerts fire and resolve, and close bob-cli-8r.

## Notes

[2026-11-04T22:17:17Z · bob-cli-h8.7] Implementation complete and verified offline in the tailnet checkout; deploy is a pending sudo gate. New: athena-hostile-exec-health collector (writable-dir/deleted-binary scan + nft mining-egress counters) with 5m systemd timer, process-exporter on 127.0.0.1:9256 grouped by username, athena.hostile rules (7 alerts) with promtool tests, nft mining_egress chain + 9256 loopback boundary, process scrape job, hostile-health-reference.md + restore/verify docs. Offline evidence: unittest discover athena/tests 47 OK, supervisor tests 6 OK, promtool check rules SUCCESS (7 rules), promtool test rules SUCCESS (both files), amtool check-config OK, prettier clean. Live deploy + synthetic SYN-to-127.0.0.1:3333 fire/resolve proof runs in the filed sase_sudo gate; successor verifies the ledger, checks Gmail firing/resolved mail, then closes bob-cli-8r and this phase.

[2026-11-04T22:20:20Z · bob-cli-h8.7] Deploy filed as sudo gate sudo-6c4b23f3-5717-452c-a7ad-71c29b53625f (staged; runs after this turn ends). Batch: apt install prometheus-process-exporter, install all hostile-health + boundary files, nft/promtool validation, enable units, stack verify, then synthetic proof (gen 170s loopback SYNs to 3333, collector refresh, check-firing, check-resolved). Proof driver staged to /root/athena-hostile-proof.py, never executes the repo copy. Successor: read the ledger, verify loopback-only 9256, healthy rules, Gmail firing/resolved pair, run repo checks, then close bob-cli-8r and this phase.

[2026-11-04T22:25:34Z · bob-cli-h8.7] Gate status check 22:24 UTC: staged sudo gate sudo-6c4b23f3 (staged_id 7e0f64dc) is still pending manual approval, not lost; nothing deployed yet (no hostile files, process-exporter absent). Re-file correctly refused: pending handoff already exists. Offline tree re-verified green just now (unittest 47 OK, promtool test SUCCESS, proof driver compiles). Delivery route needs no new proof: existing Alertmanager email path already verified by 8v landing. Remaining: Bryan approves the gate on a real terminal; approving turn verifies loopback-only 9256, healthy athena.hostile rules, Gmail firing/resolved pair, runs repo checks, then closes this phase (8r left to its own land agent).

[2026-11-04T22:27:08Z · bob-cli-h8.7] Recheck: staged gate sudo-6c4b23f3 still pending manual approval, nothing deployed yet. Tree intact and green (unittest 47 OK). Bead stays open until approval; closing now would skip the required deploy+proof.

[2026-11-04T22:38:34Z · bob-cli-h8.7--1] Verification 2026-11-04T22:38Z (athena, post-gate ledger): DEPLOY INCOMPLETE - did not close. (1) process-exporter: drop-in correct (-config.path + 127.0.0.1:9256) but service never restarted - PID 1889634 runs bare binary, ss shows *:9256 NOT 127.0.0.1:9256, /metrics has zero namedprocess_namegroup_cpu_seconds_total series, prom query count-by-groupname empty, up{job=process}=1. Gate ledger verify-stack FAILED "no per-username cpu series" and syn-* proof steps SKIPPED. Needs systemctl restart prometheus-process-exporter. (2) nft: /etc/nftables.d/athena-monitoring-boundary.nft present (loopback accept + drop for 9256, mining_egress chain) but /etc/nftables.conf is stock flush-ruleset with no include, nftables.service loads only that file, so athena_monitoring/mining_egress not live; collector textfile shows athena_hostile_nft_ok 0, AthenaHostileNftReadFailing pending, MiningEgress can never fire. (3) Rules healthy: all 7 athena.hostile health=ok, alerts pending only (WritableDirExec=1 chrome test binary in /tmp, DeletedBinaryExec=1 copilot-language-server, NftReadFailing), no hostile alert FIRING - no stuck firing. Node textfile path /var/lib/prometheus/node-exporter/athena_hostile_exec_health.prom fresh (17:35). (4) Repo checks green: unittest 47 OK, promtool check config SUCCESS (3 files), check rules 7 SUCCESS, test rules SUCCESS both files, amtool check-config SUCCESS. (5) Gmail proof BLOCKED: gog oauth client bob-gcal returns 403 insufficientPermissions for gmail.search (both MiningEgress query and inbox query) - cannot confirm FIRING/RESOLVED pair. Evidence commands: ss -tlnp, systemctl cat process-exporter, curl /api/v1/rules, /api/v1/alerts, :9256/metrics, :9100/metrics, prom queries.

[2026-11-04T22:38:46Z · bob-cli-h8.7--1] PROPOSED FOLLOW-UP: restart prometheus-process-exporter after drop-in so per-username CPU series appear and 9256 binds 127.0.0.1 only - ss shows *:9256, no namedprocess_namegroup_cpu_seconds_total

[2026-11-04T22:38:50Z · bob-cli-h8.7--1] PROPOSED FOLLOW-UP: wire athena-monitoring-boundary.nft into live ruleset (include from /etc/nftables.conf or explicit nft -f + reload) so mining_egress chain exists and athena_hostile_nft_ok returns to 1

[2026-11-04T22:38:54Z · bob-cli-h8.7--1] PROPOSED FOLLOW-UP: re-run synthetic SYN-to-127.0.0.1:3333 fire/resolve proof end-to-end after restart+nft fix, then verify Gmail AthenaHostileMiningEgress FIRING+RESOLVED pair (gog gmail scopes currently 403)

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.7.md) | [bob-cli-h8.7](bob-cli-h8.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h8.7--1][1] | confirm notes landed, bead stays open | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.7.md

<!-- sase:referenced-by:end -->
