# Bead: bob-cli-pw.8.1.2 — First-class Meetings kind in Bob Refs

[Bead Pages](../README.md) / [bob-cli-pw.8.1](bob-cli-pw.8.1.md) / bob-cli-pw.8.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pw.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.8.md) · **Assignee:** `bob-cli-pw.8.1.2` · **Size:** small
**Created:** 2026-11-24 23:55:02 EST · **Closed:** 2026-11-25 00:47:03 EST
**Plan:** [202611/mac\_meeting\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_meeting_notes.md)

## Description

meetings-library: add RefKind.meeting, the Meetings scope on Command-6, presentation and search coverage, synthetic tests, and the Bob Refs documentation in bob-mac-capture.

## Notes

[2026-11-25T05:04:24Z · bob-cli-pw.8.1.2] PROPOSED FOLLOW-UP: Reduce existing word-budget overruns in docs/develop/plugins/plugin-apis.md (9287/8000 words) and docs/reference/plugins/bob-navigation-hotkeys.md (6029/6000 words); just docs-check fails on these untouched pages.

[2026-11-25T05:47:03Z · bob-cli-pw.8.1.2--3] Completed Meetings library phase. Passing gates: Athena just portable-check (2,712 tests passed, 1 skipped); exact-SHA macOS CI run 45553473212 at 1f639b9ee79a8058754ee1e2c7dc2a03d19b85da passed lint and Build, and phase RefsCore/Meetings tests passed. Overall CI Test step failed only at RefsPanelModelTests.testHighlightsTaskFallbackShowKeepsTabsAndBannerUntilLibraryRestores (expected query 'small', actual 'small_reading'); the identical assertion also failed on base c8692ed363408ae398516fc1b0c50787b0425961 CI run 45552044521, so this predates the phase. Mac scratch bundle/typecheck was unavailable: SSH to the Mac timed out. Previously recorded docs-check issue remains: just docs-check fails on untouched plugin-apis.md (9287/8000 words) and bob-navigation-hotkeys.md (6029/6000 words). No epic symbols remained.

## Dependencies

- **Blocks:** [bob-cli-pw.8.1.3](bob-cli-pw.8.1.3.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pw.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.8.1.2.md) | [bob-cli-pw.8.1.2](bob-cli-pw.8.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c8692ed`](https://github.com/bobs-org/bob-mac-capture/commit/c8692ed363408ae398516fc1b0c50787b0425961) | feat(refs): add Meetings library scope | [bob-cli-pw.8.1.2](bob-cli-pw.8.1.2.md) | 2026-11-25 00:13:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pw.8.1.2--1][1] | Need the phase scope, design file, notes, and prior work status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.8.1.2.md

<!-- sase:referenced-by:end -->
