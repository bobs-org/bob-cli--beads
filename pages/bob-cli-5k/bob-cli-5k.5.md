# Bead: bob-cli-5k.5 — Build the Tasks JS sandbox only when a query needs it

[Bead Pages](../README.md) / [bob-cli-5k](README.md) / bob-cli-5k.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0y2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y2.md) · **Assignee:** `bob-cli-5k.5` · **Size:** medium
**Created:** 2026-10-07 14:38:41 EDT
**Plan:** [202610/close\_top\_ten\_impact\_beads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/close_top_ten_impact_beads.md)

## Description

tasks-sandbox: construct the Tasks JavaScript sandbox lazily and give its initialization its own budget apart from the 2 s per-expression deadline, add regression tests, measure before/after latency on the live read path, and close bob-cli-33.

## Dependencies

- **Depends on:** [bob-cli-5k.3](bob-cli-5k.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.5/README.md) | [bob-cli-5k.5](bob-cli-5k.5.md) | 0 |
