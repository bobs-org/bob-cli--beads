# Bead: bob-cli-gl.5.1.1 — Execute ordered parent moves with atomic batch safety

[Bead Pages](../README.md) / [bob-cli-gl.5.1](bob-cli-gl.5.1.md) / bob-cli-gl.5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-gl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.md) · **Assignee:** `bob-cli-gl.5.1.1` · **Size:** medium
**Created:** 2026-11-03 16:14:53 EST · **Closed:** 2026-11-03 17:43:58 EST
**Plan:** [202611/capture\_move\_execution.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_execution.md)

## Description

move_execution: Resolve caret moves against staged parents, render task slots, execute one batch move per item, emit move JSON, and enforce all vault refusals. Correct chained destination-before-source ordering and cover the move-only MV vectors.

## Notes

[2026-11-03T22:43:58Z · bob-cli-gl.5.1.1--2] Implemented ordered caret moves for project-note capture with atomic batch execution, destination-before-source ordering, moved-task reporting, typed refusals, and rollback coverage. Focused project-note/task-move/inbox-route regressions passed; required just check passed (exit 0). epic-symbols reported no remaining entries.

## Dependencies

- **Blocks:** [bob-cli-gl.5.1.2](bob-cli-gl.5.1.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.1.md) | [bob-cli-gl.5.1.1](bob-cli-gl.5.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6650faa`](https://github.com/bobs-org/bob-cli/commit/6650faa30491c8f7f39c2657bdbe8676ec97c6f6) | feat(capture): execute ordered project-note moves | [bob-cli-gl.5.1.1](bob-cli-gl.5.1.1.md) | 2026-11-03 17:45:01 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.5.1.1--2][1] | Confirm phase scope, DECISIONS, prior notes, and design before closure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.1.md

<!-- sase:referenced-by:end -->
