# Bead: bob-cli-87.3.1.1 — Source-aware Bob task rows and relationship metadata

[Bead Pages](../README.md) / [bob-cli-87.3.1](bob-cli-87.3.1.md) / bob-cli-87.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.3.md) · **Assignee:** `bob-cli-87.3.1.1` · **Size:** medium
**Created:** 2026-10-16 11:43:18 EDT · **Closed:** 2026-10-16 12:11:29 EDT
**Plan:** [202610/snapshot\_bob\_layer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_bob_layer.md)

## Description

task-rows: add the Bob projection context and source attribution through the existing Obsidian/transclusion pipeline; implement task chips and BLOCKS, WAITS ON, and Sub-projects rows using shared parsers, with focused source and nesting tests.

## Notes

[2026-10-16T16:11:15Z · bob-cli-87.3.1.1] PROPOSED FOLLOW-UP: full lib suite shows the same 2 clean-base failures (completion kinds decision + native command canonical path, both capture-templates registry gaps assigned to bob-cli-8b); reproduced identically on stashed base, no action for this phase

[2026-10-16T16:11:29Z · bob-cli-87.3.1.1] task-rows done: TaskSource attribution on SnapshotTask/ListItem, new note_snapshot/bob.rs with BobTaskContext date, chips (sched/priority/repeat/ref, code-span safe, past+malformed retained), Waits on/Blocks/Sub-projects LabeledRows reusing resolved Note › task labels with done/canceled chips, Bob-kind gated in project_snapshot via snapshot_date option; 20 new bob tests + all 110 note_snapshot tests green, projects/helpers suites green, zero new clippy/fmt drift; full lib has only the 2 pre-existing clean-base capture-templates failures tracked by bob-cli-8b

## Dependencies

- **Blocks:** [bob-cli-87.3.1.2](bob-cli-87.3.1.2.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.3.1.1/README.md) | [bob-cli-87.3.1.1](bob-cli-87.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`57c3df2`](https://github.com/bobs-org/bob-cli/commit/57c3df2a87a5b8da8b29bc146e0fb2699a5241f2) | feat(snapshot): add source-aware Bob task rows and relationship metadata | [bob-cli-87.3.1.1](bob-cli-87.3.1.1.md) | 2026-10-16 12:17:45 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.3.1.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.3.1.1/README.md

<!-- sase:referenced-by:end -->
