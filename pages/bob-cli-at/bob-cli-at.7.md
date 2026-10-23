# Bead: bob-cli-at.7 — Acceptance kit, docs consolidation, decision record, and follow-ups

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.7` · **Size:** medium
**Created:** 2026-10-23 11:44:16 EDT · **Closed:** 2026-10-23 16:16:42 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

accept: add `scripts/dev/highlights_coordination_acceptance`, a guided, colored, interactive runbook for the Mac. It works in a throwaway vault and config under `$TMPDIR` (never `~/bob` or the real config), covers the research's nine steps, and records `results.md` plus a verdict with the exact enable line. It also has a non-GUI `--self-test` wired into `just check-scripts`. Consolidate the "PDFs open in Highlights" docs. Replace both "keep Highlights idle" notes, and add the conflict-dialog troubleshooting row and the enable steps. Write the decisions strand if accepted, then record the proposed follow-ups on this phase bead.

## Notes

[2026-10-23T20:15:18Z · bob-cli-at.7] PROPOSED FOLLOW-UP: Flip the shipped default of highlights.coordinate_pdf_writes to true after the guided Mac acceptance run passes (steps 2, 3, 5, 6) — detail

[2026-10-23T20:15:22Z · bob-cli-at.7] PROPOSED FOLLOW-UP: Coordinate rename/move, id stamp, and create --force through the same bounded .forMerging executor (other atomic_save_pdf callers); the rename card can then drop its Close the PDF in Highlights first warning — detail

[2026-10-23T20:15:26Z · bob-cli-at.7] PROPOSED FOLLOW-UP: Pending-marker refinement — write the note now and the marker later instead of holding the whole per-PDF sequence — detail

[2026-10-23T20:15:30Z · bob-cli-at.7] PROPOSED FOLLOW-UP: Decide whether lifecycle status belongs in the PDF marker at all — detail

[2026-10-23T20:15:39Z · bob-cli-at.7] PROPOSED FOLLOW-UP: Scan-wide dirty_targets refusal caused by one autosaved PDF — consider per-PDF granularity so one dirty PDF does not fail the scan — detail

[2026-10-23T20:15:43Z · bob-cli-at.7] PROPOSED FOLLOW-UP: Cron wrapper success logging and the docs/vault-git-sync.md schedule drift — detail

[2026-10-23T20:15:48Z · bob-cli-at.7] PROPOSED FOLLOW-UP: bob-cli-6h (reading-task landing notifications) can build on the scan receipt channel (<state>/bob-cli/ref/last-scan.json + org.bobs.bob.ref.scan-finished) — detail

[2026-10-23T20:15:52Z · bob-cli-at.7] PROPOSED FOLLOW-UP: Plan B app-driven Apply now — only if the guided acceptance run shows lost annotations or a conflict dialog — detail

[2026-10-23T20:16:42Z · bob-cli-at.7] Accept kit landed: scripts/dev/highlights_coordination_acceptance (9 guided Mac steps + results.md/verdict, --self-test 7/7 green) wired into just check-scripts; docs consolidated (Enabling, Acceptance kit, Mac notification, conflict-dialog row, validation bullet); decisions strand open-pdf-writes-are-coordinated written + memory init republished; 8 PROPOSED FOLLOW-UP notes recorded; epic-symbols clean. Verified: just check-scripts exit 0, just docs-check 447 passed, bash -n clean. No dupes for follow-ups (bob-cli-6h cited for receipt channel).

## Dependencies

- **Depends on:** [bob-cli-at.4](bob-cli-at.4.md) ✓ · ⧖ 2026-10-23
- **Depends on:** [bob-cli-at.6](bob-cli-at.6.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.7/README.md) | [bob-cli-at.7](bob-cli-at.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`134016c`](https://github.com/bobs-org/bob-cli/commit/134016cec23b93c2191c404a812d050f50653833) | feat(highlights): add coordinated PDF writes acceptance kit and docs | [bob-cli-at.7](bob-cli-at.7.md) | 2026-10-23 16:18:23 EDT |
