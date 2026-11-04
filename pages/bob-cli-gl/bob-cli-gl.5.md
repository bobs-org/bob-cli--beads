# Bead: bob-cli-gl.5 — Project-note planner moves, \`:\` links, offers, and output

[Bead Pages](../README.md) / [bob-cli-gl](README.md) / bob-cli-gl.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.35.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.35.linker.w0.md) · **Assignee:** `bob-cli-gl.5` · **Size:** large
**Created:** 2026-11-03 13:39:31 EST · **Closed:** 2026-11-03 21:26:52 EST
**Plan:** [202611/capture\_move\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_bullets.md)

## Description

cli-execution: Execute `- ^id` and `- :id` inside `plan_project_note_item`: resolve against the staged parent, apply vault refusals, render ordered slots, move through the batch move helper, stamp, link `:` moves through the existing-task link semantics in draft order, integrate offers (`moved_from`), and report `project_note.moved_tasks`, the move summary and move hint, plus human output. Remove the interim refusal, rewrite the `bob capture` help, and land the MV vectors as tests.

## Dependencies

- **Depends on:** [bob-cli-gl.2](bob-cli-gl.2.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-gl.3](bob-cli-gl.3.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.7](bob-cli-gl.7.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.md) | [bob-cli-gl.5](bob-cli-gl.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.3][1] | Coordinate the shared eligibility and batch-move engine interfaces with dependent phases | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.3/README.md

<!-- sase:referenced-by:end -->
