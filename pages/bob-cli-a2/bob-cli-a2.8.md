# Bead: bob-cli-a2.8 — bob-ledger-tools live relation index and api.relationIndex

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.8` · **Size:** medium
**Created:** 2026-10-20 09:08:22 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

relation-index: build a raw-text relation index in bob-ledger-tools. It does a prefiltered startup scan including done/, reparses per file on change, delete, and rename, overlays unsaved editor text, publishes forward and reverse maps together, and resolves targets by path plus block id. Publish it as api.relationIndex v1 with label suggestions. Measure cold and warm costs.

## Dependencies

- **Blocks:** [bob-cli-a2.10](bob-cli-a2.10.md) ◐ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a2.11](bob-cli-a2.11.md) ◐ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.3](bob-cli-a2.3.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-a2.8.md) | [bob-cli-a2.8](bob-cli-a2.8.md) | 0 |
