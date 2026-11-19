# Bead: bob-cli-nh.6.1.2 — Shared Reading and Live Preview host lifecycle

[Bead Pages](../README.md) / [bob-cli-nh.6.1](bob-cli-nh.6.1.md) / bob-cli-nh.6.1.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.md) · **Assignee:** `bob-cli-nh.6.1.2` · **Size:** medium
**Created:** 2026-11-19 09:44:34 EST
**Plan:** [202611/property\_card\_kit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_kit.md)

## Description

host: extract createPropertyCardHost and move album, record, and bank lifecycle plumbing onto it. Preserve species models, anchors, caches, record-walk integration, Source-mode bank lint, embed display behavior, and cleanup.

## Notes

[2026-11-19T17:08:10Z · bob-cli-nh.6.1.2] Host implementation landed (uncommitted in linked bob-plugins): createPropertyCardHost in 240c/240d; album/record/bank adapters are thin wrappers. Focused card/rail + host unit tests pass (host 8/8). npm test: 7416 pass / 1 load-flake / 2 skipped; isolated stage-performance passed in 33ms. npm run validate 12/12. Fragments ≤1000 lines. Real Obsidian e2e handed to /sase_monitor; reports will land in /tmp/nh612-e2e/out. Ownership baselines already consumed: file:explicit:d19bd1571d8869c3fbd0f94c, file:explicit:6ef537cd9927c600b96c5526, file:explicit:5366ba3f1c91e381b416eb0b. bob-cli 5b4c2636 debug bob sha256 979bdf8993f9866fb6b12e29c8a3e447e74d19b3e49f47f76451d7a706fd5ed9. -r Record host implementation and pending e2e

[2026-11-19T17:08:18Z · bob-cli-nh.6.1.2] PROPOSED FOLLOW-UP: perf flake — scripts/test-navigation-dependencies-stage-performance.cjs "stage opening builds 200/400/1000-task notes without cubic growth" failed once in full parallel npm test (400-task 382.3 ms vs 250 ms budget) and passed isolated in 33 ms; same load-flake class as ownership-phase event-link-times / bob-cli-ki. Does not keep this phase open. -r Record npm test load-flake as follow-up

## Dependencies

- **Depends on:** [bob-cli-nh.6.1.1](bob-cli-nh.6.1.1.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.6.1.3](bob-cli-nh.6.1.3.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.2.md) | [bob-cli-nh.6.1.2](bob-cli-nh.6.1.2.md) | 0 |
