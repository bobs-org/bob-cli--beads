# Bead: bob-cli-9k.6 — Where the time went panel on dash\_stats.md

[Bead Pages](../README.md) / [bob-cli-9k](README.md) / bob-cli-9k.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4t.linker.w0.md) · **Assignee:** `bob-cli-9k.6` · **Size:** medium
**Created:** 2026-10-18 16:35:49 EDT · **Closed:** 2026-10-18 19:44:17 EDT
**Plan:** [202610/pomodoro\_homes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:b50fabd7793647c91cc93653 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

stats-panel: replace the "by theme" pomodoro context panel with an Areas & projects view (area bar, projects grouped by area, apportioned tint, buckets, drill-down, pinned-day filter) and keep Themes one click away. Show the same table for task metrics, add preview fixtures and tests, then sync.

## Notes

[2026-10-18T23:42:59Z · bob-cli-9k.6] PROPOSED FOLLOW-UP: The Bob Plugins full suite still has six unrelated CI failures: four unblocked-glyph cases (bob-cli-6v), Keep counts once (bob-cli-6w), and forward/reverse project conversion (bob-cli-7i). All six reproduced from clean bob-plugins HEAD 0ffb3e075d48 in the isolated affected-file run (39 passed, 6 failed); the full suite reported 3098 passed and 6 failed. Independent evidence is attached to those existing tasks and summarized in file:explicit:b50fabd7793647c91cc93653.

[2026-10-18T23:44:17Z · bob-cli-9k.6] Implemented the Areas & projects and Themes Stats views, task home breakdowns, session drill-down, catalog labels, and preview fixtures; bumped bob-ledger-tools to 1.57.0 and updated docs. Focused Stats tests pass 32/32; browser preview matrix was reviewed at wide light and narrow dark; npm run validate passes 7/7 plugins. Full npm test reported 3098/3104 passing; its six failures reproduced on clean bob-plugins HEAD 0ffb3e075d48 and were corroborated to existing beads bob-cli-6v, bob-cli-6w, and bob-cli-7i. Live 4w/3m/1y area palettes report no hue collisions. Synced the opened linked checkout to ~/bob (3 files copied); follow-up dry run reports all 3 unchanged. epic-symbols is empty.

## Dependencies

- **Depends on:** [bob-cli-9k.3](bob-cli-9k.3.md) ✓ · ⧖ 2026-10-18
- **Depends on:** [bob-cli-9k.5](bob-cli-9k.5.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.6/README.md) | [bob-cli-9k.6](bob-cli-9k.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1933d54`](https://github.com/bobs-org/bob-cli/commit/1933d544e224e92e05ca8a94b60c9e8e08538cdb) | docs(stats): document area and project attribution | [bob-cli-9k.6](bob-cli-9k.6.md) | 2026-10-18 19:45:02 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.6][1] | Need phase notes before deciding whether this phase can be completed by one agent | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.6/README.md

<!-- sase:referenced-by:end -->
