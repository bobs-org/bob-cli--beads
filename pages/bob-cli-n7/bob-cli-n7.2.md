# Bead: bob-cli-n7.2 — Fix the macOS /var symlink path failures in note catalog and note goto

[Bead Pages](../README.md) / [bob-cli-n7](README.md) / bob-cli-n7.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-n5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n5.land.md) · **Assignee:** `bob-cli-n7.2` · **Size:** medium
**Created:** 2026-11-18 01:55:52 EST
**Plan:** [202611/backlog\_triage\_t4.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t4.md)

## Description

macos-symlink: Resolve bob-cli-n6 (note_catalog xlib tier and note_goto vault_root under the /var -> /private/var temp symlink), fixing product canonicalization where it is a real bug.

## Notes

[2026-11-18T12:48:04Z · bob-cli-n7.2] Linux verification done: fixed TierContext::for_vault and ClassifyContext::new to canonicalize library/ref paths before relativizing against the canonical vault_root (lexical bob_dir fallback when path missing). note_goto vault_root test now compares canonical forms. New regression native::note_catalog::tests::symlinked_vault_root_keeps_library_tiers_hidden passes via symlink alias on Linux. Focused: 3 note_catalog lib tests ok, capture_complete_note_goto_reports_shape_without_query ok. just check exit 0. Starting macos-ci-check monitor for the 3 macOS nodes.

[2026-11-18T12:53:04Z · bob-cli-n7.2] Follow-up check: macos-ci-check monitor 2zdrzg still staged with no output at inspection (pid null, not launched); no GitHub run covers this dirty tree, so no macOS evidence yet. Focused tests re-verified green on current tree (3 note_catalog lib tests, note_goto shape test) and just check exit 0 from this tree stands. Leaving bead open per phase close criterion (3 nodes must pass on macos-latest); submitting intermediate declaration with keep.

## Dependencies

- **Depends on:** [bob-cli-n7.1](bob-cli-n7.1.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-n7.3](bob-cli-n7.3.md) ◐ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n7.2.md) | [bob-cli-n7.2](bob-cli-n7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1f6cc7b`](https://github.com/bobs-org/bob-cli/commit/1f6cc7bedbeb6786202d9e003dad3b1cbccd4911) | fix(note-catalog): canonicalize library roots for symlinked vaults | [bob-cli-n7.2](bob-cli-n7.2.md) | 2026-11-18 07:55:27 EST |
