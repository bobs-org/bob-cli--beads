# Bead: bob-cli-6u.18.4 — Navigation-hotkeys project-blocking fixes

[Bead Pages](../README.md) / [bob-cli-6u.18](bob-cli-6u.18.md) / bob-cli-6u.18.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.land.md) · **Assignee:** `bob-cli-6u.18.4` · **Size:** medium
**Created:** 2026-10-12 18:07:06 EDT · **Closed:** 2026-10-12 18:41:21 EDT
**Plan:** [202610/prj\_line\_blocking\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_landing_fixes.md)

## Description

nav-fixes: resident recovery only from a blocked ^prj, resident cycle edges when ^prj gains a prerequisite, tag drift in schedule and move paths, [unblocked::] and emptied-entry cleanup on counted/batch paths, conversion and move gaps, lenient frontmatter scheduled, out-of-scope skip flags, docs.

## Notes

[2026-10-12T22:41:21Z · bob-cli-6u.18.4] nav-fixes done in linked bob-plugins (nav 2.24.0->2.25.0) + bob-cli docs. All 10 items: (1) resident recovery gated on pre-gesture [?] ^prj and tagged-only residents; (2) stage guard + vault-commit guard trial implicit resident->X edges via dependent.projectResidentKeys; (3) due/deleted schedules keep #prj_is_blocked while ^prj holds Depends-On links, closed lines never edited in move/reversal; (4) markUnblockedLine on every counted/batch path (560/570/500/070/420) with removeEmptiedEntries on 560 cleanups, counted recoveries write [unblocked::] (^prj own line excluded); (5) forward conversion seeds Ready unless carried open prereq/future date with pre-seed lane transfer, reversal repoints #^prj before Pomodoro cleanup, moves promote verifiable-open prereqs with Blocked/Ready counts in move/route/reversal notices, insert after Cancel Log subtree; (6) frontmatter scheduled ignored; (7) isDailyNote/isToday threaded, null writer lets v12-missing warn fire; (9) cycler README row restored, stale frontmatter comments fixed. Verified: npm run build ok, npm run validate 6/6, npm test 2525/2531 with only the 6 allowed pre-epic failures (4 unblocked-glyph bob-cli-6v incl. base-tree repro, Keep-once bob-cli-6w, ranker timing flake), 18 new regression tests green, deployed on this host via bob plugins sync (vault main.js+manifest at 2.25.0). bob-cli change is docs/task-dependencies.md only (comment refs, no Rust). No epic-symbols entries.

## Dependencies

- **Blocks:** [bob-cli-6u.18.6](bob-cli-6u.18.6.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.4/README.md) | [bob-cli-6u.18.4](bob-cli-6u.18.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`524073e`](https://github.com/bobs-org/bob-cli/commit/524073e5775d9f4e851c40c0a0e572d1111dee63) | docs(task-deps): record nav-fixes ^prj blocking corrections | [bob-cli-6u.18.4](bob-cli-6u.18.4.md) | 2026-10-12 18:44:33 EDT |
| bob-plugins | [`bob-plugins@a7fafed`](https://github.com/bobs-org/bob-plugins/commit/a7fafedb34bb8bd0348ea14c74a276fd6749d368) | feat(navigation): land nav-fixes ^prj blocking corrections | [bob-cli-6u.18.4](bob-cli-6u.18.4.md) | 2026-10-12 18:49:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.4/README.md

<!-- sase:referenced-by:end -->
