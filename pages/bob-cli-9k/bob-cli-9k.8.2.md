# Bead: bob-cli-9k.8.2 — bob-cli: homes on bob ref today, human bob plan, and the = override surfaces

[Bead Pages](../README.md) / [bob-cli-9k.8](bob-cli-9k.8.md) / bob-cli-9k.8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-9k.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.land.md) · **Assignee:** `bob-cli-9k.8.2` · **Size:** medium
**Created:** 2026-10-18 20:20:11 EDT · **Closed:** 2026-10-18 21:20:28 EDT
**Plan:** [202610/pomodoro\_homes\_landing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes_landing.md)

## Description

surfaces: add the R9 `homes` object to `bob ref today -f json` Pomodoro rows and use the derived label in its human output, print the dim chip for unnamed entries in human `bob plan`, and add `homes` to the bob-cli-9j override JSON (`override.previous`, `override.demoted`, capture-complete `override.running`) with the chip in the human warning, demoted, and `--refuse-override` lines for unnamed sessions. Update docs and tests.

## Notes

[2026-10-19T01:20:28Z · bob-cli-9k.8.2] Surfaces done: R9 homes on ref-today rows (derived label in human), dim chip for unnamed entries in human bob plan, homes on override.previous/demoted/running JSON with chips in warning/demoted/refuse lines (named sessions resolve nothing). Verified: just check green (fmt, clippy, 2990 lib + 1834 cli tests incl. 4 new), capture-pomodoros --tasks -f json ~6ms on athena, just install ran, no epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-9k.8.1](bob-cli-9k.8.1.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9k.8.4](bob-cli-9k.8.4.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.2/README.md) | [bob-cli-9k.8.2](bob-cli-9k.8.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c2c9f5c`](https://github.com/bobs-org/bob-cli/commit/c2c9f5c1a0f1f96659e47949d0f53a84e69dbc62) | feat(unnamed-sessions): label unnamed sessions by derived homes | [bob-cli-9k.8.2](bob-cli-9k.8.2.md) | 2026-10-18 21:22:04 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.8.2][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-9k.8.land--1][2] | Need phase evidence and all notes before recording the remaining epic gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.8.land.md

<!-- sase:referenced-by:end -->
