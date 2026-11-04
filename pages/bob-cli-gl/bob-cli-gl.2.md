# Bead: bob-cli-gl.2 — Move-bullet lexer, parsers, and capture-parse

[Bead Pages](../README.md) / [bob-cli-gl](README.md) / bob-cli-gl.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.35.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.35.linker.w0.md) · **Assignee:** `bob-cli-gl.2` · **Size:** medium
**Created:** 2026-11-03 13:39:31 EST · **Closed:** 2026-11-03 15:59:14 EST
**Plan:** [202611/capture\_move\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_bullets.md)

## Description

cli-grammar: Add the shared `move_bullet` lexer. Wire it into the execution parser (`item.rs`) and the editor parser (`editor_parse.rs`). Report the new spans, the `project_task_move` need, `sub_bullet_moves`, and every lexical diagnostic, and apply the grammar-revision decision. Execution refuses move bullets until `cli-execution` lands.

## Notes

[2026-11-03T20:59:14Z · bob-cli-gl.2] cli-grammar done: shared move_bullet lexer claims first-level ^/:id (unfinished + 8 lexical errors with byte-identical messages in both parsers), wired into item.rs and editor_parse.rs with project_task_move need, 3 new spans, sub_bullet_moves JSON + human output, GRAMMAR 6->7, interim planner refusal with test. Verified: 4741 lib + 2948 cli + all workspace bins green, fmt/clippy clean, docs-gen + docs-check pass, 16 new lexer/agreement unit tests + capture-parse MC1/MC2/MV7 CLI tests + interim-guard CLI test green. No follow-ups.

## Dependencies

- **Depends on:** [bob-cli-gl.1](bob-cli-gl.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.4](bob-cli-gl.4.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.5](bob-cli-gl.5.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.2/README.md) | [bob-cli-gl.2](bob-cli-gl.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b94eec2`](https://github.com/bobs-org/bob-cli/commit/b94eec2c04ba7f9730ff605df4116f3928b62825) | feat(capture)!: parse move bullets in sealed project-note items | [bob-cli-gl.2](bob-cli-gl.2.md) | 2026-11-03 16:00:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.2/README.md

<!-- sase:referenced-by:end -->
