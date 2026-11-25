# Bead: bob-cli-q4.4 — Reconcile drift meter and recorded baseline

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.4` · **Size:** medium
**Created:** 2026-11-25 08:51:35 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

## Description

drift-meter: add `scripts/dev/reconcile-drift`, which replays vault commits through `bob task reconcile --dry-run -f json` with `BOB_NOW` pinned. It sorts the planned changes into churn categories, attributes them to gestures, and reports tidy debt. Record today's baseline on the phase bead.

## Dependencies

- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.4/README.md) | [bob-cli-q4.4](bob-cli-q4.4.md) | 0 |
