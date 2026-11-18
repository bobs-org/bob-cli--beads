# Bead: bob-cli-na.7 — Record-sheet walk rail

[Bead Pages](../README.md) / [bob-cli-na](README.md) / bob-cli-na.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5b.linker.w0.md) · **Assignee:** `bob-cli-na.7` · **Size:** medium
**Created:** 2026-11-18 11:07:19 EST · **Closed:** 2026-11-18 16:31:27 EST
**Plan:** [202611/record\_walk\_ring.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_walk_ring.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:6fd98fa413fbd1e4e21629f1 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

walk-rail (bob-plugins): render the walk line as a docked rail under the record sheet in Live Preview and Reading view (prev, album + N of M, next, hue track, wrap cue, narrow collapse, a11y), with an Obsidian e2e and docs.

## Notes

[2026-11-18T21:28:33Z · bob-cli-na.7] PROPOSED FOLLOW-UP: Corroborate existing bob-cli-km and bob-cli-io timing gates — full npm test on this change and clean bob-plugins 281ee8a both fail the event-link-times 200-link 25 ms and frees-marks 200-link/2000-task 25 ms assertions. Athena repeats those two failures. Apollo also hit the unrelated KT1-KT8 resident-count timing assertion; all 46 tests in the three affected files pass in isolation. No timing limits or unrelated production code changed. Coordinate with the existing CPU-work gate effort rather than filing duplicate tasks.

[2026-11-18T21:31:27Z · bob-cli-na.7] Implemented the bob-plugins record walk rail in Live Preview and Reading view, including written-link navigation, checked live counts, syncing, wrap cues, hue track, singleton/two-record handling, narrow collapse, accessible targets/focus/hover, modified clicks, cursor reveal, and async source-generation protection. Added real-Obsidian acceptance and docs. Verified: build and generated-source checks; 42 focused tests; 15 real Obsidian cases on athena (0px dock gap, 32px arms, 297px narrow layout, no ghost creation or renderer errors); startup smoke (four editor mounts, 46.9 MiB peak heap, no crashes/exceptions); docs gate (447 passed, one dependency skip); all 11 configured deployed plugins synced with zero drift. Full-suite timing failures are documented in the PROPOSED FOLLOW-UP note; all 46 affected-file tests pass isolated, and the two 25ms failures reproduce on clean 281ee8a. No epic symbols remain. Evidence: file:explicit:6fd98fa413fbd1e4e21629f1. Closed only this phase; no memory edits or ancestor closure.

## Dependencies

- **Depends on:** [bob-cli-na.6](bob-cli-na.6.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-na.8](bob-cli-na.8.md) ✓ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-na.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-na.7/README.md) | [bob-cli-na.7](bob-cli-na.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e7d82af`](https://github.com/bobs-org/bob-plugins/commit/e7d82afe0c5fb6b9e5424803dc3bcf26fd456a28) | feat(records): dock the record walk rail under record sheets | [bob-cli-na.7](bob-cli-na.7.md) | 2026-11-18 16:32:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-na.7][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-na.land][2] | Need the child scope and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-na.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-na.land.md

<!-- sase:referenced-by:end -->
