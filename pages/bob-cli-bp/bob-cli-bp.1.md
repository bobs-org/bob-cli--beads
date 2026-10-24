# Bead: bob-cli-bp.1 — bob stats reads "not yet" for an unmet provisional boolean

[Bead Pages](../README.md) / [bob-cli-bp](README.md) / bob-cli-bp.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2f.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2f.linker.w1.md) · **Assignee:** `bob-cli-bp.1` · **Size:** small
**Created:** 2026-10-24 16:30:44 EDT · **Closed:** 2026-10-24 16:49:36 EDT
**Plan:** [202610/daily\_note\_day\_strip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_note_day_strip.md)

## Description

stats-not-yet: in bob-cli, make an unmet provisional (today) boolean point display `not yet` in JSON, CSV, and human output, and draw `◌` in the bool sparkline. Then update the unit and CLI tests and the docs/stats.md display rules and M6 row.

## Notes

[2026-10-24T20:43:07Z · bob-cli-bp.1] PROPOSED FOLLOW-UP: Fix the pre-existing Rust test compile error at src/native/capture/inbox_route.rs:1318 — commit_capture_batch now requires a bob_dir path argument, but this test still supplies one argument; cargo test native::stats currently cannot compile past it.

[2026-10-24T20:49:36Z · bob-cli-bp.1] Implemented provisional unmet boolean display as 'not yet' in JSON/CSV/human output and ◌ in overview sparklines; updated unit/CLI expectations and docs M6. Verified 14 filtered CLI stats tests pass, cargo fmt -- --check and git diff --check pass, just docs-check passes (447 passed, 1 optional-dependency skip), and epic-symbol check is clear. cargo test native::stats is blocked by a clean-HEAD compile error at capture/inbox_route.rs:1318; recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-bp.6](bob-cli-bp.6.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bp.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.1/README.md) | [bob-cli-bp.1](bob-cli-bp.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0fc6ebf`](https://github.com/bobs-org/bob-cli/commit/0fc6ebfaccaca03e00dab4f0ee6552db2c92834c) | fix(stats): mark unmet provisional booleans not yet | [bob-cli-bp.1](bob-cli-bp.1.md) | 2026-10-24 16:51:15 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bp.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.1/README.md

<!-- sase:referenced-by:end -->
