# Bead: bob-cli-31.7 — Bob Navigation Hotkeys gestures stamp freshness; Ctrl+Shift+P refresh row

[Bead Pages](../README.md) / [bob-cli-31](README.md) / bob-cli-31.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.v.linker.w0.md) · **Assignee:** `bob-cli-31.7` · **Size:** medium
**Created:** 2026-09-30 19:32:06 EDT · **Closed:** 2026-09-30 23:15:19 EDT
**Plan:** [202609/task\_freshness\_review.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_freshness_review.md)

## Description

nav-stamps: Alt+N, the Ctrl+Shift+P property/lane rows, Ctrl+Shift+M moves, and the dependency toggle stamp every open task they rewrite, and a new pinned refresh row sets or clears [refresh:: N].

## Notes

[2026-10-01T03:15:19Z · bob-cli-31.7] nav-stamps landed in bob-plugins: Alt+N lane, Ctrl+Shift+P property/lane, Ctrl+Shift+M moves, and ! dependency toggle stamp via api.freshness.stampLine (injected stamper, identity default); pinned refresh row sets/clears [refresh:: N] via setRefreshLine; fresh/refresh guarded from end-append writers. Verified: new scripts/test-navigation-stamps.cjs 18/18 pass, full npm test 945/945 pass, npm run validate 6/6, rg finds no upsert/insert fresh call sites, manifest 1.44.0, README row updated, deployed via bob plugins sync -p bob-navigation-hotkeys (2 copied), docs/freshness.md Surfaces row marked landed.

## Dependencies

- **Blocks:** [bob-cli-31.10](bob-cli-31.10.md) ◐ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-31.6](bob-cli-31.6.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-31.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-31.7/README.md) | [bob-cli-31.7](bob-cli-31.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`663a0bc`](https://github.com/bobs-org/bob-cli/commit/663a0bc1846d2e75a3d7854b83d9607246076357) | docs(freshness): mark nav-stamps surfaces landed | [bob-cli-31.7](bob-cli-31.7.md) | 2026-09-30 23:18:34 EDT |
