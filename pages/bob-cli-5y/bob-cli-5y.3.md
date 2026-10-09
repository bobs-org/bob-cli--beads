# Bead: bob-cli-5y.3 — Freshness keys refs on the #ref tag, with the lane split

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.3` · **Size:** medium
**Created:** 2026-10-09 12:29:34 EDT · **Closed:** 2026-10-09 12:55:34 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

freshness-rekey: re-key ref review identity from the ^ref block ID to the #ref tag in Rust and bob-ledger-tools; Ready refs keep REFERENCES while Next/Pending refs walk their lanes.

## Notes

[2026-10-09T16:55:16Z · bob-cli-5y.3] PROPOSED FOLLOW-UP: Add decisions strand ref-tasks-live-with-their-parent recording that ref tasks live with their parent note (skipped per epic memory_ref_parent_decision=no)

[2026-10-09T16:55:21Z · bob-cli-5y.3] PROPOSED FOLLOW-UP: Update glossary strands reference-task, reference-note, area-note for the parent-resident ref model (skipped per epic memory_glossary_ref_terms=no)

[2026-10-09T16:55:25Z · bob-cli-5y.3] PROPOSED FOLLOW-UP: Fix 2 pre-existing test-navigation-roll-decay.cjs failures (picker-single Ctrl+Enter P2 roll expects [?] got [ ]); reproduces identically on the clean base tree without freshness-rekey changes

[2026-10-09T16:55:34Z · bob-cli-5y.3] freshness-rekey done: Rust TrackerKind re-keyed to #ref tag/exact ^ref with Ready-only REFERENCES + lane refs as ordinary lane rows, schema 12; ledger-tools mirrored with api v10 + refTagIdentity (manifest 1.37.0, built + synced); docs/freshness.md updated; just check green; focused suites green (tracking/recurring/namespace/nav-freshness 114 pass); npm test 2234/2236 with 2 pre-existing roll-decay failures reproduced on clean base (noted as follow-up)

## Dependencies

- **Blocks:** [bob-cli-5y.13](bob-cli-5y.13.md) ◐ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.6](bob-cli-5y.6.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.3/README.md) | [bob-cli-5y.3](bob-cli-5y.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e04c421`](https://github.com/bobs-org/bob-cli/commit/e04c42156c22ea8ed24091249176f3d124517b93) | feat(freshness): re-key ref review identity to the #ref tag with the lane split | [bob-cli-5y.3](bob-cli-5y.3.md) | 2026-10-09 12:57:31 EDT |
| bob-plugins | [`bob-plugins@947615d`](https://github.com/bobs-org/bob-plugins/commit/947615d8e28871f7144dc859d1f740dcbcc10189) | feat(ledger-tools): mirror the #ref tag identity with the Ready/lane split | [bob-cli-5y.3](bob-cli-5y.3.md) | 2026-10-09 12:58:23 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5y.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.3/README.md

<!-- sase:referenced-by:end -->
