# Bead: bob-cli-pq.2 — Bob annotates requirement lines in previews and the idle agenda

[Bead Pages](../README.md) / [bob-cli-pq](README.md) / bob-cli-pq.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1f8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1f8.md) · **Assignee:** `bob-cli-pq.2` · **Size:** medium
**Created:** 2026-11-23 03:54:18 EST · **Closed:** 2026-11-23 04:58:07 EST
**Plan:** [202611/task\_reqs\_criterion\_diamond.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_reqs_criterion_diamond.md)

## Description

line-annotations: an additive `req: {depth, state}` object on capture preview block lines and idle-agenda lines, computed by the recognizer, so the Mac can draw the diamond without inferring anything from `[ ]`.

## Notes

[2026-11-23T09:57:55Z · bob-cli-pq.2] PROPOSED FOLLOW-UP: skipped decisions:requirements-wear-the-criterion-diamond — epic decision memory_req_mark_record=no, so line-annotations did not add that record; memory phase / land agent may still file it if the later accepted set changes

[2026-11-23T09:58:07Z · bob-cli-pq.2] Additive req:{depth,state} on BlockLineJson and AgendaLine from the recognizer. Verified: unit tests annotate_req_lines_* (after snapshot except removed; notes/drawers omitted; dropped/carried/excluded/moot) and EffectiveReqState::as_str; CLI capture::req_annotations (created-parent depths 1-3, complete→met, dropped/carried/excluded, idle agenda); cargo clippy with just-check gates; cargo fmt --check; just docs-gen and just docs-check. No leftover --epic-symbol entries. JSON is skip_serializing_if none so unrelated output stays byte-identical.

## Dependencies

- **Depends on:** [bob-cli-pq.1](bob-cli-pq.1.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pq.6](bob-cli-pq.6.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pq.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pq.2.md) | [bob-cli-pq.2](bob-cli-pq.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`87ee683`](https://github.com/bobs-org/bob-cli/commit/87ee683ae7ed698db10e79c892d2be109a45d737) | feat(task-reqs): annotate preview and agenda lines with req depth and state | [bob-cli-pq.2](bob-cli-pq.2.md) | 2026-11-23 05:10:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |
| read-by | [agent:bob-cli-pq.2--1][2] | Need phase scope, status, notes, and whether work already closed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.1fk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pq.2.md

<!-- sase:referenced-by:end -->
