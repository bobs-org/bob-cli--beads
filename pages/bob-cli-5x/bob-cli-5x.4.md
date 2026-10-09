# Bead: bob-cli-5x.4 — ⌘S key, footer status, banners, notifications, docs, and renders

[Bead Pages](../README.md) / [bob-cli-5x](README.md) / bob-cli-5x.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z1.md) · **Assignee:** `bob-cli-5x.4` · **Size:** medium
**Created:** 2026-10-09 12:26:29 EDT · **Closed:** 2026-10-09 14:30:45 EDT
**Plan:** [202610/bob\_refs\_scan\_keymap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_scan_keymap.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-61][1] | Triage outcome for the refresh timeout proposed in phase note #2 |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-61/README.md

<!-- sase:links:end -->

## Description

refs-scan-ui: route ⌘S and the ⌘K item, draw the footer scan status, the Just scanned header, the no-match hint, and the Scan Again banner action, post notifications when the panel is hidden, document the feature in the README, check fixture parity with the real bob envelope, and review light and dark renders.

## Notes

[2026-10-09T18:13:36Z · bob-cli-5x.4] Status: refs-scan-ui implemented and committed as d808c6d in bob-mac-capture (⌘S routing, ⌘K Scan item, footer status+hints, Just scanned header time, no-match hint, hidden-panel notifications, README, 8 render fixtures + router/menu/notification/footer tests). Linux scratch swift test: 861 tests, 0 failures. Fixture parity with cli-scan-json INTERFACE SAMPLE: key sets match exactly. CI run https://github.com/bobs-org/bob-mac-capture/actions/runs/37971680341 in progress; renders not yet reviewed.

[2026-10-09T18:30:21Z · bob-cli-5x.4--1] PROPOSED FOLLOW-UP: stabilize RefsPanelModelTests.testRefreshReordersFromNewDataKeepingSelection (macOS-only 5s waitForModel timeout flakes on CI: same timeout failed on runs 37971680341 twice and on unrelated run 37962741576, while parent commit 37b914c run 37968034913 passed; consider settling the -g git-date lane before serveAddedVariant like testOpenRefreshesTodayWithoutRefreshingSnapshot does)

[2026-10-09T18:30:33Z · bob-cli-5x.4--1] CI run https://github.com/bobs-org/bob-mac-capture/actions/runs/37971680341 (SHA d808c6d): Lint OK, Build OK, Upload render fixtures OK; Test has 1 failure in RefsPanelModelTests.testRefreshReordersFromNewDataKeepingSelection (model condition not met before timeout). Reran the failed job: same test failed identically. Phase diff is 2 lines adding .scanLibrary routing in RefsPanelModel.performAction and cannot affect refresh ordering; identical failure appears on unrelated run 37962741576, so recorded as PROPOSED FOLLOW-UP per base-tree rule. Renders: downloaded all 16 refs-scan-*/refs-no-matches-scan-hint PNGs (light+dark) and reviewed each: footer status baseline aligned with hints, green/orange glyphs legible on glass in dark mode, JUST SCANNED header trailing time right-aligned, failed/partial banners wrap long paths without clipping, no-match second line quiet and untruncated. No render fixes needed. sase bead epic-symbols: no leftover entries. Manual checklist for Bryan on a real Mac: (1) focus Refs panel, press Cmd+S, footer shows Scanning library with elapsed seconds then Added N references or No new references; (2) run a scan with the panel hidden, confirm a notification posts and clicking it shows Bob Refs; (3) open the Cmd+K menu while scanning and confirm Scan for New References is last and disabled; (4) after a scan that adds refs, confirm the JUST SCANNED header shows a relative time.

[2026-10-09T18:30:45Z · bob-cli-5x.4--1] refs-scan-ui done: Cmd+S routing, Cmd+K item, footer/banner/hint UI, notifications, README all committed as d808c6d. Verified: CI lint+build green; all 16 scan render fixtures reviewed in light+dark with no defects; epic-symbols clean. Sole CI test failure (testRefreshReordersFromNewDataKeepingSelection timeout) is a pre-existing macOS-only flake also failing on unrelated runs, recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-5x.1](bob-cli-5x.1.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5x.3](bob-cli-5x.3.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5x.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5x.4.md) | [bob-cli-5x.4](bob-cli-5x.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@d808c6d`](https://github.com/bobs-org/bob-mac-capture/commit/d808c6d50390c605359784a506197336145da0e1) | feat(refs): route ⌘S scan, footer status, banners, and hidden-panel notifications | [bob-cli-5x.4](bob-cli-5x.4.md) | 2026-10-09 14:12:35 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5x.3][1] | Check later phase scope to avoid overlap | 1 |
| read-by | [agent:bob-cli-5x.4][2] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5x.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5x.4.md

<!-- sase:referenced-by:end -->
