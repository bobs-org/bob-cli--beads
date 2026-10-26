# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5 — Keep long Day strip legend labels from painting over each other

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5` · **Size:** medium
**Created:** 2026-10-26 08:32:07 EDT · **Closed:** 2026-10-26 09:34:57 EDT
**Plan:** [202610/backlog\_batch12\_perf\_baseline\_fakenode\_daystrip\_blocks\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch12_perf_baseline_fakenode_daystrip_blocks_notice.md)

## Description

day-strip-legend-overflow: resolve bob-cli-c8 by keeping each Day strip legend item at its content width and moving whole items that do not fit into the overflow counter, with a preview-harness check that catches the overlap and a bob plugins sync deploy.

## Notes

[2026-10-26T13:34:57Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5] Legend fix was pre-landed on master as 41f2093 (flex:none items + measured fit pass with names fallback, counter+title, unit/host tests) but undeployed: vault still had 1.72.0 and the harness lacked the phase-required item scrollWidth-vs-box check. Added legendItemOverflow to preview-day-strip template+(k) rule (skips invisible skeleton placeholders). Proved it fails on the old min-width:0 CSS for longLabels at 410/540/700 light+dark (26-127px) and passes with the fix (114 cells, 0 failures). Inspected longLabels crops at all widths/themes: one root+2 at 410, two roots+1 names-only at 540, three roots names-only at 700, no overlap. docs/stats.md already documents this behavior, no wording change. npm build ok, npm test 3693/3693 pass, npm run validate 7/7. bob plugins sync deployed bob-ledger-tools 1.73.0 to the vault (verified flex:none + fit in deployed copy). Target task bob-cli-c8 left open for the lander.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@abb6ea6`](https://github.com/bobs-org/bob-plugins/commit/abb6ea648c2ec40006cfa07c974151fd64eb382c) | test(ledger-tools): add item-level legend overflow check to day-strip preview harness | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5.md) | 2026-10-26 09:36:13 EDT |
