# Bead: bob-cli-f6.4 — bob-cli: warn when non-MEET sessions run past an Event Task

[Bead Pages](../README.md) / [bob-cli-f6](README.md) / bob-cli-f6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bv](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bv.md) · **Assignee:** `bob-cli-f6.4` · **Size:** medium
**Created:** 2026-11-01 11:24:14 EST · **Closed:** 2026-11-01 16:04:25 EST
**Plan:** [202611/untracked\_calendar\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/untracked_calendar_events.md)

## Description

event-start-warnings: structured run-past-event warnings with fit drafts for starts, adjusts, and shifts of non-MEET sessions.

## Notes

[2026-11-01T21:03:54Z · bob-cli-f6.4] PROPOSED FOLLOW-UP: just lint fails on clean HEAD with clippy::filter_map_bool_then in src/native/capture_pomodoros_agenda.rs:1086 (same denial already noted on closed bob-cli-fb.2.1.2); this phase did not touch that file

[2026-11-01T21:04:25Z · bob-cli-f6.4] Verified: 5 event_conflict unit tests and 14 capture::event_start_warnings CLI tests (start/restart/swap/named/link/+N/-N/++/--/no-fit/chain/dry-run/human/MEET/own-lineup). cargo fmt --check and just docs-check pass. just lint fails identically on clean HEAD (clippy::filter_map_bool_then in capture_pomodoros_agenda.rs:1086; see PROPOSED FOLLOW-UP citing bob-cli-fb.2.1.2). No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-f6.3](bob-cli-f6.3.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f6.6](bob-cli-f6.6.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f6.8](bob-cli-f6.8.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.4/README.md) | [bob-cli-f6.4](bob-cli-f6.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`273e09a`](https://github.com/bobs-org/bob-cli/commit/273e09a7fd870f235c4cbe9ff6483b0909b5f778) | feat(capture): warn when a non-MEET session runs past an Event Task | [bob-cli-f6.4](bob-cli-f6.4.md) | 2026-11-01 16:38:31 EST |
| bob-cli | [`3980489`](https://github.com/bobs-org/bob-cli/commit/39804896ce402ae95e807badc03fc228c2a151ed) | fix(capture): keep keep-moving goldens and clippy green | [bob-cli-f6.4](bob-cli-f6.4.md) | 2026-11-01 16:40:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f6.4][1] | Need notes, description, and remaining work before implementing | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.4/README.md

<!-- sase:referenced-by:end -->
