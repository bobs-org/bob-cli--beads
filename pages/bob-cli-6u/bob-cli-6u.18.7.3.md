# Bead: bob-cli-6u.18.7.3 — Navigation-hotkeys reversal order, schedule tag, and move promotion fixes

[Bead Pages](../README.md) / [bob-cli-6u.18.7](bob-cli-6u.18.7.md) / bob-cli-6u.18.7.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.land.md) · **Assignee:** `bob-cli-6u.18.7.3` · **Size:** medium
**Created:** 2026-10-12 20:32:25 EDT · **Closed:** 2026-10-12 21:18:54 EDT
**Plan:** [202610/prj\_line\_blocking\_land\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_land_audit_fixes.md)

## Description

nav-fixes: write nothing before the reversal parent write, make the schedule tag follow ^prj status, never raise ^prj on move promotion, add the missing plugin-level tests, nav README row and bob-cli docs.

## Notes

[2026-10-13T01:18:36Z · bob-cli-6u.18.7.3] PROPOSED FOLLOW-UP: just check --test cli still fails the two capture::r#ref percent-listen tests (bob-cli-6m) identically on this tree — percent_listen_reference_runs_existing_worker_and_installs_audio and failed_percent_listen_worker_keeps_listen_retry_guidance; allowed by this epic, not caused by nav-fixes.

[2026-10-13T01:18:54Z · bob-cli-6u.18.7.3] Verified nav-fixes: reversal plans Pomodoro cleanup against #^prj and restored parent block id in memory, then writes parent first (Health.md Depends-On converts; rewrite-failure aborts with files unchanged; live Daily cleanup when parent is blocked). Schedule tag follows ^prj post-gesture status (closed Depends-On history does not keep #prj_is_blocked; Ctrl+D strips or keeps tags from remaining open links; counted ^prj schedule writes [unblocked::]). Move promotion walks through dest ^prj without raising it; only open tasks' Depends-On promote; per-task lanes (Q.md unchanged, R.md [*], X=[*] Y=[/], closed-task Depends-On not promoted). Plugin-level 6u.18.4 item-8 tests: commitVaultRefs refuses implicit resident-edge cycles; counted Depends-on and recommended roll recover with [unblocked::]; inbox route into blocked project tags the moved task; forward conversion carries Depends-On and reverse restores it. Docs: plugins README 2.26.0 nav row, task-dependencies §13.8/§13.10, projects.md conversion paragraph. Manifest 2.26.0; npm test 2543 pass / 6 allowed fail (bob-cli-6v/6w/3w); validate 6/6; deployed this host via bob plugins sync. just check --test cli fails only the two allowed capture::r#ref percent-listen tests (bob-cli-6m). epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-6u.18.7.5](bob-cli-6u.18.7.5.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.3/README.md) | [bob-cli-6u.18.7.3](bob-cli-6u.18.7.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`12abfd7`](https://github.com/bobs-org/bob-cli/commit/12abfd7a1888ed3c67c05e8bc19729359b086730) | docs(projects): document ^prj schedule tag and conversion seeding | [bob-cli-6u.18.7.3](bob-cli-6u.18.7.3.md) | 2026-10-12 21:20:15 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.7.3][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.3/README.md

<!-- sase:referenced-by:end -->
