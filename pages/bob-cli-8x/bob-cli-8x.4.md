# Bead: bob-cli-8x.4 — Task Card ⇧B row, Ctrl+Shift+Alt+B, and every other entry point

[Bead Pages](../README.md) / [bob-cli-8x](README.md) / bob-cli-8x.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.117](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.117.md) · **Assignee:** `bob-cli-8x.4` · **Size:** medium
**Created:** 2026-10-17 17:11:59 EDT · **Closed:** 2026-10-17 19:28:10 EDT
**Plan:** [202610/ctrl\_shift\_alt\_b\_blocks\_stage.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_alt_b_blocks_stage.md)

## Description

entry: add the Task Card Blocks… row (key ⇧B), the task-card-blocks command bound to Ctrl+Shift+Alt+B, and counted N<Ctrl+Shift+Alt+B>. Wire Task Link, Depends-On-line, and BLOCKS-line entries, Ctrl+Shift+P on a BLOCKS line, entry refusals, the generated-line notice copy, and api.blocks (openStage, removeDependent). Bump the nav minor version.

## Notes

[2026-10-17T23:27:22Z · bob-cli-8x.4] PROPOSED FOLLOW-UP: Full bob-plugins npm test has six clean-base failures, unchanged at starting commit bca788d: four unblocked-glyph cases (bob-cli-6v), Keep counts once (bob-cli-6w), and forward/reverse conversion BLOCKS re-keying (bob-cli-7i).

[2026-10-17T23:28:10Z · bob-cli-8x.4] Implemented Blocks Task Card row, command, entry routes, BLOCKS-line redirect, generated-line notice, and api.blocks v1; focused tests (157), build/manifest validation, diff check, and workspace plugin sync verified. Full npm test's six failures reproduce on clean base and are tracked by bob-cli-6v, bob-cli-6w, and bob-cli-7i.

## Dependencies

- **Depends on:** [bob-cli-8x.3](bob-cli-8x.3.md) ✓ · ⧖ 2026-10-17
- **Blocks:** [bob-cli-8x.5](bob-cli-8x.5.md) ✓ · ⧖ 2026-10-17
- **Blocks:** [bob-cli-8x.6](bob-cli-8x.6.md) ✓ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8x.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.4/README.md) | [bob-cli-8x.4](bob-cli-8x.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@10d12f4`](https://github.com/bobs-org/bob-plugins/commit/10d12f42aeb3944fe0ed54fa7c3c3da5c501486c) | feat(navigation): add Task Card Blocks entry points | [bob-cli-8x.4](bob-cli-8x.4.md) | 2026-10-17 19:28:45 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8x.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.4/README.md

<!-- sase:referenced-by:end -->
