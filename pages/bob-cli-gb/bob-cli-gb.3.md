# Bead: bob-cli-gb.3 — bob-cli: agenda JSON, reconcile settle, and stats drift use the effective clock

[Bead Pages](../README.md) / [bob-cli-gb](README.md) / bob-cli-gb.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.31.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.31.linker.w0.md) · **Assignee:** `bob-cli-gb.3` · **Size:** medium
**Created:** 2026-11-02 17:38:44 EST · **Closed:** 2026-11-02 20:59:47 EST
**Plan:** [202611/off\_on\_tags\_and\_offclock\_areas.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_on_tags_and_offclock_areas.md)

## Description

clock-readers: enrich Event Tasks in the capture-pomodoros agenda, settle inherited off-clock Event Tasks in reconcile, and recompute clock_drift by the same rule, with docs.

## Notes

[2026-11-02T23:45:28Z · bob-cli-gb.3] -r check prior work

[2026-11-03T01:59:20Z · bob-cli-gb.3--1] PROPOSED FOLLOW-UP: flaky completion tests under full-suite load return empty stdout yet pass in isolation and on rerun; reproduced on clean base tree without phase changes; candidate for a flake task bead

[2026-11-03T01:59:47Z · bob-cli-gb.3--1] clock-readers done: agenda JSON carries effective clock_source/clock_note, settle enriches events via resolver, stats drift uses effective_clock; new tests pass; fmt/clippy/docs-check clean; full-suite completion flakes reproduced on clean base and noted as follow-up

## Dependencies

- **Depends on:** [bob-cli-gb.1](bob-cli-gb.1.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-gb.8](bob-cli-gb.8.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gb.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gb.3.md) | [bob-cli-gb.3](bob-cli-gb.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a9a499a`](https://github.com/bobs-org/bob-cli/commit/a9a499ac6ee9a0d0cbc68a8c2bdb3b8bcec39930) | feat(clock-readers): effective clock\_source in agenda, settle, and stats drift | [bob-cli-gb.3](bob-cli-gb.3.md) | 2026-11-02 21:02:32 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gb.3--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gb.3.md

<!-- sase:referenced-by:end -->
