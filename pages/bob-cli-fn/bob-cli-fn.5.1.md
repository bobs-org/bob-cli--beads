# Bead: bob-cli-fn.5.1 — Section selectors with spaces and header-line completion in bob

[Bead Pages](../README.md) / [bob-cli-fn.5](bob-cli-fn.5.md) / bob-cli-fn.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fn.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fn.land.md) · **Assignee:** `bob-cli-fn.5.1` · **Size:** medium
**Created:** 2026-11-02 07:14:36 EST · **Closed:** 2026-11-02 07:59:54 EST
**Plan:** [202611/capture\_list\_section\_names.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_list_section_names.md)

## Description

section-selectors: add slug matching to `@route#selector` section selectors, make section completion insert a selector that resolves back to the picked heading (raw, slug, or quoted literal), decode partial quoted section queries, treat an unterminated `#"…` section as incomplete in parse and execution, complete route and section tokens on a list header that already has bullets, add the off-clock list-vs-batch test, and document it all.

## Notes

[2026-11-02T12:59:54Z · bob-cli-fn.5.1] Slug matching in target_bullet_section (raw prefix, then identity, then whole-slug, then slug-prefix); section completion replacements round-trip by heading line_index (raw title, hyphen slug, or quoted Title); partial quoted queries decode inner text and cover the whole literal; unterminated quoted section is capture-parse incomplete (needs section, no diagnostic) and bob capture refuses incomplete_section with Bob-authored copy and zero writes; list-header route and section completion works with bullets already present (CRLF/UTF-8 covered); off-clock list matches equivalent batch; screenshot complete sase#Fu then append boom lands under Future Work. Unit and CLI tests for those vectors passed. just docs-gen and just docs-check passed. Temp-vault Why table: sase#future-work files under Future Work; quoted exact works; unterminated is incomplete; capture-complete sase#Fu replacement is future-work; header sase#Fu with bullets and sa with bullets offer section/route menus. No leftover --epic-symbol entries.

[2026-11-02T13:20:18Z · bob-cli-fn.5.1--1] just check failed after close on capture::keep_moving::human_pick_suffix_and_not_pulled_in: expected added ^write-changelog-entry, got ^write-changelog. Reproduced identically on the clean base tree (c3a2e62a). Updated the stale golden so host verification can land. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-fn.5.2](bob-cli-fn.5.2.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fn.5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fn.5.1.md) | [bob-cli-fn.5.1](bob-cli-fn.5.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b483c93`](https://github.com/bobs-org/bob-cli/commit/b483c93b0ec02c5589ef0535d78de10ee31f0afb) | feat(capture): round-trip spaced section selectors | [bob-cli-fn.5.1](bob-cli-fn.5.1.md) | 2026-11-02 08:40:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fn.5.1--2][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fn.5.1.md

<!-- sase:referenced-by:end -->
