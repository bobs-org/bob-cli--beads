# Bead: bob-cli-qi.3 — Delete the bank/area arbitration and restore the single-owner Bank Card

[Bead Pages](../README.md) / [bob-cli-qi](README.md) / bob-cli-qi.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gn.md) · **Assignee:** `bob-cli-qi.3` · **Size:** medium
**Created:** 2026-11-26 10:06:12 EST
**Plan:** [202611/bank\_hub\_demotion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_hub_demotion.md)

## Description

plugin-single-owner: delete 249db and every bank/area arbitration hook in bob-ledger-tools, restore the bank.md home-card exclusion, and gate bank on props_v1. Bank becomes a no-settings Property Editor kind whatever bob reports. Settle the 240r foot lifecycle by a species-agnostic test, convert the hybrid unit and e2e cases, fix the baseline harness blockers, then build, test, and sync.

## Notes

[2026-11-26T15:46:58Z · bob-cli-qi.3--1] PROPOSED FOLLOW-UP: Repair the block-id-prompt generated bundle/source mismatch — `npm test` on clean bob-plugins HEAD `4e0a8fd0e96453a6c92ca8293dfa0c964d1f6111` exits 1 before unit/perf tests because `node scripts/build-plugins.mjs --check` reports `plugins/block-id-prompt/main.js` stale; this plugin is outside the bank phase.

## Dependencies

- **Blocks:** [bob-cli-qi.4](bob-cli-qi.4.md) ◐ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qi.5](bob-cli-qi.5.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qi.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qi.3.md) | [bob-cli-qi.3](bob-cli-qi.3.md) | 0 |
