# Bead: bob-cli-go.2 — Fragment transplant, task-children classifier, drawer ensure, and task locators

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.2` · **Size:** medium
**Created:** 2026-11-03 16:11:30 EST · **Closed:** 2026-11-03 18:03:39 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

foundation: extract the move engine's fragment cut, re-indent, anchor-rename, and vault-wide link-repair machinery into a reusable transplant API, rebuild plan_task_move on it unchanged, and add a shared task-children classifier, a find-or-create drawer helper, and the note:block-id task locator.

## Notes

[2026-11-03T23:03:39Z · bob-cli-go.2--4] Transplant API, task-children classifier, drawer ensure helper, and note:block-id locator implemented with plan_task_move rebuilt on shared path. just fmt clean; just lint && just test passed exit 0 (monitor hhcwr8q0q630); epic-symbols clean. Authorized glossary strands task-merge/task-split added plus task-relation update.

## Dependencies

- **Blocks:** [bob-cli-go.3](bob-cli-go.3.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.4](bob-cli-go.4.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.2.md) | [bob-cli-go.2](bob-cli-go.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`aac3947`](https://github.com/bobs-org/bob-cli/commit/aac3947c7f415b7037fdb7e10fa5e0322df4ade3) | feat(task-move): shared transplant API, children classifier, drawer ensure, task locator | [bob-cli-go.2](bob-cli-go.2.md) | 2026-11-03 18:04:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.2--4][1] | Need phase scope and design before symbol check and close | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.2.md

<!-- sase:referenced-by:end -->
