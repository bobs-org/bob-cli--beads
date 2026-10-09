# Bead: bob-cli-5y.7 — Scan writes reading tasks into parent notes

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.7` · **Size:** large
**Created:** 2026-10-09 12:29:34 EDT · **Closed:** 2026-10-09 19:03:14 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

ref-sync-v2: births insert the v2 line into the parent's Tasks section, ref notes carry the managed embed, status syncs to the located line across files, and annotation follow-ups go to the parent.

## Notes

[2026-10-09T19:04:21Z · bob-cli-5y.7] PROPOSED FOLLOW-UP: Record the ref-tasks-live-with-their-parent decision after the epic lands — the final memory_ref_parent_decision=no decision forbids editing that memory strand in this phase.

[2026-10-09T19:04:27Z · bob-cli-5y.7] PROPOSED FOLLOW-UP: Update reference-task, reference-note, and area-note glossary strands after the epic lands — their current definitions describe in-note ^ref trackers; memory_glossary_ref_terms=no forbids editing them in this phase.

[2026-10-09T19:16:36Z · bob-cli-5y.7] Section 1 implemented: ref_tasks/line.rs now exposes render_ref_task_line, allocate_ref_block_id, managed_embed_line, sanitize_title_alias, slug_ref_stem, stamp_close_date_any_id (generalized to any trailing ^id, BOB_NOW honored); ref_tasks/insert.rs adds insert_ref_task(bob_dir: &Path, destination: &Path, line: &str, children: &[String]) -> Result<InsertedRefTask { block_id, placement: capture::Placement, task_line }, String> using insert_task_line + write_staged_files with 3-attempt preimage retry, archive-aware allocation, CRLF preservation, missing-inbox creation. Durable tests in ref_tasks/tests.rs cover sanitization/truncation/slug/empty/length/collisions/archive/CRLF/closed-at-birth. cargo test --lib ref_tasks: 24 passed. Pre-existing failure: doctor_reports_ref_tasks_and_parents_rows fails identically on clean base (recorded, not caused here). Remaining: sections 2-5 (index-backed planning, v1/v2/birth/reopen, residence projection, sequential execution, annotations/output/docs) still open; bead stays in_progress.

[2026-10-09T23:03:14Z · bob-cli-62.land--1] ref-sync-v2 complete via epic bob-cli-62 (closed) implementing plan:202610/finish_ref_sync_parent_tasks.md plus landing repairs. Births: ref_tasks/insert.rs insert_ref_task(bob_dir,destination,line,children)->InsertedRefTask{block_id,placement,task_line} preserved plus additive insert_ref_task_with_preferred_id for reopen ID reuse, executed via highlights_ref/reading_execute.rs execute_reading_insert with StagedTextFile 3-attempt preimage retries and post-success dedup commit; verified by CRLF/archive-collision/preferred-ID tests and rerun-adopts integration. Managed embed: ref_tasks/embed.rs find_managed_embed restricted to H1 slot, reading_plan.rs heal_managed_embed plus v2_birth_body, audio.rs maybe_insert_audio_embed_after_managed wired into Insert route; later authored embeds preserved, region errors propagate. Status sync: reading_plan.rs plan_reading_task with v2_task_status_signal plus semantic parent-free opt-in refusal in sync.rs plan_pdf_sync_v2, ref_tasks/edit.rs edit_reading_task_checkbox (quote-prefix stripping, byte-preserving splice_line) via execute_reading_line_edit plus revalidate_located_task; refuse_status_parent_writes fails per-PDF with reading_diagnostic lines in human/single-PDF/verbose reports; ambiguity leaves bytes unchanged. Annotation follow-ups: rebased routed intentions with per-PDF ownership and run-level dedup to residence/mac_inbox, archive-move dedup covered by new scan_integration test. Verification: monitor eqt68nqb920y just check COMPLETED exit 0 2026-10-09T22:58Z; focused ref_tasks 38, highlights_ref 303, scan_integration 29, doctor_reports_ref_tasks_and_parents_rows and pomodoros_agenda 9 passed. Skipped-memory follow-ups (notes 1-2) left for outer epic 5y lander per plan; epic-symbols empty.

## Dependencies

- **Blocks:** [bob-cli-5y.11](bob-cli-5y.11.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.5](bob-cli-5y.5.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.9](bob-cli-5y.9.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5y.7.md) | [bob-cli-5y.7](bob-cli-5y.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4016229`](https://github.com/bobs-org/bob-cli/commit/40162297a54caf743a177d85266a41e8bfe1a838) | feat(ref-tasks): add shared v2 reading-task rendering and guarded insertion | [bob-cli-5y.7](bob-cli-5y.7.md) | 2026-10-09 15:19:22 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-62.1][1] | Need remaining scope and latest completion evidence | 1 |
| read-by | [agent:bob-cli-62.land--1][2] | landing re-read for close | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-62.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-62.land.md

<!-- sase:referenced-by:end -->
