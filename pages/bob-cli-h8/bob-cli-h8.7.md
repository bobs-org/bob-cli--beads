# Bead: bob-cli-h8.7 — Alert on hostile CPU, writable-dir execution, and mining egress on athena

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.7

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.7` · **Size:** medium
**Created:** 2026-11-04 16:39:09 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

athena-hostile-alerts: in the tailnet repo, add per-user CPU telemetry (process-exporter on loopback), a textfile collector for writable-dir and deleted-binary execution plus nft mining-port egress counters, and Prometheus rules with promtool tests and staleness alerts. Route them through the existing Alertmanager email path. Deploy through /sase_sudo, prove that synthetic alerts fire and resolve, and close bob-cli-8r.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.7/README.md) | [bob-cli-h8.7](bob-cli-h8.7.md) | 0 |
