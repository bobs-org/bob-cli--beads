# Bead: bob-cli-mr.3.1.2 — Apply prepared scans inside a bounded mutation window

[Bead Pages](../README.md) / [bob-cli-mr.3.1](bob-cli-mr.3.1.md) / bob-cli-mr.3.1.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-mr.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.md) · **Assignee:** `bob-cli-mr.3.1.2` · **Size:** medium
**Created:** 2026-11-17 12:14:07 EST
**Plan:** [202611/highlights\_scan\_lock\_window.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/highlights_scan_lock_window.md)

## Description

locked-apply: move full-library planning and hooks outside the locks, validate before mutation, preserve protected intake and recovery, and make no-work scans finish without either lock in human and JSON modes.

## Notes

[2026-11-17T18:58:11Z · bob-cli-mr.3.1.2] PROPOSED FOLLOW-UP: just docs-check fails generated drift on docs/develop/decisions.md on the clean base tree (run just docs-gen); this phase did not touch docs.

[2026-11-17T18:58:31Z · bob-cli-mr.3.1.2] Verified lock-free no-work human+JSON (held locks, unchanged receipt), nested writing scan lock_busy/hook_failed, recovery receipt surviving empty-lib no-work, output_collision prelock without receipt, note-only PDF hash MarkerChanged hold, TextBundle intake evidence. Suites: 1066 highlights_ref unit; 119 scan*; 6 marker_write CLI; 7 ingest; 81 overwrite*.

[2026-11-17T19:24:14Z · bob-cli-mr.3.1.2--1] just check failed on highlights_ref_task_checked_dry_run_requires_and_writes_pdf_marker: lock-free no-work duplicated plan-time failures as write failures. unchanged_write_outcomes_for now emits Planned-only write outcomes. Re-ran that CLI test, highlights_ref_task_ready_scan_reopens_read_ref_to_ready, highlights_ref_scan_writes_valid_pdfs_despite_invalid_pdf, and scan_plan unit tests (9).

## Dependencies

- **Depends on:** [bob-cli-mr.3.1.1](bob-cli-mr.3.1.1.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-mr.3.1.3](bob-cli-mr.3.1.3.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mr.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.1.2.md) | [bob-cli-mr.3.1.2](bob-cli-mr.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3236cee`](https://github.com/bobs-org/bob-cli/commit/3236ceefaa690c2c9aa8d935db0de7b1a2c11ce1) | feat(scan): apply prepared full scans inside a bounded lock window | [bob-cli-mr.3.1.2](bob-cli-mr.3.1.2.md) | 2026-11-17 14:53:36 EST |
