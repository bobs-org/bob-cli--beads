# Bead: bob-cli-gj.2.1.1 — Note-pull grammar and single-item planner

[Bead Pages](../README.md) / [bob-cli-gj.2.1](bob-cli-gj.2.1.md) / bob-cli-gj.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-gj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.2.md) · **Assignee:** `bob-cli-gj.2.1.1` · **Size:** medium
**Created:** 2026-11-03 12:31:13 EST · **Closed:** 2026-11-03 14:12:10 EST
**Plan:** [202611/note\_pull\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_pull_cli.md)

## Description

core: implement sections 3 and 4, including the lone-header grammar and editor mode, staged note-pull planner, classification, placement, explicit picks, refusals, additive result model, and shared offer traversal. Cover the single-item NP vectors and parser regressions. Read section 2 constraints.

## Notes

[2026-11-03T19:12:10Z · bob-cli-gj.2.1.1] Core note-pull grammar and single-item planner done and verified. Grammar: CaptureKind::NotePull for lone @route headers (count==0, Tasks kind, no section), EditorMode::NotePull with needs [] and preserved list metadata, GRAMMAR_REVISION 7 with feat(capture!:) + BREAKING CHANGE footer left to the land agent (no commit made, no version/CHANGELOG/memory edits). Planner (src/native/capture/note_pull.rs): staged classification with NP5 precedence, KM31 dependents-snapshot gate (no snapshot for dependency-free pulls), Pending-Next-Ready then line order, §12.2 keys frozen pre-pick, sequential scratch vs picks-only actual placement, Ready->Next + mint + stamp_fresh writes, refused pull_note_missing/nothing_to_pull_in with additive payloads, rows in all_offer_rows/numbering/completion counts with trigger note_pull and group note_pull, TaskBlockRole::NotePull. Tests: 22 planner tests pin NP1-NP12, NP15, NP21-23 (incl. file-byte assertions for picks/refusals, blocked-project reasons, KM31 unavailable-proof unit, daily-note errors); lists/editor/capture-parse/CLI suites pin NP24-27 and grammar 7. just check and just docs-check both green.

## Dependencies

- **Blocks:** [bob-cli-gj.2.1.2](bob-cli-gj.2.1.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gj.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gj.2.1.1/README.md) | [bob-cli-gj.2.1.1](bob-cli-gj.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c673d14`](https://github.com/bobs-org/bob-cli/commit/c673d14439212e79443d231c81dc11204d10a25c) | feat(capture!): lone @route pulls its note's ready tasks | [bob-cli-gj.2.1.1](bob-cli-gj.2.1.1.md) | 2026-11-03 14:13:21 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gj.2.1.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gj.2.1.1/README.md

<!-- sase:referenced-by:end -->
