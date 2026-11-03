# Bead: bob-cli-gl.4 — capture-complete \`project\_task\_move\` context and rows

[Bead Pages](../README.md) / [bob-cli-gl](README.md) / bob-cli-gl.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.35.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.35.linker.w0.md) · **Assignee:** `bob-cli-gl.4` · **Size:** medium
**Created:** 2026-11-03 13:39:31 EST · **Closed:** 2026-11-03 17:01:29 EST
**Plan:** [202611/capture\_move\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_bullets.md)

## Description

cli-complete: Add the `project_task_move` completion field and context. It serves the parent's open top-level tasks as rows (ID-less rows included) with a Bob-authored consequence, disabled reasons, ordering, a `project_task_move` picker descriptor with the shift-return `continuation`, and a response header object. Update the capture-complete help and the generated reference.

## Notes

[2026-11-03T21:55:39Z · bob-cli-gl.4] PROPOSED FOLLOW-UP: Fix the clean-base bob-cli compile failure: src/native/capture/plan.rs:2019 initializes CaptureItemResult without required note_pull; reproduced by just check / cargo check --bin bob. This planner issue is outside bob-cli-gl.4.

[2026-11-03T22:01:29Z · bob-cli-gl.4] Implemented project_task_move completion, picker metadata, candidate rows, shell completion, help, and generated reference. Verified the 3 focused move tests, all 134 capture completion regressions, just docs-gen, just docs-check (447 passed, 1 skipped), cargo fmt, and git diff --check. just check reproduces the clean-base missing note_pull initializer at src/native/capture/plan.rs:2019; recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-gl.2](bob-cli-gl.2.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-gl.3](bob-cli-gl.3.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.6](bob-cli-gl.6.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.4/README.md) | [bob-cli-gl.4](bob-cli-gl.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b8688d9`](https://github.com/bobs-org/bob-cli/commit/b8688d9ef802f719d5ee46f02d3b87c1080fcaa2) | feat(capture)!: add project task move completion | [bob-cli-gl.4](bob-cli-gl.4.md) | 2026-11-03 17:02:59 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.3][1] | Coordinate the shared eligibility and batch-move engine interfaces with dependent phases | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.3/README.md

<!-- sase:referenced-by:end -->
