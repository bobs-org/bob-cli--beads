# Bead: bob-cli-5k.2 — Stop lib tests from racing on process environment

[Bead Pages](../README.md) / [bob-cli-5k](README.md) / bob-cli-5k.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0y2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y2.md) · **Assignee:** `bob-cli-5k.2` · **Size:** medium
**Created:** 2026-10-07 14:38:40 EDT
**Plan:** [202610/close\_top\_ten\_impact\_beads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/close_top_ten_impact_beads.md)

## Description

env-isolation: replace every module-private env-mutating test helper with one shared isolation mechanism that never lets a test see another test's BOB_DAY_FILE or BOB_NOW, enforce it with clippy, stress-test it, and close bob-cli-2e, bob-cli-40 (superseded) and bob-cli-5c.

## Dependencies

- **Blocks:** [bob-cli-5k.3](bob-cli-5k.3.md) ◐ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.2/README.md) | [bob-cli-5k.2](bob-cli-5k.2.md) | 0 |
