# Bead: bob-cli-8x.5 — BLOCKS chip ＋ / × through api.blocks

[Bead Pages](../README.md) / [bob-cli-8x](README.md) / bob-cli-8x.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.117](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.117.md) · **Assignee:** `bob-cli-8x.5` · **Size:** small
**Created:** 2026-10-17 17:11:59 EDT · **Closed:** 2026-10-17 19:53:06 EDT
**Plan:** [202610/ctrl\_shift\_alt\_b\_blocks\_stage.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_alt_b_blocks_stage.md)

## Description

chips: in bob-ledger-tools, give open-owner BLOCKS chip rows a ＋ that calls api.blocks.openStage and a hover × on live chips that calls api.blocks.removeDependent. Feature-detect api.blocks, leave frozen and stale chips alone, and update the tooltip copy. Bump the ledger-tools minor version. Gated by decision chips.

## Notes

[2026-10-17T23:52:55Z · bob-cli-8x.5] PROPOSED FOLLOW-UP: npm test still fails 6 cases identically on clean master — unblocked-glyph Live Preview/Reading (bob-cli-6v), Keep counts once (bob-cli-6w), and forward conversion BLOCKS Work_ship#^prj (bob-cli-7i).

[2026-10-17T23:53:06Z · bob-cli-8x.5] Open-owner BLOCKS rows feature-detect api.blocks v1 for trailing ＋ (openStage with 0-based line) and hover × on live chips (removeDependent); frozen/stale/no-API stay navigation-only. RBC1–RBC4 pass. ledger-tools 1.51.0 synced. Six npm test failures reproduce on clean master (bob-cli-6v, bob-cli-6w, bob-cli-7i).

## Dependencies

- **Depends on:** [bob-cli-8x.4](bob-cli-8x.4.md) ✓ · ⧖ 2026-10-17
- **Blocks:** [bob-cli-8x.6](bob-cli-8x.6.md) ✓ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8x.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.5/README.md) | [bob-cli-8x.5](bob-cli-8x.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@254b32b`](https://github.com/bobs-org/bob-plugins/commit/254b32ba0ee7e54fc0a922de9fbf501701ae9540) | feat(ledger-tools): add BLOCKS chip ＋ / × through api.blocks | [bob-cli-8x.5](bob-cli-8x.5.md) | 2026-10-17 19:54:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8x.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.5/README.md

<!-- sase:referenced-by:end -->
