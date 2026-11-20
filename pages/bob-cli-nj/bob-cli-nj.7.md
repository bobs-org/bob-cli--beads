# Bead: bob-cli-nj.7 — bob-mac-capture: inline Work Log recall in the completion popup

[Bead Pages](../README.md) / [bob-cli-nj](README.md) / bob-cli-nj.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.f3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.f3.md) · **Assignee:** `bob-cli-nj.7` · **Size:** medium
**Created:** 2026-11-19 12:14:03 EST · **Closed:** 2026-11-19 16:40:39 EST
**Plan:** [202611/log\_reason\_recall.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/log_reason_recall.md)

## Description

mac-worklog-recall: request completion inside close-log summary spans, decode the `work_log` context, and render USED BEFORE history rows. Return accepts only a selected row; otherwise it keeps today's behavior. Gate on exact-SHA macOS CI.

## Notes

[2026-11-19T21:40:16Z · bob-cli-nj.7] PROPOSED FOLLOW-UP: macOS CI Test step fails 6 pre-existing CapturePullInRecallTests (nj.5 pull-in cancel recall setup: activeReasonKey nil at CapturePullInRecallTests.swift:33) identically on clean base e58a9e27 (run 44603120124, 23 failures) and on this phase head b6b7f6cf (rerun of 44613921772, 23 failures, zero new failures); needs a task bead and owner

[2026-11-19T21:40:23Z · bob-cli-nj.7] PROPOSED FOLLOW-UP: just docs-check reference budget overage is pre-existing (capture-previews 6096 words and keyboard 6027 words over the 6000 cap at base e58a9e27; this phase adds ~75 more)

[2026-11-19T21:40:39Z · bob-cli-nj.7] Inline Work Log recall shipped in b6b7f6cf (fix on ddeab6c8): completion requests inside pomodoro_close_log_summary spans, work_log context decodes with no selection, USED BEFORE popup rows with N× · age metadata, Return keeps capture-as-typed without selection. Verified: portable-check 2626 tests pass on athena; exact-SHA macOS CI rerun 44613921772: all 10 new tests green, zero new failures (6 failing pull-in recall cases + docs-check budget overage reproduce identically on clean base e58a9e27, recorded as PROPOSED FOLLOW-UP notes). One transient DotRouteAlias timing failure passed on rerun.

## Dependencies

- **Depends on:** [bob-cli-nj.5](bob-cli-nj.5.md) ✓ · ⧖ 2026-11-19
- **Depends on:** [bob-cli-nj.6](bob-cli-nj.6.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nj.8](bob-cli-nj.8.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nj.7.md) | [bob-cli-nj.7](bob-cli-nj.7.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@ddeab6c`](https://github.com/bobs-org/bob-mac-capture/commit/ddeab6c8d3e5e4400dabd569f678df5c62f2299f) | feat(capture): inline Work Log recall in the completion popup | [bob-cli-nj.7](bob-cli-nj.7.md) | 2026-11-19 15:49:25 EST |
| bob-mac-capture | [`bob-mac-capture@b6b7f6c`](https://github.com/bobs-org/bob-mac-capture/commit/b6b7f6cf23b70060c8fab0d4c088a80ed66e90e5) | fix(tests): pass work\_log response init arguments in order | [bob-cli-nj.7](bob-cli-nj.7.md) | 2026-11-19 15:57:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.4.1.land][1] | Need the phase scope behind the newly measured Mac reference growth | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nh.4.1.land/README.md

<!-- sase:referenced-by:end -->
