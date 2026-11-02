# Bead: bob-cli-fl.6.1.3 — Render clocks in Stats tiles and focus charts

[Bead Pages](../README.md) / [bob-cli-fl.6.1](bob-cli-fl.6.1.md) / bob-cli-fl.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.6.md) · **Assignee:** `bob-cli-fl.6.1.3` · **Size:** medium
**Created:** 2026-11-02 05:03:38 EST · **Closed:** 2026-11-02 07:19:56 EST
**Plan:** [202611/stats\_clock\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock_ui.md)

## Description

clock-charts: render Off-clock outlines and Total tails in tile sparklines and focus charts, with correct labels, neutral comparisons, spoken breakdowns, quality states, and browser preview cases.

## Notes

[2026-11-02T12:19:42Z · bob-cli-fl.6.1.3] PROPOSED FOLLOW-UP: npm test still fails four pre-existing cases (freshness-namespace, note-ready, relation-index, schedule-work-log) plus command-mode-sheet-sequence-dom Chromium discovery that does not search the Playwright cache

[2026-11-02T12:19:56Z · bob-cli-fl.6.1.3] Rendered Off-clock dashed outlines and Total worked/off-clock tails in Stats tiles, sparklines, and focus charts. Verified clock helper/DOM tests, Chromium preview (30 checks: three lenses, empty vs not_tracked, count Total, pinned family_time, forced-colors dashes), build:check, validate, and docs:check. bob-ledger-tools 1.86.0.

## Dependencies

- **Depends on:** [bob-cli-fl.6.1.2](bob-cli-fl.6.1.2.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fl.6.1.4](bob-cli-fl.6.1.4.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.3/README.md) | [bob-cli-fl.6.1.3](bob-cli-fl.6.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@33318e0`](https://github.com/bobs-org/bob-plugins/commit/33318e07cdd1e48c8fc5c8e7771fd41d0ce67bef) | feat(stats): render Off-clock outlines and Total tails in tiles and charts | [bob-cli-fl.6.1.3](bob-cli-fl.6.1.3.md) | 2026-11-02 07:37:03 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.6.1.3][1] | Need the phase scope and design file | 7 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.3/README.md

<!-- sase:referenced-by:end -->
