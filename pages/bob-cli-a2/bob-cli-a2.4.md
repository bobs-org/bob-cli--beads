# Bead: bob-cli-a2.4 — Reconcile owns the LINKED FROM projection

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.4` · **Size:** medium
**Created:** 2026-10-20 09:08:22 EDT · **Closed:** 2026-10-20 10:50:15 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

cli-reconcile: collect relation edges from active notes, plus read-only previous daily and done/ sources. Add a reconcile_relation_lines pass that inserts, rewrites, deletes, and dedupes LINKED FROM lines, and mints source ids, with guarded output, never pruning on uncertainty, and the kill switch. Add JSON and human outputs, relation_warnings, LR tests, and a read-only live dry run.

## Notes

[2026-10-20T14:50:15Z · bob-cli-a2.4] just check green; LR1–LR24; live dry-run bob task reconcile --dry-run -f json on ~/bob: 0 linked_from_line_updates, 0 minted_relation_source_block_ids, 0 relation_warnings, scanned_files=5264, wall≈7.16s; done/ LINKS prefilter ≈9ms over 29 files (0 hits). No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-a2.15](bob-cli-a2.15.md) ◐ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.2](bob-cli-a2.2.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.3](bob-cli-a2.3.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.4/README.md) | [bob-cli-a2.4](bob-cli-a2.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a02f9b3`](https://github.com/bobs-org/bob-cli/commit/a02f9b33b3636298706fdc06865e5b7c500899b7) | feat(task-status-hooks): project LINKED FROM lines from authored LINKS | [bob-cli-a2.4](bob-cli-a2.4.md) | 2026-10-20 10:50:54 EDT |
