# Bead: bob-cli-bp.2 — Stats fetch service fixes for the Stats page and the strip

[Bead Pages](../README.md) / [bob-cli-bp](README.md) / bob-cli-bp.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2f.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2f.linker.w1.md) · **Assignee:** `bob-cli-bp.2` · **Size:** medium
**Created:** 2026-10-24 16:30:44 EDT
**Plan:** [202610/daily\_note\_day\_strip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_note_day_strip.md)

## Description

fetch-service: in bob-plugins' bob-ledger-tools, give each key its own in-flight promise behind a FIFO queue so no waiter is lost, track change generations and fetch ages so cache hits spawn only when dirty, add a cache-update listener API, a synchronous peek, and `group`. Also gate Stats page revalidation on visibility and add spawn counters.

## Dependencies

- **Blocks:** [bob-cli-bp.3](bob-cli-bp.3.md) ◐ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bp.4](bob-cli-bp.4.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bp.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.2/README.md) | [bob-cli-bp.2](bob-cli-bp.2.md) | 0 |
