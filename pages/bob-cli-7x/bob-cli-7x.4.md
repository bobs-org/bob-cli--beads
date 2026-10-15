# Bead: bob-cli-7x.4 — bob ref rename live write flow

[Bead Pages](../README.md) / [bob-cli-7x](README.md) / bob-cli-7x.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1k.linker.w0.md) · **Assignee:** `bob-cli-7x.4` · **Size:** medium
**Created:** 2026-10-15 15:25:59 EDT
**Plan:** [202610/bob\_ref\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_rename.md)

## Description

rename-write: in bob-cli, take bob_sync.lock then the scan lock, pre-sync, re-plan, snapshot, move, rewrite, verify (no-op dry-run sync plus a clean index row), roll back on failure, commit exactly the touched paths, post-sync; --offline, already_renamed re-runs, docs runbook, and the decision record.

## Dependencies

- **Depends on:** [bob-cli-7x.3](bob-cli-7x.3.md) ◐ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.5](bob-cli-7x.5.md) ◐ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.6](bob-cli-7x.6.md) ◐ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.8](bob-cli-7x.8.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7x.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7x.4/README.md) | [bob-cli-7x.4](bob-cli-7x.4.md) | 0 |
