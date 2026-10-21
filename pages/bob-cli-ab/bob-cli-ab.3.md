# Bead: bob-cli-ab.3 — Calibrate thresholds and measure on the Mac

[Bead Pages](../README.md) / [bob-cli-ab](README.md) / bob-cli-ab.3

**Status:** ○ open · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.27.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.27.linker.w0.md) · **Size:** medium
**Created:** 2026-10-20 17:44:13 EDT
**Plan:** [202610/capture\_similar\_tasks\_band.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_similar_tasks_band.md)

## Previously Closed

> ↺ Closed 2026-10-21T00:50:54Z · done
>
> (none)
>
> Reopened 2026-10-21T00:52:11Z by `sase bead open`

## Description

calibrate: build the leave-one-out sampling script, collect Bryan's labels, set the bars from them, time a release build on the Mac against the 50 ms gate, and file a calibration report in the research sidecar.

## Notes

[2026-10-21T00:40:27Z · bob-cli-ab.3] PROPOSED FOLLOW-UP: Time release bob capture-related on the Mac when it is online (30 qualifying + 30 non-qualifying runs); if p95 exceeds 50 ms, file the in-app index-escalation task bead from the research and do not block

[2026-10-21T00:50:18Z · bob-cli-ab.3] PROPOSED FOLLOW-UP: Collect Bryan labels for the 100-pair calibration worksheet (0/100 filled 2026-10-21), then set bands.rs bars to possible_duplicate precision >= 80% and similar usefulness >= 60% (calibration=labels decision; do not invent researcher labels)

[2026-10-21T00:50:54Z · bob-cli-ab.3] Sampler landed: scripts/dev/capture_related_calibrate + _test wired into just check-scripts (just check-scripts green incl. new PASS; 12 capture_related unit + 1 CLI test green). Live rerun reproduces census exactly: 502 queries/0 errors, firing rates 10/24/30/42, bands 2/7/19/0/26/448, all 28 fired rows byte-identical. Bars stay at starting values per R10: worksheet labels are 0/100 (Q1 checkbox notwithstanding), so no retune; recorded as PROPOSED FOLLOW-UP. Mac still offline (SSH timeout rechecked); timing stays provisional + follow-up recorded. calibration.md updated in research sidecar (rerun table, 30-pair fix).

[2026-10-21T00:57:41Z · bob-cli-ab.3] PROPOSED FOLLOW-UP: Reconcile the completed-labels Q&A with the audited worksheet, which is still 0/100 labeled, then set thresholds from Bryan’s labels; the MacTiming “online” answer also still times out over SSH on recheck, so run the 30+30 Mac timing when reachable.

## Dependencies

- **Depends on:** [bob-cli-ab.2](bob-cli-ab.2.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ab.8](bob-cli-ab.8.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ab.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ab.3.md) | [bob-cli-ab.3](bob-cli-ab.3.md) | 0 |
