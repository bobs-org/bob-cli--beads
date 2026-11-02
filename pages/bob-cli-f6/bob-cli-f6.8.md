# Bead: bob-cli-f6.8 — bob-mac-capture: day rail, start-card event runs, conflict banners

[Bead Pages](../README.md) / [bob-cli-f6](README.md) / bob-cli-f6.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bv](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bv.md) · **Assignee:** `bob-cli-f6.8` · **Size:** medium
**Created:** 2026-11-01 11:24:14 EST · **Closed:** 2026-11-01 19:57:39 EST
**Plan:** [202611/untracked\_calendar\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/untracked_calendar_events.md)

## Description

mac-rail-and-cards: draw the day rail and render event runs, far-run and conflict banners, and untracked Now cards.

## Notes

[2026-11-02T00:00:52Z · bob-cli-f6.8--1] PROPOSED FOLLOW-UP: Resolve baseline strict Swift format diagnostics — strict formatting fails on the clean base across existing Package.swift and test files; clean-base portable-check passes.

[2026-11-02T00:01:00Z · bob-cli-f6.8--1] PROPOSED FOLLOW-UP: Import the reviewed agenda-events render after landing — defer the docs image refresh until successful master CI publishes the artifact accepted by the repository importer.

[2026-11-02T00:57:39Z · bob-cli-f6.8--4] Phase work (day rail, start-card event runs, conflict banners, untracked Now cards) is on bob-mac-capture origin/master as c4d8cf0, which an Athena auto-commit swept up from the shared checkout. It carried one phase-authored test bug: testEventConflictsDecodeForAdjustAndShift was missing its opening brace. The fix is a one-line change to Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift, committed by the finalizer. Verified in a clean throwaway Athena copy of c4d8cf0 plus the fix: just portable-check passed (1920 tests, 0 failures) and just docs-check passed. Strict format-lint failure reproduces on the clean base; recorded as PROPOSED FOLLOW-UP. Docs image import deferred until master CI publishes an accepted artifact; recorded as PROPOSED FOLLOW-UP. No epic-symbol entries remained.

## Dependencies

- **Depends on:** [bob-cli-f6.3](bob-cli-f6.3.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-f6.4](bob-cli-f6.4.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-f6.7](bob-cli-f6.7.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f6.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-f6.8.md) | [bob-cli-f6.8](bob-cli-f6.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@f520515`](https://github.com/bobs-org/bob-mac-capture/commit/f5205151da4da2ca1643eef3df2c8c16c2f33d37) | fix(mac-capture): restore the conflict JSON brace in the event-conflict decode test | [bob-cli-f6.8](bob-cli-f6.8.md) | 2026-11-01 19:58:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f6.8--4][1] | Need phase scope, notes and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-f6.8.md

<!-- sase:referenced-by:end -->
