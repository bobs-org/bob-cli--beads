# Bead: bob-cli-fl.3.1.1 — Evaluate Stats metrics on separate clocks

[Bead Pages](../README.md) / [bob-cli-fl.3.1](bob-cli-fl.3.1.md) / bob-cli-fl.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.3.md) · **Assignee:** `bob-cli-fl.3.1.1` · **Size:** medium
**Created:** 2026-11-02 01:23:56 EST · **Closed:** 2026-11-02 02:26:12 EST
**Plan:** [202611/stats\_clock.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock.md)

## Description

clock_evaluation: add request and pinned metric clocks, isolated formula evaluation, coverage, labels, and the clock/sub-share JSON contract.

## Notes

[2026-11-02T07:26:12Z · bob-cli-fl.3.1.1] Stats engine evaluates Worked/Off-clock/Total from one index: request and pinned clocks, formula isolation, adoption coverage, clock JSON, and off_clock sub-shares. Verified cargo test --lib native::stats (186 passed) and cargo test --test cli stats (15 passed), including golden Oct 9 32m+60m, clock options 42/60/102, human output still Worked-only this phase, sessions[2].minutes still 0.

## Dependencies

- **Blocks:** [bob-cli-fl.3.1.2](bob-cli-fl.3.1.2.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.3.1.1/README.md) | [bob-cli-fl.3.1.1](bob-cli-fl.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4d950c5`](https://github.com/bobs-org/bob-cli/commit/4d950c58a5b198fcb89067d6fd6b1fc26c2f09b4) | feat(stats): evaluate Pomodoro metrics on worked, off-clock, and total clocks | [bob-cli-fl.3.1.1](bob-cli-fl.3.1.1.md) | 2026-11-02 02:27:24 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.3.1.1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.3.1.1/README.md

<!-- sase:referenced-by:end -->
