# Bead: bob-cli-3n.3 — R1-R10 reconciliation in bob task-status-hooks

[Bead Pages](../README.md) / [bob-cli-3n](README.md) / bob-cli-3n.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vl.md) · **Assignee:** `bob-cli-3n.3` · **Size:** medium
**Created:** 2026-10-02 16:54:35 EDT
**Plan:** [202610/task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links.md)

## Description

hooks-reconcile: before Blocked derivation, project Depends-On lines into the dependsOn/id fields and adopt, heal, canonicalize, and warn. Projection-only notes are written through the guarded pipeline and quiet interval. Add JSON and human output, docs, and tests, then verify with a read-only dry run against the vault.

## Notes

[2026-10-03T00:14:57Z · bob-cli-3n.3] PROPOSED FOLLOW-UP: lib test native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes flakes under default test parallelism (fails ~1/3 runs on the clean base tree too); test with_env helpers mutate process-global env vars with no lock, so parallel tests race (also seen once in note_ready::scan_excludes_r3_and_r7_paths)

## Dependencies

- **Depends on:** [bob-cli-3n.2](bob-cli-3n.2.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.9](bob-cli-3n.9.md) ◐ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.3/README.md) | [bob-cli-3n.3](bob-cli-3n.3.md) | 0 |
