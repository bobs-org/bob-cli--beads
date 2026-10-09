# Bead: bob-cli-62.2 — Execute reading-task writes safely across files

[Bead Pages](../README.md) / [bob-cli-62](README.md) / bob-cli-62.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z7.md) · **Assignee:** `bob-cli-62.2` · **Size:** medium
**Created:** 2026-10-09 15:45:03 EDT · **Closed:** 2026-10-09 16:31:57 EDT
**Plan:** [202610/finish\_ref\_sync\_parent\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/finish_ref_sync_parent_tasks.md)

## Description

v2-execution: implement guarded insertion, adoption, line edits, and archive reopen execution before PDF/ref-note writes, preserving destination edits.

## Notes

[2026-10-09T20:31:43Z · bob-cli-62.2] v2-execution implemented (no scan wiring; for bob-cli-62.3): ref_tasks/edit.rs with edit_reading_task_checkbox + locate_original_line (planned-index else unique-line, READING_TASK_CHANGED=reread-gated "reading task changed during sync; rerun", checkbox+close-stamp-only flips, CRLF preserved, preimage-checked writer with 3 bounded retries, no git-dirty veto); insert.rs adds insert_ref_task_with_preferred_id (old ID reused when free incl. archive, else <old>-2; 4-arg API unchanged) and audits archive lookup (vault-relative default done/<stem>_done.md so absolute vault-root destinations consult their archive; non-NotFound archive read errors propagate); line.rs refactors shared allocate_unique_block_id. highlights_ref/reading_execute.rs consumes ReadingTaskPlan actions: ReadingTaskExecution {destination, block_id, task_line, action Inserted|LineEdited}, execute_reading_insert (renders via render_ref_task_line, warning child indented), execute_reading_line_edit (refuses archived done/), revalidate_located_task (refreshes moved index/mark/ID, fails stale before any embed/parent write), v2_dirty_note_allowed + frontmatter_change_is_residence_only + v2_body_change_confined_to_managed_embed (v1 guard untouched). Mandated per-PDF order (destination/routed inserts, then authorized marker, then ref note) and rerun-adoption documented in module docs. 20 new tests: 11 in ref_tasks (moved/deleted/changed/duplicate lines, CRLF, stamp preservation, unrelated-addition survival, preferred-ID reuse/suffix, archive collision + error propagation), 9 in highlights_ref/tests/reading_execute.rs (birth-then-rerun-adopts via rebuilt RefTaskIndex, reopen into sase/inbox with warning child, edit+revalidate ordering, archive refusal, changed-line-fails-before-ref-write, v2 guard allow/refuse incl. v1-tracker non-weakening). Verified: cargo test --lib 2130 passed; highlights_ref 301 passed; ref_tasks 35 passed; cli highlights 222 passed; cli ref_ 205 passed + 1 pre-existing doctor failure (see follow-up); cargo fmt --check clean; cargo clippy --all-targets --all-features exit 0 (only awaiting-wiring/unused-reexport warnings, same class as prior phase).

[2026-10-09T20:31:49Z · bob-cli-62.2] PROPOSED FOLLOW-UP: doctor_reports_ref_tasks_and_parents_rows still fails with `library directory does not exist or is not a directory: <vault>/lib` — same signature as the clean-base baseline recorded in bob-cli-62.1 note 2 (proven byte-identical on HEAD 4cc1281) and bob-cli-5y.7 note 3; unrelated to v2-execution, no product change made.

[2026-10-09T20:31:57Z · bob-cli-62.2] v2-execution done and verified: guarded inserts with preferred reopen IDs, exact line edits with reread validation, archive-aware allocation, task revalidation, and v2 ref-note guard predicates, all scan-unwired for bob-cli-62.3. cargo test --lib 2130 passed, cli highlights 222 passed, cli ref_ 205 passed, fmt clean, clippy exit 0. Only failure is doctor_reports_ref_tasks_and_parents_rows, same pre-existing missing-fixture-lib signature as the clean-base baseline (recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Depends on:** [bob-cli-62.1](bob-cli-62.1.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-62.3](bob-cli-62.3.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-62.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-62.2/README.md) | [bob-cli-62.2](bob-cli-62.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4bfacc3`](https://github.com/bobs-org/bob-cli/commit/4bfacc320cab9995a09351a56ce2ab434da4d6a8) | feat(highlights-ref): execute v2 reading-task writes with guarded cross-file edits | [bob-cli-62.2](bob-cli-62.2.md) | 2026-10-09 16:33:06 EDT |
