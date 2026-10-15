# Bead: bob-cli-7x.3 — bob ref rename command, refusals, and dry run

[Bead Pages](../README.md) / [bob-cli-7x](README.md) / bob-cli-7x.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1k.linker.w0.md) · **Assignee:** `bob-cli-7x.3` · **Size:** medium
**Created:** 2026-10-15 15:25:59 EDT · **Closed:** 2026-10-15 16:47:25 EDT
**Plan:** [202610/bob\_ref\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_rename.md)

## Description

rename-plan: in bob-cli, register `bob ref rename` in the Library help group with help, completion, and docs; resolve REF exactly; compute the full move, link, and frontmatter plan; implement every scope, name, highlight-state, and precondition refusal; print -d plans as human or JSON (schema 1); live mode still refuses until rename-write.

## Notes

[2026-10-15T20:47:25Z · bob-cli-7x.3--3] Implemented the bob ref rename planner CLI, refusal and dry-run reporting, docs, completion, and help fixtures. Verified with just check (exit 0); epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-7x.2](bob-cli-7x.2.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.4](bob-cli-7x.4.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7x.7](bob-cli-7x.7.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7x.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7x.3.md) | [bob-cli-7x.3](bob-cli-7x.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f732097`](https://github.com/bobs-org/bob-cli/commit/f732097c99668cc009294a76d1fa89cd6ea92ae9) | feat(ref): add reference rename planning | [bob-cli-7x.3](bob-cli-7x.3.md) | 2026-10-15 16:48:53 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7x.3--3][1] | Need the phase scope and design file before closing after verification | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7x.3.md

<!-- sase:referenced-by:end -->
