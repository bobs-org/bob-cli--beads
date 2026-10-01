# Bead: bob-cli-31.5 — bob-ledger-tools api v3 freshness namespace and status bar

[Bead Pages](../README.md) / [bob-cli-31](README.md) / bob-cli-31.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.v.linker.w0.md) · **Assignee:** `bob-cli-31.5` · **Size:** medium
**Created:** 2026-09-30 19:32:06 EDT · **Closed:** 2026-09-30 22:18:10 EDT
**Plan:** [202609/task\_freshness\_review.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_freshness_review.md)

## Description

ledger-freshness: the JavaScript evaluator and placement helper on the shared vectors, api v3 (api.freshness with stampLine, state, isDue, tier, rank, queue, counts), the freshness: config, and a status bar counter that clicks through to the next due task.

## Notes

[2026-10-01T02:18:10Z · bob-cli-31.5] ledger-freshness landed: api v3 api.freshness (stampLine/setRefreshLine/state/isDue/tier/rank/intervalFor/queue/counts/lints/config) mirroring docs/freshness.md P+S vectors, freshness: config block, debounced status bar counter with click-through, manifest 1.8.0. Verified: npm test 894 pass/0 fail (21 new freshness tests), npm run validate 6/6, deployed via bob plugins sync -p bob-ledger-tools and vault copy matches, no epic-symbols remain.

## Dependencies

- **Depends on:** [bob-cli-31.1](bob-cli-31.1.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-31.4](bob-cli-31.4.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.6](bob-cli-31.6.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.8](bob-cli-31.8.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-31.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-31.5/README.md) | [bob-cli-31.5](bob-cli-31.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fcf1f6a`](https://github.com/bobs-org/bob-cli/commit/fcf1f6ab679869befac977f07ad13f0b6c2601ea) | docs(freshness): add ledger-freshness spec and phase Surfaces row | [bob-cli-31.5](bob-cli-31.5.md) | 2026-09-30 22:20:27 EDT |
| bob-plugins | [`bob-plugins@8fd0f90`](https://github.com/bobs-org/bob-plugins/commit/8fd0f906fd7f881be8814ab377a20ff4fbe85f97) | feat(ledger-tools): add ledger-freshness evaluator, api v3, and status bar | [bob-cli-31.5](bob-cli-31.5.md) | 2026-09-30 22:21:13 EDT |
