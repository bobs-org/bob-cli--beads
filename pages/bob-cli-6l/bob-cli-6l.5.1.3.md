# Bead: bob-cli-6l.5.1.3 — Render metric-family context panels

[Bead Pages](../README.md) / [bob-cli-6l.5.1](bob-cli-6l.5.1.md) / bob-cli-6l.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6l.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.5.md) · **Assignee:** `bob-cli-6l.5.1.3` · **Size:** medium
**Created:** 2026-10-11 14:15:46 EDT · **Closed:** 2026-10-11 15:22:58 EDT
**Plan:** [202610/stats\_charts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/stats_charts.md)

## Description

context_panels: add theme and task breakdowns, task flow, review counterweights, calendar and chore grids using the shared chart and interaction helpers.

## Notes

[2026-10-11T19:22:46Z · bob-cli-6l.5.1.3] PROPOSED FOLLOW-UP: Full npm test shows 19 pre-existing failures (unblocked-glyph, successor-polish/wiring/promotion, navigation picker/cold-fallback) that reproduce identically on the clean base tree (verified via git stash: 12 fail in the 3 successor files alone on base); all Stats tests pass. Already noted by bob-cli-6l.5.1.2 and bob-cli-6l.4; no new bead needed.

[2026-10-11T19:22:58Z · bob-cli-6l.5.1.3] Context panels ship in bob-ledger-tools 1.46.0: kind-dispatched panels (net is the only formula exception) under the focus chart — pomodoro By-theme thin bars with total+share, task flow SVG (Created up blue, Done green + Dropped gray stacked down, 2px ink Net line from the report series, missing stays missing, absent companions named, custom-filter overall-flow note, Net splits Created/Done/Dropped breakdowns, Reviewed never plotted), journal Answers by tier/outcome in violet + Review-time total + gapped keep-rate chart with dashed 90% reopen-trigger reference and hollow today, Monday-aligned checklist calendar with 5-state legend + accessible date/display/reason cells + provisional today + horizontal scroller, chore dot grid with met/missed/not-due/unknown text labels and grouped N-of-M summaries. Panel cells reuse the chart keyboard model (roving tab stop, Enter pins with propagation stopped, hover previews shared day detail) and pin locally with zero fetches. Verified: 10/10 new panels tests pass, all existing Stats tests pass, npm run build + build:check + validate green, bob plugins sync deployed from this checkout (panels code confirmed in the vault main.js), fragments under the 1000-line limit, epic-symbols clean. Full npm test has 19 failures that reproduce identically on the clean base (recorded as PROPOSED FOLLOW-UP, already noted by .1.2/.4).

## Dependencies

- **Depends on:** [bob-cli-6l.5.1.2](bob-cli-6l.5.1.2.md) ✓ · ⧖ 2026-10-11
- **Blocks:** [bob-cli-6l.5.1.4](bob-cli-6l.5.1.4.md) ✓ · ⧖ 2026-10-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5.1.3/README.md) | [bob-cli-6l.5.1.3](bob-cli-6l.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2e7f3b0`](https://github.com/bobs-org/bob-plugins/commit/2e7f3b0ff365ad5696dc4ee0d61cfd11b84c8a8b) | feat(bob-ledger-tools): render Stats metric-family context panels | [bob-cli-6l.5.1.3](bob-cli-6l.5.1.3.md) | 2026-10-11 15:23:57 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6l.5.1.3][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-6l.5.1.land][2] | Need the epic, every child scope, and every note | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5.1.land/README.md

<!-- sase:referenced-by:end -->
