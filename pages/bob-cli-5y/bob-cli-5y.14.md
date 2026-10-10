# Bead: bob-cli-5y.14 — Retire the transitional bypass, docs coherence, memory, final report

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.14

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.14` · **Size:** medium
**Created:** 2026-10-09 12:29:35 EDT · **Closed:** 2026-10-09 22:14:43 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

closeout: remove the transitional hidden ^ref review bypass, read the docs end to end, apply the accepted memory decisions, and leave Bryan the verification checklist.

## Notes

[2026-10-10T02:11:54Z · bob-cli-5y.14] PROPOSED FOLLOW-UP: Add decisions strand recording that ref tasks live with their parent note (epic auto-decision memory_ref_parent_decision=no skipped it)

[2026-10-10T02:11:57Z · bob-cli-5y.14] PROPOSED FOLLOW-UP: Update glossary reference-task, reference-note, and area-note strands for the parent-residence model (epic auto-decision memory_glossary_ref_terms=no skipped it)

[2026-10-10T02:12:01Z · bob-cli-5y.14] PROPOSED FOLLOW-UP: Verify bob-ledger-tools freshness mirror dropped the exact-^ref #hide bypass to match the Rust closeout (docs/freshness.md is the shared contract; only the Rust side was changed here)

[2026-10-10T02:14:43Z · bob-cli-5y.14] Closeout done. Bypass removed: scan.rs no longer collects hidden exact-^ref rows (Snapshot.trackers field, collection block, and tracker_candidate_visible deleted), cli.rs review input is ready/pending/next plus checklist only, state/scan/cli docs updated; a #hide tag now hides exact-^ref rows like any task (schema stays 12, JSON shape unchanged). Tests updated to the post-closeout contract: hidden ^ref stays out, visible ^ref still walks REFERENCES (incl. renamed list_hidden_reference_stays_out_while_visible_walks). Docs read end to end: freshness.md fixed in 6 spots plus a 2026-10-10 changelog entry; highlights-ref-sync.md v1 tracker paragraph qualified; other ref docs already coherent. Memory: no edits per the epic no/no decisions; cancel_dropped_wrapper_refs=no implemented as no action. Three PROPOSED FOLLOW-UPs recorded (decisions strand, glossary strands, ledger-mirror parity check). Verified: just check green (fmt, clippy, 2159 lib + 1334 cli + all other suites, 0 failed); epic-symbols clean. Bryan checklist: reinstall bob from this checkout, run bob freshness list on the live vault and confirm no hidden ^ref row walks, confirm schema_version 12, then handle the three follow-ups.

## Dependencies

- **Depends on:** [bob-cli-5y.12](bob-cli-5y.12.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.13](bob-cli-5y.13.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.14](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.14/README.md) | [bob-cli-5y.14](bob-cli-5y.14.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f315c58`](https://github.com/bobs-org/bob-cli/commit/f315c58c70dfe16fadb6052457250e670efe3c28) | feat(freshness): remove hidden ^ref review bypass and close out post-closeout contract | [bob-cli-5y.14](bob-cli-5y.14.md) | 2026-10-09 22:16:25 EDT |
