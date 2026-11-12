# Bead: bob-cli-kd.6.1.3 — Month and queue cards with the daily bank chip

[Bead Pages](../README.md) / [bob-cli-kd.6.1](bob-cli-kd.6.1.md) / bob-cli-kd.6.1.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.md) · **Assignee:** `bob-cli-kd.6.1.3` · **Size:** medium
**Created:** 2026-11-11 14:27:33 EST
**Plan:** [202611/bank\_obsidian.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_obsidian.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:406f620cf619e73fcdb56669 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

bank-ui-cards: render bob-bank month and queue fences and the daily bob-plan chip using the shared data and action services. Follow the bank-ui-cards section.

## Notes

[2026-11-11T21:46:48Z · bob-cli-kd.6.1.3] Implemented synthetic-fixture month and queue cards plus the daily plan chip. Verified plugin build; 167 bank/day-strip/build regression tests passed; docs inventory and manifest validation passed. Synthetic text captures are attached as file:explicit:406f620cf619e73fcdb56669. Deployment and closure remain blocked by the protected uncommitted bob-ledger-tools build from active author bob-cli-k3.5.1.3; the plugin deployment runbook requires waiting for that author, and no force overwrite was attempted. Docs lint still reports eight word-budget failures; the base docs reproduce the same eight.

## Dependencies

- **Depends on:** [bob-cli-k3.5.1.3](../bob-cli-k3/bob-cli-k3.5.1.3.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-kd.6.1.2](bob-cli-kd.6.1.2.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.6.1.4](bob-cli-kd.6.1.4.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.1.3.md) | [bob-cli-kd.6.1.3](bob-cli-kd.6.1.3.md) | 0 |
