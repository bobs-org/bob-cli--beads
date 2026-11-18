# Bead: bob-cli-n8.2 — Obsidian: selector dot, ink, and footer hues follow the \]s walk

[Bead Pages](../README.md) / [bob-cli-n8](README.md) / bob-cli-n8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1dx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1dx.md) · **Assignee:** `bob-cli-n8.2` · **Size:** medium
**Created:** 2026-11-18 09:48:02 EST · **Closed:** 2026-11-18 10:30:37 EST
**Plan:** [202611/review\_attention\_follows\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/review_attention_follows_walk.md)

## Description

obsidian-attention: ledger push follows the walk, POST gets its hue, nav selector gains rotten/post tiers, vectors plus a dot-iff-not-clear parity test, previews, docs, sync.

## Notes

[2026-11-18T15:30:16Z · bob-cli-n8.2--1] PROPOSED FOLLOW-UP: Stabilize the existing plugin timing-budget tests under shared-runner contention. Clean-HEAD npm run test:unit at 04ef18f reproduced the full-run scripts/test-ledger-tools-frees-marks.cjs 200-link / 2,000-task budget failure at the 25 ms bound; it also failed the independent keep-moving 1,000-task growth budget. The post-phase npm test additionally failed two keep-moving and one off-clock timing budgets in unchanged files. These timings varied substantially between runs, so investigate runner contention and budget calibration.

[2026-11-18T15:30:37Z · bob-cli-n8.2--1] Implemented and synced the walk-attention changes. npm run build passed; the focused walker-footer suite passed 46/46 after correcting the stale ROTTEN/POST expectation. npm run validate and npm run docs:check passed, and light/dark previews were reviewed. The full npm test run reported five failures before that correction: one stale phase assertion now passes in the focused suite, while four timing-budget failures occurred in unchanged paths; clean-HEAD timing failures are recorded in a PROPOSED FOLLOW-UP note. bob plugins sync copied both changed plugins. epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-n8.4](bob-cli-n8.4.md) ◐ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n8.2.md) | [bob-cli-n8.2](bob-cli-n8.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c7e6d3e`](https://github.com/bobs-org/bob-plugins/commit/c7e6d3e8906b440e897a96042d74514ddb4c4512) | feat(walks): align Obsidian attention with review walk | [bob-cli-n8.2](bob-cli-n8.2.md) | 2026-11-18 10:31:56 EST |
