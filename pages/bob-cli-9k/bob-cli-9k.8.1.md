# Bead: bob-cli-9k.8.1 — bob-cli: homes contract parity, review time, and Stats fixes

[Bead Pages](../README.md) / [bob-cli-9k.8](bob-cli-9k.8.md) / bob-cli-9k.8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-9k.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.land.md) · **Assignee:** `bob-cli-9k.8.1` · **Size:** medium
**Created:** 2026-10-18 20:20:11 EDT · **Closed:** 2026-10-18 20:53:55 EDT
**Plan:** [202610/pomodoro\_homes\_landing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes_landing.md)

## Description

contract: give the R5 remainder to the first task, mark every closed entry attributed, re-split the shared vectors so only the ambiguous-basename case is rust_only and add the missing cases, put review_time on the GTD review row (per decision), stop re-splitting theme parts when no home filter drops a task, prune the homes catalog to used keys, align `bob projects list`, print the R10 caveat and review hue in `bob stats show`, delete the stale `allow(unused)`, fill the H-vector gaps, and update docs/pomodoro-homes.md and docs/stats.md.

## Notes

[2026-10-19T00:53:55Z · bob-cli-9k.8.1--1] Verified just check passed, just install completed, and release bob stats -f json -r 4w on athena measured 182.2 ms median (178.5–188.1 ms, nine runs after one warmup), 4.7% above the 174 ms plan baseline; updated docs/stats.md Performance and confirmed no epic symbols remain.

## Dependencies

- **Blocks:** [bob-cli-9k.8.2](bob-cli-9k.8.2.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9k.8.3](bob-cli-9k.8.3.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.8.1.md) | [bob-cli-9k.8.1](bob-cli-9k.8.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`77c7741`](https://github.com/bobs-org/bob-cli/commit/77c77410e32b52010ad8f0d539f466202deb30d5) | feat(stats): complete pomodoro homes parity and stats fixes | [bob-cli-9k.8.1](bob-cli-9k.8.1.md) | 2026-10-18 20:54:36 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.8.1--1][1] | Confirm the assigned phase close and recorded verification note | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.8.1.md

<!-- sase:referenced-by:end -->
