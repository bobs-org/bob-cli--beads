# Bead: bob-cli-qp.3 — Shared ref-library report service

[Bead Pages](../README.md) / [bob-cli-qp](README.md) / bob-cli-qp.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6l.linker.w0.md) · **Assignee:** `bob-cli-qp.3` · **Size:** medium
**Created:** 2026-11-26 14:22:08 EST · **Closed:** 2026-11-26 14:51:58 EST
**Plan:** [202611/ref\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_cards.md)

## Description

ref-service: one lazily subscribed, stale-while-revalidate `bob ref list -A -R all -f json` snapshot indexed by path and shared by every mounted card. It uses narrow, debounced revalidation triggers and never spawns from paint.

## Notes

[2026-11-26T19:51:58Z · bob-cli-qp.3] Implemented the shared full-library ref report service, immutable path index, lazy scoped subscriptions, debounce/trailing refresh, stale fallback, and unload cleanup in bob-plugins. Verified plugin build and all 6 service tests; synced the bundle after the clean-stamp recovery. No --epic-symbol entries in this working tree. reports no leftovers.

## Dependencies

- **Blocks:** [bob-cli-qp.5](bob-cli-qp.5.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qp.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.3/README.md) | [bob-cli-qp.3](bob-cli-qp.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6045168`](https://github.com/bobs-org/bob-plugins/commit/6045168fd586c71cb7cd98d94809cbabdb505838) | feat(ref-card): add shared report service | [bob-cli-qp.3](bob-cli-qp.3.md) | 2026-11-26 15:26:58 EST |
