# Bead: bob-cli-5s.6 — Refs panel window, list, basic inspector, and keyboard

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5z.md) · **Assignee:** `bob-cli-5s.6` · **Size:** medium
**Created:** 2026-10-08 19:32:40 EDT · **Closed:** 2026-10-09 05:44:16 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

refs-panel-ui: build the borderless non-activating glass panel, search bar, two-line rows, section headers, basic inspector, footer, empty and error states, key router, motion and accessibility, with geometry, router, and rendered design tests checked from the CI artifact.

## Notes

[2026-10-09T07:43:19Z · bob-cli-5s.6] PROPOSED FOLLOW-UP: add the refs-panel-is-a-thin-client decision strand (Bob Refs ranks bob reference index and never mutates it), skipped per auto decision refs_decision_memory = no

[2026-10-09T08:36:13Z · bob-cli-5s.6] PROPOSED FOLLOW-UP: CapturePanelModelTests.testClosePendingListPreviewsTrimmedDraftWithCloseDisabled flakes on CI (waitUntil 5s timeout, failed twice then passed on identical tree 1e22464); consider a longer timeout or less load-sensitive wait

[2026-10-09T09:43:52Z · bob-cli-5s.6] PROPOSED FOLLOW-UP: ImageRenderer fixture limits found in refs-panel-ui — SwiftUI .glassEffect blanks snapshots (live glass now via NSGlassEffectView), ScrollView content snapshots blank (fixtures use static preview stacks), link/borderless Button styles snapshot as blank boxes (use plain); later Refs phases should keep these workarounds

[2026-10-09T09:44:16Z · bob-cli-5s.6] Done: RefsPanelController/RefsPanel (borderless non-activating, NSGlassEffectView, prewarm/show/hide, key monitor, focus repair, resign-hide), RefsPanelView shell, RefsSearchBar (scope token, counts, debounced announcements), RefsListView (pinned sections, selection scroll, row budget), RefsRowView/KindTile/StateGlyph/TodayPill, basic RefsInspectorView, RefsFooter, banner/empty/skeleton/load-failed states, pure RefsKeyRouter (§12+IME), RefsVisualTokens geometry. Tests: RefsKeyRouterTests, RefsPanelGeometryTests, RefsPanelDesignTests (9 states + 7 piece renders, all assertions pass). README gained 'The panel'. CI green on master e987b2f (run 37911975830: lint, build, full suite, bundle, smoke). Reviewed all refs PNGs from render-fixtures (light+dark): sections/order/counts, tiles, pills, glyph alignment, code spans, missing-PDF and banner states, contrast. Additive-only model changes for later phases: RefsCommand.consume, refreshState/hasSnapshot/lastSuccessAt/refreshIfStale/signals/pomodoroName passthroughs, Equatable (RefScope/RefsSectionKind/RefsMove/RefsCommand/RefsOpenTarget) + Hashable (RefsBanner.Action). No entry point wired (belongs to 5s.7). Follow-ups recorded as notes (memory decision, ImageRenderer limits, one flaky capture test that passed on rerun).

## Dependencies

- **Depends on:** [bob-cli-5s.2](bob-cli-5s.2.md) ✓ · ⧖ 2026-10-08
- **Depends on:** [bob-cli-5s.5](bob-cli-5s.5.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.7](bob-cli-5s.7.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.8](bob-cli-5s.8.md) ◐ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.6/README.md) | [bob-cli-5s.6](bob-cli-5s.6.md) | 0 |
