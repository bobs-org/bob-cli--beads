# Bead: bob-cli-fs.2.1.2 — Pure relation extraction and classification

[Bead Pages](../README.md) / [bob-cli-fs.2.1](bob-cli-fs.2.1.md) / bob-cli-fs.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-fs.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.2.md) · **Assignee:** `bob-cli-fs.2.1.2` · **Size:** medium
**Created:** 2026-11-02 06:30:50 EST · **Closed:** 2026-11-02 07:39:01 EST
**Plan:** [202611/relation\_successor\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_successor_core.md)

## Description

classifier: share reconcile target resolution and implement event, released-state, R1-R7 classification, groups, held rows, and snapshot gates over in-memory inputs.

## Notes

[2026-11-02T12:39:01Z · bob-cli-fs.2.1.2] Shared resolve_relation_entry/resolve_relation_target_path with parity tests (same-note, basename/qualified, ambiguous, archive known/unknown, missing/non-task, self-edge). Reconcile uses the helper; CLI LR14 still passes. classify_relation_successors implements cheap gates, incomplete-snapshot unavailable (no reads), parked-event validation, R1–R7, grouping, held rows, and shared copy over staged source_texts plus a narrow TargetNoteReader — no vault enumeration. Fixture adapter materializes base+overlays into real notes/ledgers; classifier-owned rule vectors SA1–SA13, SA14-P, SA16, SA17, SA19, SA24, SA26, SA28 call production code. Integration SA14/SA15/SA18/SA20/SA21 skipped with explicit reasons. Coverage assertion rejects unknown JSON keys. Independent regressions: gates/read counts, incomplete snapshot, staged edge removal, missing source IDs, Next-before-Ready, R6 Done/Cancelled/Parked vs Ready, unread resolved target, previous-daily gap, R4 recovered overlay, KM31. just fmt, just lint, and relation/reconcile tests passed. No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-fs.2.1.1](bob-cli-fs.2.1.1.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fs.2.1.3](bob-cli-fs.2.1.3.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.2/README.md) | [bob-cli-fs.2.1.2](bob-cli-fs.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ace86f8`](https://github.com/bobs-org/bob-cli/commit/ace86f8e5d7fc9c2103e7513953548b119b6629c) | feat(task-relations): add pure relation-successor classifier | [bob-cli-fs.2.1.2](bob-cli-fs.2.1.2.md) | 2026-11-02 07:39:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fs.2.1.2][1] | Need notes for leftover work | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.2/README.md

<!-- sase:referenced-by:end -->
