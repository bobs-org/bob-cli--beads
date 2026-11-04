# Bead: bob-cli-go.4.1.3 — Compose ledger offers and finish the merge planner contract

[Bead Pages](../README.md) / [bob-cli-go.4.1](bob-cli-go.4.1.md) / bob-cli-go.4.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-go.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.md) · **Assignee:** `bob-cli-go.4.1.3` · **Size:** medium
**Created:** 2026-11-03 18:14:56 EST · **Closed:** 2026-11-03 22:18:47 EST
**Plan:** [202611/task\_merge\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_merge_engine.md)

## Description

integration: complete plan_task_merge with ledger-slot offers, explicit selections, ordered postimages, read-set metadata, MergeRecord serialization and canonical copy. Finish MG1-MG20 coverage and invariant tests using the production reconciliation and archive planners, document the engine, and pass the repository checks.

## Notes

[2026-11-04T02:45:01Z · bob-cli-go.4.1.3] PROPOSED FOLLOW-UP: Restore front matter on the tracked glossary task-merge strand so docs generated-drift validation can run — just docs-check reports that sase/memory/glossary/task-merge.md has no front matter; bob-docs lint passes and this memory path is unchanged in this phase.

[2026-11-04T03:18:25Z · bob-cli-go.4.1.3--4] PROPOSED FOLLOW-UP: Clear baseline Clippy failures in task-move/task-split — clean HEAD and the integration workspace both fail the canonical strict Clippy command on unchanged src/native/task_move/command.rs (useless_format), src/native/task_split/command.rs (collapsible_if), and src/native/task_split/plan.rs (collapsible_if, bool_comparison, collapsible_str_replace).

[2026-11-04T03:18:47Z · bob-cli-go.4.1.3--4] Verified merge suite 34/34, formatting and diff checks clean. The five strict Clippy errors reproduce identically on clean HEAD in unchanged task_move/task_split files; recorded follow-up. docs-check glossary front-matter issue is also recorded. epic-symbols is empty.

## Dependencies

- **Depends on:** [bob-cli-go.4.1.2](bob-cli-go.4.1.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.1.3.md) | [bob-cli-go.4.1.3](bob-cli-go.4.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e253ce1`](https://github.com/bobs-org/bob-cli/commit/e253ce17c96fe2ce485931e841f18c8fbedccf0b) | feat(task-merge): complete planner integration | [bob-cli-go.4.1.3](bob-cli-go.4.1.3.md) | 2026-11-03 22:19:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.5.1.3--1][1] | Check whether the in-progress task-merge planner integration is expected to consume prepare_task_merge | 1 |
| read-by | [agent:bob-cli-go.4.1.3--4][2] | Need the current phase scope, design, and recorded progress before closure | 1 |
| read-by | [agent:bob-cli-go.4.1.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.1.3.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.1.land.md

<!-- sase:referenced-by:end -->
