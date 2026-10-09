# Bead: bob-cli-5s.10.2 — RefsCore ranking, captions, dates, and refs-rank fixes

[Bead Pages](../README.md) / [bob-cli-5s.10](bob-cli-5s.10.md) / bob-cli-5s.10.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.bob-cli-5s.land` · **Assignee:** `bob-cli-5s.10.2` · **Size:** medium
**Created:** 2026-10-09 08:04:27 EDT · **Closed:** 2026-10-09 08:49:28 EDT
**Plan:** [202610/bob\_refs\_land\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_land_fixes.md)

## Description

refs-core-fixes: in bob-mac-capture RefsCore, keep vanished ids in refreshingContent as unavailable, let 2-character word prefixes reach T1, compute days in signals.calendar instead of UTC, sort Ready by added desc, mark git dates approximate, fix the weekday range, wire frecencyHalfLifeDays, cache prepared items per snapshot, and make refs-rank --now accept the documented form; with tests.

## Notes

[2026-10-09T12:20:31Z · bob-cli-5s.10.2] INTERFACE CHANGE for refs-model-fixes: RefsListing now carries unavailableIDs: Set<String> and unavailableItems: [String: RefItem] (last known titles); refreshingContent(availableIDs:lastKnownItems:) keeps vanished ids in orderedIDs/sections (defaults keep old call sites compiling; pass the library items dict for titles); fresh RefsRanker.listing drops them. Also available: RefsRanker.readyLane (Ready added-desc sort), RefsDates.ordinal(_:calendar:), RefsCaption.relativeCompact/relativeLong with defaulted calendar: param.

[2026-10-09T12:39:10Z · bob-cli-5s.10.2] PROPOSED FOLLOW-UP: base just check stays red on return_links Pandoc failures tracked by task bob-cli-5t; tailored verify script used instead

[2026-10-09T12:49:28Z · bob-cli-5s.10.2] refs-core-fixes verified: all 9 items implemented with tests (unavailableIDs/items + keep-index refresh, T1 2-char prefixes, calendar day counts, Ready added-desc, git approximate via -g path, weekday 2...6, frecencyHalfLifeDays wired, per-snapshot prepared cache, refs-rank --now/--tz + aligned columns); README Sorting/Tuning updated; tailored verify script PASS; just check red only on pre-existing base return_links failures (bob-cli-5t); no Swift toolchain on host so swift build/test and macOS CI remain for the pushed commit; epic-symbols clean

## Dependencies

- **Blocks:** [bob-cli-5s.10.3](bob-cli-5s.10.3.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.10.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.10.2/README.md) | [bob-cli-5s.10.2](bob-cli-5s.10.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3a5fd4a`](https://github.com/bobs-org/bob-mac-capture/commit/3a5fd4afa7c569157c5eab963e1c2a9209ebfff9) | fix(refs): ranking, captions, dates, and refs-rank core fixes | [bob-cli-5s.10.2](bob-cli-5s.10.2.md) | 2026-10-09 08:51:44 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.10.2][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-5s.10.3][2] | Need INTERFACE CHANGE entries from predecessor phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.3/README.md

<!-- sase:referenced-by:end -->
