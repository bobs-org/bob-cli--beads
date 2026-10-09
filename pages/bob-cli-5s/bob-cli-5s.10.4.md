# Bead: bob-cli-5s.10.4 — Panel visuals, inspector honesty, ⌘K anchor, cleanup, README, and final CI

[Bead Pages](../README.md) / [bob-cli-5s.10](bob-cli-5s.10.md) / bob-cli-5s.10.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.bob-cli-5s.land` · **Assignee:** `bob-cli-5s.10.4` · **Size:** medium
**Created:** 2026-10-09 08:04:27 EDT · **Closed:** 2026-10-09 11:32:18 EDT
**Plan:** [202610/bob\_refs\_land\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_land_fixes.md)

## Description

refs-ui-fixes: in bob-mac-capture, add the content well, Reduce Transparency base, and per-show scale-in; fix inspector honesty rules, the 3 s intrinsics timeout, and the ⌘K anchor; render stem/secondary caption ranges; fix row VoiceOver labels; remove dead symbols and debug renders; make the README's Bob Refs section coherent; confirm final CI and render fixtures.

## Notes

[2026-10-09T15:32:18Z · bob-cli-5s.10.4] refs-ui-fixes verified: all 10 items in bob-mac-capture, 3 commits (3f66470 scope, 649e0b9 transparency-knob compile fix, d5fcac0 continuation timeout race). CI green on final SHA d5fcac0 (run 37949647297, https://github.com/bobs-org/bob-mac-capture/actions/runs/37949647297, success on --failed rerun); swift-format lint + build green; RefsCoreTests 98/98 pass on Linux incl. new caption-range/no-repeat-author tests. Render-fixtures reviewed in light+dark: well, sections, rows, unavailable row (dimmed, keeps index, title+message inspector), stem-match caption (accent stem, unmarked title), inspector chat/paper/encrypted/missing-PDF (no Unknown date, no Added repeat, Tasks only when open, ABSTRACT papers-only, ↵ callout), banner, Reduce Transparency; no clipping/contrast issues. No --epic-symbol leftovers. No memory edits. FLAKE NOTE: RefsLibraryTests.testRefreshIfStale failed 4-vs-3 argv twice on first attempts (an untouched refresh path; my diff cannot add bob invocations) and passed on the sanctioned --failed rerun; treating as timing flake, no test changed. MAC CHECKLIST UPDATE (from bob-cli-5s.9 note 3): typing in the search field filters live; an open error re-shows the panel with query/selection/pending-open intact and Try Again re-dispatches; a deleted reference stays dimmed in place and never opens; toggling Ctrl-Shift-Cmd-R in Settings applies at once.

## Dependencies

- **Depends on:** [bob-cli-5s.10.1](bob-cli-5s.10.1.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5s.10.3](bob-cli-5s.10.3.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5s.10.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.4/README.md) | [bob-cli-5s.10.4](bob-cli-5s.10.4.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3f66470`](https://github.com/bobs-org/bob-mac-capture/commit/3f66470cb95016826e35c91e79e4138cf6a94b7f) | fix(refs): panel visuals, inspector honesty, ⌘K anchor, and closeout | [bob-cli-5s.10.4](bob-cli-5s.10.4.md) | 2026-10-09 10:49:15 EDT |
| bob-mac-capture | [`bob-mac-capture@649e0b9`](https://github.com/bobs-org/bob-mac-capture/commit/649e0b9bc733fbed365debe3ed773b14f00cb42e) | fix(refs): force the Reduce Transparency render through a view knob | [bob-cli-5s.10.4](bob-cli-5s.10.4.md) | 2026-10-09 10:52:30 EDT |
| bob-mac-capture | [`bob-mac-capture@d5fcac0`](https://github.com/bobs-org/bob-mac-capture/commit/d5fcac0d07b872dc633f5ebb201a6cc56a36d875) | fix(refs): race the intrinsics timeout on a continuation | [bob-cli-5s.10.4](bob-cli-5s.10.4.md) | 2026-10-09 11:09:46 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.10.4][1] | check notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.4/README.md

<!-- sase:referenced-by:end -->
