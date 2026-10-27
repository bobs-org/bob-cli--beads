# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1 — Remove the pinned legacy\_dependency\_children key from hooks JSON

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1` · **Size:** small
**Created:** 2026-10-27 11:12:34 EDT · **Closed:** 2026-10-27 11:27:48 EDT
**Plan:** [202610/backlog\_batch18\_hooks\_legacy\_key\_stats\_perf\_clippy\_gate\_refs\_copy\_docs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch18_hooks_legacy_key_stats_perf_clippy_gate_refs_copy_docs.md)

## Description

hooks-legacy-key: resolve bob-cli-cq by deleting the key that v0.4.0 shipped pinned at 0, with a breaking-change commit and updated docs and tests.

## Notes

[2026-10-27T15:27:48Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1] Removed legacy_dependency_children from hooks JSON: deleted the field from SyncResult (model.rs), its constructor (sync.rs), and the retry test fixture (retry.rs); replaced 5 pin assertions with JSON-absence assertions across sync.rs, dependency_lines.rs, dependency_line_writes.rs CLI tests; updated docs/task-status-hooks.md (report list, JSON example, compat note) and docs/task-dependencies.md §4 output list + §10 compatibility output. Gate verified: git tag --contains 0f76d558 lists v0.4.0. No readers in bob-plugins, bob-mac-capture, or chezmoi (grep empty). Verified: 154 task_status_hooks CLI tests pass, 120 lib hooks tests pass, just docs-check passes, just check passes. No epic symbols. Changes left uncommitted in 8 files for the lander (breaking-change ! commit with footer is the lander's call per release-train decision).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b1c6be2`](https://github.com/bobs-org/bob-cli/commit/b1c6be2c7474f9b608e04f5740a7f825b3470a4b) | feat(task-status-hooks)!: remove legacy\_dependency\_children from hooks JSON | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.1.md) | 2026-10-27 11:28:32 EDT |
