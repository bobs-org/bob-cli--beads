# Bead: bob-cli-7x.4 — bob ref rename live write flow

[Bead Pages](../README.md) / [bob-cli-7x](README.md) / bob-cli-7x.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1k.linker.w0.md) · **Assignee:** `bob-cli-7x.4` · **Size:** medium
**Created:** 2026-10-15 15:25:59 EDT · **Closed:** 2026-10-15 17:22:30 EDT
**Plan:** [202610/bob\_ref\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_rename.md)

## Description

rename-write: in bob-cli, take bob_sync.lock then the scan lock, pre-sync, re-plan, snapshot, move, rewrite, verify (no-op dry-run sync plus a clean index row), roll back on failure, commit exactly the touched paths, post-sync; --offline, already_renamed re-runs, docs runbook, and the decision record.

## Notes

[2026-10-15T21:22:30Z · bob-cli-7x.4--3] Implemented and verified the ref rename write flow, rollback, scoped commit, offline and already_renamed behavior, docs runbook, and authorized identity decision. Focused rename tests: 8 passed; just check: passed (with existing clippy warnings).

## Dependencies

- **Depends on:** [bob-cli-7x.3](bob-cli-7x.3.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.5](bob-cli-7x.5.md) ◐ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.6](bob-cli-7x.6.md) ◐ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.8](bob-cli-7x.8.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7x.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7x.4.md) | [bob-cli-7x.4](bob-cli-7x.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3cd6354`](https://github.com/bobs-org/bob-cli/commit/3cd63543d07ec8d46510552c25fdaec6297e98da) | feat(ref): implement verified bundle rename writes | [bob-cli-7x.4](bob-cli-7x.4.md) | 2026-10-15 17:23:43 EDT |
