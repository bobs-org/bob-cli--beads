# Bead: bob-cli-bp.4 — Day strip data selection, refresh policy, fence, and Stats hand-off

[Bead Pages](../README.md) / [bob-cli-bp](README.md) / bob-cli-bp.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2f.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2f.linker.w1.md) · **Assignee:** `bob-cli-bp.4` · **Size:** medium
**Created:** 2026-10-24 16:30:45 EDT · **Closed:** 2026-10-24 17:56:54 EDT
**Plan:** [202610/daily\_note\_day\_strip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_note_day_strip.md)

## Description

strip-hosts: add the day-identity and report-selection rules, the strip registry and its visible/dirty/aged refresh policy with rollover, the `bob-day-stats` fence host, and `openStatsForDay`, which opens Stats with the day pinned. Cover them with fake-timer, fake-IntersectionObserver, and fake-execFile tests.

## Notes

[2026-10-24T21:56:38Z · bob-cli-bp.4] PROPOSED FOLLOW-UP: decision_record=no — add decisions:day-strip-shows-the-days-facts (facts-not-targets, virtual mount, bob owns numbers) once Bryan approves; skipped per epic decision

[2026-10-24T21:56:44Z · bob-cli-bp.4] PROPOSED FOLLOW-UP: glossary_term=no — add Day Strip glossary term (vs Morning GTD Review Footer) once Bryan approves; skipped per epic decision

[2026-10-24T21:56:54Z · bob-cli-bp.4] strip-hosts done: day identity/selection, registry with visible-dirty-aged policy, bob-day-stats fence, openStatsForDay with pinned-day first paint + revealPanel. 29/29 new hosts tests pass; npm run build + validate green; full npm test 3623 pass with 1 unrelated flaky perf timing test (stage ranker 16.88ms vs 16ms; passes 23/23 in isolation twice). bob plugins sync deployed. Changes uncommitted in bob-plugins working tree for the land agent.

## Dependencies

- **Depends on:** [bob-cli-bp.2](bob-cli-bp.2.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bp.3](bob-cli-bp.3.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bp.5](bob-cli-bp.5.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bp.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.4/README.md) | [bob-cli-bp.4](bob-cli-bp.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bp.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.4/README.md

<!-- sase:referenced-by:end -->
