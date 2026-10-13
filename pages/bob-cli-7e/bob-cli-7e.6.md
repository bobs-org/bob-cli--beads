# Bead: bob-cli-7e.6 — Capture \`&\` and dependency drops keep the mirror current

[Bead Pages](../README.md) / [bob-cli-7e](README.md) / bob-cli-7e.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4d.linker.w0.md) · **Assignee:** `bob-cli-7e.6` · **Size:** medium
**Created:** 2026-10-13 11:09:49 EDT · **Closed:** 2026-10-13 14:34:57 EDT
**Plan:** [202610/prerequisite\_blocks\_lines.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prerequisite_blocks_lines.md)

## Description

cli-capture: stage each added prerequisite's BLOCKS entry (and the dependent's minted id) in the same capture batch, remove entries on dependency drops, report rows additively, and keep Bob Mac Capture working without Swift changes.

## Notes

[2026-10-13T18:34:57Z · bob-cli-7e.6] cli-capture BLOCKS mirror done: & stages each added prerequisite entry + dependent mint in-batch via shared planner, drops stage removals, additive blocks_line_updates/minted_dependent_block_id (omitted when empty, human quiet). Verified: 6 new tests/cli/capture/blocks.rs pass, full cargo test green (2555 lib + 1502 cli), fmt --check + clippy gate pass, epic-symbols clean, glossary sentence already present via 7e.4

## Dependencies

- **Depends on:** [bob-cli-7e.2](bob-cli-7e.2.md) ✓ · ⧖ 2026-10-13
- **Depends on:** [bob-cli-7e.5](bob-cli-7e.5.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7e.9](bob-cli-7e.9.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7e.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7e.6/README.md) | [bob-cli-7e.6](bob-cli-7e.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bfdff70`](https://github.com/bobs-org/bob-cli/commit/bfdff70467affebfe212b83d949d790a5a443b1b) | feat(capture): stage BLOCKS mirror on & adds and dependency drops | [bob-cli-7e.6](bob-cli-7e.6.md) | 2026-10-13 14:36:23 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7e.6][1] | Need full JSON including notes history | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7e.6/README.md

<!-- sase:referenced-by:end -->
