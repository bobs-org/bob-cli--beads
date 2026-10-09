# Bead: bob-cli-5s.10.2 — RefsCore ranking, captions, dates, and refs-rank fixes

[Bead Pages](../README.md) / [bob-cli-5s.10](bob-cli-5s.10.md) / bob-cli-5s.10.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-5s.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.land.md) · **Assignee:** `bob-cli-5s.10.2` · **Size:** medium
**Created:** 2026-10-09 08:04:27 EDT
**Plan:** [202610/bob\_refs\_land\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_land_fixes.md)

## Description

refs-core-fixes: in bob-mac-capture RefsCore, keep vanished ids in refreshingContent as unavailable, let 2-character word prefixes reach T1, compute days in signals.calendar instead of UTC, sort Ready by added desc, mark git dates approximate, fix the weekday range, wire frecencyHalfLifeDays, cache prepared items per snapshot, and make refs-rank --now accept the documented form; with tests.

## Notes

[2026-10-09T12:20:31Z · bob-cli-5s.10.2] INTERFACE CHANGE for refs-model-fixes: RefsListing now carries unavailableIDs: Set<String> and unavailableItems: [String: RefItem] (last known titles); refreshingContent(availableIDs:lastKnownItems:) keeps vanished ids in orderedIDs/sections (defaults keep old call sites compiling; pass the library items dict for titles); fresh RefsRanker.listing drops them. Also available: RefsRanker.readyLane (Ready added-desc sort), RefsDates.ordinal(_:calendar:), RefsCaption.relativeCompact/relativeLong with defaulted calendar: param.

## Dependencies

- **Blocks:** [bob-cli-5s.10.3](bob-cli-5s.10.3.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.10.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.10.2/README.md) | [bob-cli-5s.10.2](bob-cli-5s.10.2.md) | 0 |
