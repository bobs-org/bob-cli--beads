# Bead: bob-cli-28.2 — Active-task discovery module

[Bead Pages](../README.md) / [bob-cli-28](README.md) / bob-cli-28.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0t3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0t3.md) · **Assignee:** `bob-cli-28.2` · **Size:** small
**Created:** 2026-09-27 10:38:09 EDT · **Closed:** 2026-09-27 11:35:20 EDT
**Plan:** [202609/active\_task\_link.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/active_task_link.md)

## Description

active-task-discovery: build a read-only scanner that lists In Progress and Next tasks with block IDs from routable vault-root notes, annotated and ordered by today's open-Pomodoro Task Links, with query ranking and bounded warnings.

## Notes

[2026-09-27T15:35:20Z · bob-cli-28.2] Added src/native/capture_active_tasks.rs (discover/discover_at/rank + ActiveTask JSON-ready structs reusing capture-targets route predicate, note_tasks scan, and list_open_entry_links) with 8 unit tests covering ordering, ranking, nested tasks, ID/status/filename filters, mac_inbox inclusion, duplicate-link first owner, is_current rules, and all three warning paths. Verified: cargo fmt --check clean, clippy no errors, full cargo test green (911 lib + 485 cli). No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-28.1](bob-cli-28.1.md) ✓ · ⧖ 2026-09-27
- **Blocks:** [bob-cli-28.3](bob-cli-28.3.md) ✓ · ⧖ 2026-09-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-28.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-28.2/README.md) | [bob-cli-28.2](bob-cli-28.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a75c176`](https://github.com/bobs-org/bob-cli/commit/a75c17601ff776add39b3b1769c4814249bf2319) | feat(capture): add active-task discovery module | [bob-cli-28.2](bob-cli-28.2.md) | 2026-09-27 11:37:32 EDT |
