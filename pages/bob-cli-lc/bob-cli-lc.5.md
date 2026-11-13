# Bead: bob-cli-lc.5 — Pure Category card, write, and advance models

[Bead Pages](../README.md) / [bob-cli-lc](README.md) / bob-cli-lc.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c7.md) · **Assignee:** `bob-cli-lc.5` · **Size:** medium
**Created:** 2026-11-13 10:55:28 EST · **Closed:** 2026-11-13 13:25:20 EST
**Plan:** [202611/bank\_weekly\_category\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_weekly_category_walk.md)

## Description

card-model: in bob-ledger-tools, add pure, unit-tested models for decoding the new JSON, the card view model and key table, the single-transaction row write plan, the next-waiting-row finder, the walk session counter, and the end-of-run summary.

## Notes

[2026-11-13T18:25:20Z · bob-cli-lc.5] Pure Category card/write/advance models in bob-ledger-tools with unit tests. Extended 241h decode for hotkey/group/hidden/suggestion (verified new bob emits them via synthetic vault probe: rule/learned/bank tiers). New 245 model fragment (card view model, groups/tiles, inflow ordering, highlight+4 footer variants, restricted/old-bob modes, key table with chord+lock pure state, session counter, end-of-run summary) and 246 write fragment (write planner close/set with all refusals, next-waiting finder with wrap, JSON row match), exported via 356, registered in fragments.json. Regenerated bank JSON fixtures with new fields. New test-ledger-tools-bank-category-card.cjs: 8/8 pass; bank suite 73/73; build:check, docs:inventory:check, test:perf all pass. Full test:unit 6501 pass with 1 load-induced perf flake (keep-moving 200-link budget, passes alone 14/14) and 2 skipped. bob plugins sync run: ledger-tools up to date from canonical; bob-mail refusal is another workspace's uncommitted build, left untouched (no -F).

## Dependencies

- **Depends on:** [bob-cli-lc.3](bob-cli-lc.3.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-lc.6](bob-cli-lc.6.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lc.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.5/README.md) | [bob-cli-lc.5](bob-cli-lc.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lc.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.5/README.md

<!-- sase:referenced-by:end -->
