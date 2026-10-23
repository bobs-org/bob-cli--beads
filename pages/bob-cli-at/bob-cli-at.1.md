# Bead: bob-cli-at.1 — macOS file-coordination primitive

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.1` · **Size:** medium
**Created:** 2026-10-23 11:44:15 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

coordinate: add `native::file_coordination`, a bounded `.forMerging` coordinated write. On macOS it is `NSFileCoordinator` through objc2, objc2-foundation, and block2 (macOS-only dependencies), with a watchdog that calls `cancel()` when the budget expires and returns Granted/Held/Failed truthfully. Elsewhere it runs the closure directly. Add a macOS-only test that compiles a small Swift NSDocument presenter fixture with `swiftc` and proves three cases: no presenter writes; a dirty presenter saves first and reloads clean; a blocked presenter is held within the budget with no write. Nothing calls the primitive yet.

## Dependencies

- **Blocks:** [bob-cli-at.3](bob-cli-at.3.md) ◐ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.1/README.md) | [bob-cli-at.1](bob-cli-at.1.md) | 0 |
