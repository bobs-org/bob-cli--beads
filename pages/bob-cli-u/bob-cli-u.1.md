# Bead: bob-cli-u.1 — Bob completion and task-ID mutation contract

[Bead Pages](../README.md) / [bob-cli-u](README.md) / bob-cli-u.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.02a](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.02a.md) · **Assignee:** `bob-cli-u.1` · **Size:** medium
**Created:** 2026-08-15 10:10:31 EDT · **Closed:** 2026-08-15 10:27:51 EDT
**Plan:** [202608/file\_plus\_any\_task.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/file_plus_any_task.md)

## Description

bob_task_identity_contract: define opt-in all-task discovery, safe ID assignment, and the tested CLI wire contract.

## Notes

[2026-08-15T14:27:51Z · bob-cli-u.1] Verified the opt-in completion/mutation contract: default and @file: stay identified-only; --all-tasks on @file+ returns every open task with identified-before-unidentified order, multi-field prefix/substring search, and additive nullable block_id/route/ref/requires_block_id JSON. capture-task-id assigns ^id on LF and CRLF notes, dry-run is write-free, shifted refs recover with an updated ref, and invalid/duplicate/stale/ambiguous/terminal/already-identified/missing failures leave bytes unchanged. just all and just check-scripts passed; cargo package --list --allow-dirty includes src/native/capture_task_id.rs (just package-list itself refuses this dirty tree).

[2026-08-15T14:28:24Z · bob-cli-u.1] just all (fmt, lint, full test suite); just check-scripts; cargo package --list --allow-dirty includes src/native/capture_task_id.rs. capture-complete --all-tasks is opt-in and returns missing-ID candidates without changing the default identified-only path; bob capture-task-id assigns a block ID via stale-safe refs and leaves the note unchanged on dry-run, duplicate IDs, stale/ambiguous refs, terminal/already-identified tasks, and missing/unreadable notes.

## Dependencies

- **Blocks:** [bob-cli-u.2](bob-cli-u.2.md) ✓ · ⧖ 2026-08-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-u.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-u.1/README.md) | [bob-cli-u.1](bob-cli-u.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2037307`](https://github.com/bobs-org/bob-cli/commit/2037307c852e7257e77d96f6e9c118ea23bacdff) | feat(capture): add any-task completion and capture-task-id | [bob-cli-u.1](bob-cli-u.1.md) | 2026-08-15 10:29:08 EDT |
