# Bead: bob-cli-q4.3 — One pure Rust settle\_note that reconcile composes

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.3` · **Size:** medium
**Created:** 2026-11-25 08:51:35 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

## Description

settle-core: extract reconcile's note-local subset (the local future-schedule Blocked rule plus status groups and badges for eligible notes) as a pure `settle_note` with a line map. Reconcile composes it with byte-identical output. Add a writer helper and Rust-owned settle vectors for the plugin twin.

## Dependencies

- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.6](bob-cli-q4.6.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.7](bob-cli-q4.7.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.8](bob-cli-q4.8.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.3/README.md) | [bob-cli-q4.3](bob-cli-q4.3.md) | 0 |
