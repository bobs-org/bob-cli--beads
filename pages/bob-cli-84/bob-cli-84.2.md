# Bead: bob-cli-84.2 — RefsCore tab snapshot, matcher, ordering, and session

[Bead Pages](../README.md) / [bob-cli-84](README.md) / bob-cli-84.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7w.md) · **Assignee:** `bob-cli-84.2` · **Size:** medium
**Created:** 2026-10-15 17:50:48 EDT · **Closed:** 2026-10-16 06:58:47 EDT
**Plan:** [202610/highlights\_tabs\_switcher.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tabs_switcher.md)

## Description

tabs-core: pure Foundation types in RefsCore. They cover the snapshot, the reader protocol and its results, the full-path → unique-file-name → collision → none matcher, the A5 ordering and pre-selection, the stale-target locator, tab recency, the scoped and searchable tabs listing, the "N tabs" count text, the `.inHighlights` section, and a main-actor session that owns generations and recency. Golden tests run with `just portable-check`.

## Notes

[2026-10-16T10:53:32Z · bob-cli-84.2--2] --list

[2026-10-16T10:58:16Z · bob-cli-84.2--2] PROPOSED FOLLOW-UP: Add a decisions record stating Bob Mac Capture uses Accessibility only to read and select Highlights tabs (skipped per epic decision_record=no)

[2026-10-16T10:58:47Z · bob-cli-84.2--2] tabs-core verified: just portable-check green on athena (swift-format lint, swift build --build-tests, 1236 tests 0 failures incl. RefsHighlightsTabsTests golden coverage for snapshot, matcher path/fileName/collision/none+dedupe, A5 browse order+preselection, scope filter, search tiers, count text, locator rules, session generations/recency). Fixed one assertion to sorted candidateIDs. No Mac-only exhaustive switches over RefsSectionKind; athena scratch copy removed.

## Dependencies

- **Blocks:** [bob-cli-84.3](bob-cli-84.3.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-84.4](bob-cli-84.4.md) ✓ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-84.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-84.2.md) | [bob-cli-84.2](bob-cli-84.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@94a4e58`](https://github.com/bobs-org/bob-mac-capture/commit/94a4e589b12d45fec7d10347d0bc6931623bf568) | feat(refs): add Highlights tabs snapshot, matcher, ranking, and session | [bob-cli-84.2](bob-cli-84.2.md) | 2026-10-16 06:59:53 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-84.2--2][1] | Check phase notes for remaining work and follow-ups before verifying | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-84.2.md

<!-- sase:referenced-by:end -->
