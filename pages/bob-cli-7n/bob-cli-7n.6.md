# Bead: bob-cli-7n.6 — Execute \`\*\` captures and report them

[Bead Pages](../README.md) / [bob-cli-7n](README.md) / bob-cli-7n.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4g.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4g.linker.w1.md) · **Assignee:** `bob-cli-7n.6` · **Size:** medium
**Created:** 2026-10-14 11:27:20 EDT · **Closed:** 2026-10-14 14:04:17 EDT
**Plan:** [202610/capture\_star\_blocks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_star_blocks.md)

## Description

execute: wire parsed blocked_tasks into new-task, sub-bullet, dependency-only, and forced --task captures in the link-then-consume order, and emit dependency_updates[], minted_blocker_block_id, and the human lines, with ST vector tests.

## Notes

[2026-10-14T18:04:17Z · bob-cli-7n.6] Wired * into new-task, sub-bullet, dependency-only, and forced --task/--route captures in link-then-consume order. JSON emits dependency_updates[] (singular equals [0]), minted_blocker_block_id, and human 🧱 lines. Parse help no longer says * is unsupported. ST1–ST19 plus related capture tests pass; just check is green.

## Dependencies

- **Depends on:** [bob-cli-7n.3](bob-cli-7n.3.md) ✓ · ⧖ 2026-10-14
- **Depends on:** [bob-cli-7n.4](bob-cli-7n.4.md) ✓ · ⧖ 2026-10-14
- **Blocks:** [bob-cli-7n.7](bob-cli-7n.7.md) ✓ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7n.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7n.6/README.md) | [bob-cli-7n.6](bob-cli-7n.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1b9d35f`](https://github.com/bobs-org/bob-cli/commit/1b9d35f206f84c03ca4499d9f78dc69a8b170d78) | feat(capture): execute \* blocked-task captures and report them | [bob-cli-7n.6](bob-cli-7n.6.md) | 2026-10-14 14:06:34 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7n.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7n.6/README.md

<!-- sase:referenced-by:end -->
