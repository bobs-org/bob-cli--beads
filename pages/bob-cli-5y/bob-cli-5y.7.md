# Bead: bob-cli-5y.7 — Scan writes reading tasks into parent notes

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.7

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.7` · **Size:** large
**Created:** 2026-10-09 12:29:34 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

ref-sync-v2: births insert the v2 line into the parent's Tasks section, ref notes carry the managed embed, status syncs to the located line across files, and annotation follow-ups go to the parent.

## Notes

[2026-10-09T19:04:21Z · bob-cli-5y.7] PROPOSED FOLLOW-UP: Record the ref-tasks-live-with-their-parent decision after the epic lands — the final memory_ref_parent_decision=no decision forbids editing that memory strand in this phase.

[2026-10-09T19:04:27Z · bob-cli-5y.7] PROPOSED FOLLOW-UP: Update reference-task, reference-note, and area-note glossary strands after the epic lands — their current definitions describe in-note ^ref trackers; memory_glossary_ref_terms=no forbids editing them in this phase.

[2026-10-09T19:16:36Z · bob-cli-5y.7] Section 1 implemented: ref_tasks/line.rs now exposes render_ref_task_line, allocate_ref_block_id, managed_embed_line, sanitize_title_alias, slug_ref_stem, stamp_close_date_any_id (generalized to any trailing ^id, BOB_NOW honored); ref_tasks/insert.rs adds insert_ref_task(bob_dir: &Path, destination: &Path, line: &str, children: &[String]) -> Result<InsertedRefTask { block_id, placement: capture::Placement, task_line }, String> using insert_task_line + write_staged_files with 3-attempt preimage retry, archive-aware allocation, CRLF preservation, missing-inbox creation. Durable tests in ref_tasks/tests.rs cover sanitization/truncation/slug/empty/length/collisions/archive/CRLF/closed-at-birth. cargo test --lib ref_tasks: 24 passed. Pre-existing failure: doctor_reports_ref_tasks_and_parents_rows fails identically on clean base (recorded, not caused here). Remaining: sections 2-5 (index-backed planning, v1/v2/birth/reopen, residence projection, sequential execution, annotations/output/docs) still open; bead stays in_progress.

## Dependencies

- **Blocks:** [bob-cli-5y.11](bob-cli-5y.11.md) ◐ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.5](bob-cli-5y.5.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.9](bob-cli-5y.9.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5y.7.md) | [bob-cli-5y.7](bob-cli-5y.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4016229`](https://github.com/bobs-org/bob-cli/commit/40162297a54caf743a177d85266a41e8bfe1a838) | feat(ref-tasks): add shared v2 reading-task rendering and guarded insertion | [bob-cli-5y.7](bob-cli-5y.7.md) | 2026-10-09 15:19:22 EDT |
