# Bead: bob-cli-qq.10.2 — Fix the intermittent Reading card miss in the shared property-card host

[Bead Pages](../README.md) / [bob-cli-qq.10](bob-cli-qq.10.md) / bob-cli-qq.10.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.g7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.g7.md) · **Assignee:** `bob-cli-qq.10.2` · **Size:** medium
**Created:** 2026-11-27 09:12:20 EST · **Closed:** 2026-11-27 10:25:03 EST
**Plan:** [202611/finish\_property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_property_card_cabinets.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:7316b0d305d801541fead234 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

reading-miss: in the 240c host, resolve a Reading surface from the live preview leaf when the postprocessed element is detached or its retries are exhausted. Re-render only an eligible note that no host has carded, keep the absorption tags, and show zero misses in a reload loop.

## Notes

[2026-11-27T15:24:21Z · bob-cli-qq.10.2] Reload loop on Athena xvfb: GO-RELOAD-LOOP, 20 rounds, 0 misses. Full runner 98/100: area-reading-ready-after-plugin-reload pass; every render-*-reading pass including empty-album. Artifacts: file:explicit:b5a6f3c9c0e393a018efc8d5 (summary), full-report file:explicit:470e4c3e89d3c3c09dbcd25c, verify notes file:explicit:561103f66c60801d13a0eed4.

[2026-11-27T15:24:37Z · bob-cli-qq.10.2] PROPOSED FOLLOW-UP: keys-reading-pick-overlay-lists-numbered-kinds — Reading pick overlay footer is "▤ Cabinets1Albums▸2Notebooks▸3Projects▸4Areas▸-Propertiesesc" vs expected "1 Albums" with a space; polish overlay, not the Reading miss.

[2026-11-27T15:24:45Z · bob-cli-qq.10.2] PROPOSED FOLLOW-UP: perf-106-record-album-within-budget — Athena full runner median 131ms with a 50ms long task; phase 10.1 owns perf, and this check passed on an earlier full run of the same tree.

[2026-11-27T15:24:52Z · bob-cli-qq.10.2] PROPOSED FOLLOW-UP: npm test perf flake in test-block-id-prompt-task-links-api-performance.cjs — api.taskLinks typed keystrokes p95 12.0 ms exceeds 12 ms; unrelated to 240c, unit suite 10283 otherwise green.

[2026-11-27T15:25:03Z · bob-cli-qq.10.2] 240c recovers Reading cards from the live preview leaf when the postprocessor el is detached: descendant lookup (wrapper containerEl), rebound el prefers markdown-preview-view, pane-moved-on drops leftover widgets that would steal the next note sizer. Host tests cover detached+live, wrapper+activeLeaf, exhausted retries, card-less never re-renders, second host blocks, absorption tags, and pane navigation. Athena -L 20: 0 misses. Full runner: area-reading-ready-after-plugin-reload pass and every render-*-reading pass. npm test green apart from the recorded taskLinks p95 flake. Overlay numbering and perf-106 recorded as follow-ups. No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-qq.10.4](bob-cli-qq.10.4.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.10.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.2/README.md) | [bob-cli-qq.10.2](bob-cli-qq.10.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1c4266e`](https://github.com/bobs-org/bob-plugins/commit/1c4266ed9bf938e83719e47f93175e1d0a3e1eae) | fix(ledger-tools): recover Reading property cards after plugin reload | [bob-cli-qq.10.2](bob-cli-qq.10.2.md) | 2026-11-27 10:27:41 EST |
