# Bead: bob-cli-pf.2.1.2 — Strict property operations and byte-exact undo

[Bead Pages](../README.md) / [bob-cli-pf.2.1](bob-cli-pf.2.1.md) / bob-cli-pf.2.1.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.md) · **Assignee:** `bob-cli-pf.2.1.2` · **Size:** medium
**Created:** 2026-11-22 14:47:18 EST
**Plan:** [202611/props\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/props_cli.md)

## Description

span-operations: implement the strict six-operation protocol and pure span planner, serialization, role enforcement, candidate verification, and exact inverse operations against the inventory model.

## Notes

[2026-11-22T23:15:59Z · bob-cli-pf.2.1.2] Verified: cargo fmt --all; cargo clippy --workspace --all-targets --all-features with just-check deny gates; cargo test --lib native::props (49 passed, including golden inverse/redo). epic-symbols: none. Host just check is the remaining gate.

[2026-11-22T23:41:00Z · bob-cli-pf.2.1.2--1] PROPOSED FOLLOW-UP: just check flake in tests/gcal_ack.rs — session_timed_presses_answer_each_card and session_write_failure_keeps_earlier_answers failed under full-suite loadavg ~198 (missing .bob/gcal journal after 1200ms; debounce swallowed the second "a" so only 1 of 2 acked). Isolation rerun on this tree passed both. Unrelated to span-operations (props planner). No existing task bead.

## Dependencies

- **Depends on:** [bob-cli-pf.2.1.1](bob-cli-pf.2.1.1.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pf.2.1.3](bob-cli-pf.2.1.3.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.1.2.md) | [bob-cli-pf.2.1.2](bob-cli-pf.2.1.2.md) | 0 |
