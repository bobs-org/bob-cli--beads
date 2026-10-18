# Bead: bob-cli-9c.4 — bob ref scan --intake-only drain

[Bead Pages](../README.md) / [bob-cli-9c](README.md) / bob-cli-9c.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4s.linker.w0.md) · **Assignee:** `bob-cli-9c.4` · **Size:** medium
**Created:** 2026-10-18 14:40:04 EDT
**Plan:** [202610/ref\_ingest\_at\_birth.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_ingest_at_birth.md)

## Description

scan-intake-only: add `bob ref scan -i/--intake-only`. It drains the local xlib/ queue through the intake session, with one commit per reference, and skips the annotation pass and the pre-scan hook. It refuses `-w`, adds additive JSON fields, and exits non-zero while anything stays queued, so timers surface stuck items.

## Dependencies

- **Depends on:** [bob-cli-9c.1](bob-cli-9c.1.md) ✓ · ⧖ 2026-10-18
- **Depends on:** [bob-cli-9c.2](bob-cli-9c.2.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9c.5](bob-cli-9c.5.md) ◐ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9c.6](bob-cli-9c.6.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9c.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9c.4/README.md) | [bob-cli-9c.4](bob-cli-9c.4.md) | 0 |
