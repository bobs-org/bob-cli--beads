# Bead: bob-cli-7c.2 — Rust planner emits offers and applies a selection

[Bead Pages](../README.md) / [bob-cli-7c](README.md) / bob-cli-7c.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.11.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.11.linker.w0.md) · **Assignee:** `bob-cli-7c.2` · **Size:** large
**Created:** 2026-10-13 09:48:12 EDT
**Plan:** [202610/successor\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_offers.md)

## Description

rust_offers: change plan_successors, project_close, and project_pull_in so every would-be link becomes a keyed offer, project residents are offered, the breaker is deleted, unplanned predecessors use the implicit destination, and a selection input drives link, mint, Next, and freshness writes; port the SO vectors as unit tests.

## Notes

[2026-10-13T15:36:15Z · bob-cli-7c.2] Implemented rust_offers: plan_successors, project_close, and project_pull_in emit keyed successor offers (hand_off, project, project_finished). Selection drives link, mint, Next, and freshness writes; CLI call sites pass SuccessorSelection::None so capture still compiles. Breaker deleted. Planner SO vectors plus CLI fixtures cover picked, unpicked, implicit destination, and the kill switch. No leftover --epic-symbol entries. Parent bob-cli-7c stays open.

## Dependencies

- **Depends on:** [bob-cli-7c.1](bob-cli-7c.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.3](bob-cli-7c.3.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7c.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.2.md) | [bob-cli-7c.2](bob-cli-7c.2.md) | 0 |
