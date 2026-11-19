# Bead: bob-cli-nh.6.1.3 — Shared property-card chrome and precise documentation

[Bead Pages](../README.md) / [bob-cli-nh.6.1](bob-cli-nh.6.1.md) / bob-cli-nh.6.1.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.md) · **Assignee:** `bob-cli-nh.6.1.3` · **Size:** medium
**Created:** 2026-11-19 09:44:34 EST
**Plan:** [202611/property\_card\_kit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_kit.md)

## Description

chrome: consolidate property-card chrome and hue tokens without changing pixels, align the three plugin references around card versus card editor, and document the extension API for the intention-card phase. Compare final screenshots to the original baseline, run the complete acceptance gates, and deploy with bob plugins sync. Prepare completion evidence for the land agent; do not close bob-cli-nh.6 or bob-cli-nh from a child phase.

## Notes

[2026-11-19T20:33:06Z · bob-cli-nh.6.1.3--1] PROPOSED FOLLOW-UP: Update the navigation copy-card model row-order expectation for the copy-chip row. Reproduced on clean bob-plugins base SHA 946ef56589c2650807bdf45c3dfd0eb59005c956 with `node --test scripts/test-navigation-copy-card-model.cjs`; scripts/test-navigation-copy-card-model.cjs:558 fails ERR_ASSERTION because expected [path, absolute, file, note, template-2, block-id, template-1] but actual adds copy-chip between note and template-2. The same assertion fails on this phase tree. No existing tracker was found by `sase bead search 'copy-chip row order'` or `sase bead search 'navigation copy card'`.

## Dependencies

- **Depends on:** [bob-cli-nh.6.1.2](bob-cli-nh.6.1.2.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.3.md) | [bob-cli-nh.6.1.3](bob-cli-nh.6.1.3.md) | 0 |
