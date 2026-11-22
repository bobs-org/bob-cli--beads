# Bead: bob-cli-on.8.1.1 — Pre-close requirement groups and snapshot identity

[Bead Pages](../README.md) / [bob-cli-on.8.1](bob-cli-on.8.1.md) / bob-cli-on.8.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.md) · **Assignee:** `bob-cli-on.8.1.1` · **Size:** medium
**Created:** 2026-11-22 07:22:29 EST · **Closed:** 2026-11-22 08:02:07 EST
**Plan:** [202611/requirement\_close\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/requirement_close_engine.md)

## Description

rows: collect each managed closing owner's pre-close requirement forest, implement snapshot-bound row keys and canonical group copy, and establish the RV fixture schema and row-building vectors.

## Notes

[2026-11-22T13:02:07Z · bob-cli-on.8.1.1] Pre-close req groups and snapshot identity: collect_owner/groups_from_owners bind owner.key to sha256 of exact pre-close owner-block bytes; managed Done paths (complete_task_tree, complete_embedded_trees, plan_close_successors, complete_existing_task) attach forests before mutation. RV1–RV11 in tests/fixtures/req_close/vectors.json match the collector. just check green; no --epic-symbol leftovers. pull_in.reqs.supported stays off.

## Dependencies

- **Blocks:** [bob-cli-on.8.1.2](bob-cli-on.8.1.2.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.1/README.md) | [bob-cli-on.8.1.1](bob-cli-on.8.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e4ee55b`](https://github.com/bobs-org/bob-cli/commit/e4ee55bdfe14f6b43ca71d2a3deaace7480b029b) | feat(task-complete): collect pre-close requirement groups and snapshot identity | [bob-cli-on.8.1.1](bob-cli-on.8.1.1.md) | 2026-11-22 08:03:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.8.1.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.1/README.md

<!-- sase:referenced-by:end -->
