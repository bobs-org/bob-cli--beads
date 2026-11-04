# Bead: bob-cli-go.10.1.3 — Staged transfer moves and shared result fields

[Bead Pages](../README.md) / [bob-cli-go.10.1](bob-cli-go.10.1.md) / bob-cli-go.10.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-go.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.10.md) · **Assignee:** `bob-cli-go.10.1.3` · **Size:** medium
**Created:** 2026-11-04 01:50:45 EST · **Closed:** 2026-11-04 04:05:58 EST
**Plan:** [202611/capture\_transfer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_transfer.md)

## Description

transfer-moves: resolve and validate transfer identities, execute bare-note destinations through batch_move, and report moves and repairs with human output. Preserve atomic draft planning, link relocation, freshness, and dry-run parity.

## Notes

[2026-11-04T09:05:34Z · bob-cli-go.10.1.3] PROPOSED FOLLOW-UP: Clean-base HEAD 706eab67 does not compile (MergeContext missing successor_labels in relations_merge.rs and task_merge/command.rs) — fixed minimally here to verify; land agent should confirm or split the wiring

[2026-11-04T09:05:40Z · bob-cli-go.10.1.3] PROPOSED FOLLOW-UP: capture::r#ref::capture_bracketed_url_queues_without_brackets fails — transfer lexer claims <https://example.com/post> with transfer_arrow_spacing instead of Ref; needs lexer-phase fix

[2026-11-04T09:05:45Z · bob-cli-go.10.1.3] PROPOSED FOLLOW-UP: 5 lib parse tests fail (grammar::execution_parses_equals_family, ref_grammar claim/editor/percent_l, target_runs::terminal_extraction) in files untouched by transfer-moves; likely lexer/expectation drift for land-agent triage

[2026-11-04T09:05:58Z · bob-cli-go.10.1.3] transfer-moves done: new capture/transfer.rs resolves identities against staged snapshots (NoteIndex, no path assumption), preflights resolved duplicates/overlaps, moves each source via apply_batch_move in typed order with freshness/link repair, reports moves[]+repaired_files[] sharing the task-move wire shape and human Moved/repair rows; merges keep transfer_execution_unavailable. Verified: 11 transfer CLI tests + parse contract pass; relations_merge/project_note/task_move+merge/parse/capture-lib suites green; fmt clean; clippy gate passes; epic-symbols empty. Pre-existing base break (MergeContext successor_labels) fixed minimally to verify; 1 CLI + 5 lib failures recorded as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-go.10.1.2](bob-cli-go.10.1.2.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-go.10.1.4](bob-cli-go.10.1.4.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.10.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.3/README.md) | [bob-cli-go.10.1.3](bob-cli-go.10.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b9fe9d0`](https://github.com/bobs-org/bob-cli/commit/b9fe9d0c1208ca4a4670c6e886060621116b6286) | feat(capture): implement transfer-moves planner with typed batch moves | [bob-cli-go.10.1.3](bob-cli-go.10.1.3.md) | 2026-11-04 04:07:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.10.1.3][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-go.10.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.land/README.md

<!-- sase:referenced-by:end -->
