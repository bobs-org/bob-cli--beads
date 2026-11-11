# Bead: bob-cli-kc.1 — Pure Copy card model, template grammar, and config loader

[Bead Pages](../README.md) / [bob-cli-kc](README.md) / bob-cli-kc.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bg](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bg.md) · **Assignee:** `bob-cli-kc.1` · **Size:** medium
**Created:** 2026-11-11 11:19:06 EST · **Closed:** 2026-11-11 11:38:29 EST
**Plan:** [202611/cmd\_y\_copy\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/cmd_y_copy_card.md)

## Description

model: add Obsidian-free fragments for the row table, the owning-task resolver, the single-pass template grammar, copy.templates loading and validation, the frozen card model, and key resolution, with exhaustive unit tests.

## Notes

[2026-11-11T16:38:06Z · bob-cli-kc.1] PROPOSED FOLLOW-UP: Pre-existing stylesheet hex contract failures on clean HEAD 27b99dd — test-ledger-tools-reading-board-block.cjs and test-ledger-tools-stats-block.cjs reject --bob-keep-moving-mark-ink hex; already noted on bob-cli-j8.6.1.3 and bob-cli-je.2

[2026-11-11T16:38:16Z · bob-cli-kc.1] PROPOSED FOLLOW-UP: test-ledger-tools-keep-moving-marks-surface.cjs 25 ms Live Preview budget failed at 324 ms under full npm test load and passed in isolation on clean HEAD 27b99dd — same class of load flake as bob-cli-ej, from the keep-moving marks work on bob-cli-k7

[2026-11-11T16:38:29Z · bob-cli-kc.1] Added Obsidian-free Copy card fragments 101/101a/102/717 in bob-plugins: builtin rows, owning-task resolver, single-pass template grammar, frozen model, cmd_y_twice key resolution, and copy.templates loader with mtime/size cache. 41 new unit tests pass; npm run build and build:check pass. Full npm test is 6092 pass / 3 fail, all three reproduced on clean HEAD 27b99dd or as a full-suite load flake (recorded as PROPOSED FOLLOW-UP). No UI/command changes; no bob plugins sync. No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-kc.2](bob-cli-kc.2.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kc.1/README.md) | [bob-cli-kc.1](bob-cli-kc.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@353eedb`](https://github.com/bobs-org/bob-plugins/commit/353eedbc8799f9c16d8c5e26325a203e99980b0e) | feat(navigation-hotkeys): add pure Copy card model, grammar, and config loader | [bob-cli-kc.1](bob-cli-kc.1.md) | 2026-11-11 11:39:51 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kc.1][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kc.1/README.md

<!-- sase:referenced-by:end -->
