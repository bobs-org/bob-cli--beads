# Bead: bob-cli-9c.2 — Shared intake session and create wiring

[Bead Pages](../README.md) / [bob-cli-9c](README.md) / bob-cli-9c.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4s.linker.w0.md) · **Assignee:** `bob-cli-9c.2` · **Size:** medium
**Created:** 2026-10-18 14:40:03 EDT
**Plan:** [202610/ref\_ingest\_at\_birth.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_ingest_at_birth.md)

## Description

create-ingest: build the shared locked intake session in a new highlights_ref intake module. It takes the locks, pre-syncs, re-checks, moves, plans with rollback, writes, makes one scoped commit, and post-syncs. Wire it into every `bob ref create` route in place of `next: bob ref scan`. Add `-k/--keep-intake`, the `highlights.ingest_on_create` switch, and `BOB_HIGHLIGHTS_INGEST_ON_CREATE`, with scratch-vault integration tests.

## Dependencies

- **Blocks:** [bob-cli-9c.3](bob-cli-9c.3.md) ◐ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9c.4](bob-cli-9c.4.md) ◐ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9c.6](bob-cli-9c.6.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9c.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9c.2/README.md) | [bob-cli-9c.2](bob-cli-9c.2.md) | 0 |
