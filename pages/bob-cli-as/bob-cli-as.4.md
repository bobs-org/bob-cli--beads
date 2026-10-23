# Bead: bob-cli-as.4 — Keep-reason prompt and combined write for a single keep

[Bead Pages](../README.md) / [bob-cli-as](README.md) / bob-cli-as.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.55.linker.w2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.55.linker.w2.md) · **Assignee:** `bob-cli-as.4` · **Size:** medium
**Created:** 2026-10-23 08:24:12 EDT · **Closed:** 2026-10-23 10:03:13 EDT
**Plan:** [202610/rotten\_log.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_log.md)

## Description

keep-single: build the shared keep-reason stage and prompt model, the counted-keep predicate, and the stamp-plus-log planner, then wire single-target Alt+F and Ctrl+Alt+F (including the card-unavailable fallback) through them.

## Notes

[2026-10-23T13:45:25Z · bob-cli-as.4] Implemented the single source-task keep reason stage/model, dry-run counted predicate, stamp-plus-log planner, stale-document/day guards, and shared card-unavailable fallback in linked bob-plugins (navigation 2.54.0). All 142 focused new/regression tests pass; the broader focused run is 158/159 with only the identical clean-base bob-cli-6w notice failure. Live Obsidian verification was attempted, but obsidian --help reports that Obsidian is not running. Final full npm test, docs check, and deployment remain as verification steps; no implementation work is known outstanding.

[2026-10-23T13:45:30Z · bob-cli-as.4] PROPOSED FOLLOW-UP: Existing plugin test failures still reproduce on clean base 1b1a5ba — bob-cli-6w (Keep notice receives the missing stats API notice), bob-cli-7i (reverse project conversion retains BLOCKS [[Work_ship#^prj]]), and bob-cli-6v (four wall-clock-dependent unblocked-glyph assertions). Independent clean-base worktree checks confirmed each failure; no statuses changed.

[2026-10-23T13:45:34Z · bob-cli-as.4] PROPOSED FOLLOW-UP: Corroborate bob-cli-3w — the navigation suite hit the stage-ranker 16 ms timing assertion at 16.60 ms; the unchanged isolated performance suite passed. Keep the existing performance-flake triage.

[2026-10-23T14:03:13Z · bob-cli-as.4--1] Completed single-task keep reason stage/model, exact counted-keep predicate, combined stamp-and-Rotten-Log planner, stale-note/day guards, and shared card-unavailable fallback in navigation 2.54.0. Verification: focused tests 142/142; full npm test 3484/3490 with only the six previously reproduced clean-base 1b1a5ba failures (bob-cli-6v x4, bob-cli-6w, bob-cli-7i), already recorded as PROPOSED FOLLOW-UP notes. All docs:check gates passed, including 447 documentation tests (1 optional-font skip); npm run build reports every generated plugin unchanged and git diff --check passes. Monitor 7q93vfspmx2p carries full verification evidence. Deployed navigation manifest/main/styles successfully via bob plugins sync --no-pull from the linked checkout. No epic-symbol entries remain. Live Obsidian verification was attempted earlier but unavailable because Obsidian is not running. Only this phase is closed; later card and batch phases remain out of scope.

## Dependencies

- **Depends on:** [bob-cli-as.3](bob-cli-as.3.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-as.5](bob-cli-as.5.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-as.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-as.4.md) | [bob-cli-as.4](bob-cli-as.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@22ec6b2`](https://github.com/bobs-org/bob-plugins/commit/22ec6b2f338700f96d25388ef24d81e950bea90f) | feat(navigation): log reasons for single-task rotten keeps | [bob-cli-as.4](bob-cli-as.4.md) | 2026-10-23 10:03:51 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-as.4--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-as.4.md

<!-- sase:referenced-by:end -->
