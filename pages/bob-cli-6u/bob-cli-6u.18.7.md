# Bead: bob-cli-6u.18.7 — Finish ^prj project blocking — fix what the bob-cli-6u.18 land audit found

[Bead Pages](../README.md) / [bob-cli-6u.18](bob-cli-6u.18.md) / bob-cli-6u.18.7

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.land.md) · **Assignee:** `bob-cli-6u.18.7.land`
**Created:** 2026-10-12 20:32:25 EDT
**Plan:** [202610/prj\_line\_blocking\_land\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_land_audit_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/prj_line_blocking_land_audit_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_land_audit_fixes.md

<!-- sase:links:end -->

## Description

Every defect the bob-cli-6u.18 land audit found in the ^prj project-blocking fixes is fixed in bob-cli and bob-plugins, with regression tests that fail on the old code. bob-cli `just check` fails only the bob-cli-6m percent-listen tests. bob-plugins `npm test` fails only the known bob-cli-6v, bob-cli-6w and bob-cli-3w cases. The fixed bob and plugins are installed on this host and, when it is reachable, on the MacBook.

## Notes

[2026-10-13T02:05:46Z · bob-cli-6u.18.7.land] FOLLOW-UP TRIAGE (land agent): the only PROPOSED FOLLOW-UP notes (bob-cli-6u.18.7.1, .2, .3) are the two capture::r#ref percent-listen CLI failures = duplicate of bob-cli-6m; no new task, +1 recorded with land repro on 12abfd7 (1410 CLI pass / 2 fail). 6u.18.7.4 and .5 proposed nothing. Declined as non-follow-ups: (a) nav reversal prepareDependencyTargetNote may mint a block id on a target note before the parent write — unchanged since before a7fafed and benign (an idempotent block-id mint, no dangling link); (b) references.rs resident-edge filter keys by note path rather than the [id::] rule — differs only when one [id::] value exists in two notes, an id collision the plugins already refuse; low severity, not worth a task. Everything else the land audit found is epic-caused and stays epic work (see the remaining-work plan).

[2026-10-13T02:08:55Z · bob-cli-6u.18.7.land] LAND VERIFICATION (steps 1-2, land agent 2026-10-13): Integration: no non-epic commits landed in bob-cli (since b09612e; only e45c3ab, 1851d77, d2836e0, 12abfd7) or bob-plugins (since a7fafed; only 39fd9b1, d34e078), so nothing to integrate. Baseline: bob-cli 12abfd7 just check = only the bob-cli-6m pair (1410 CLI / 2452 lib pass). epic-symbols: none. Source audit of every phase commit confirmed most items but found epic-caused gaps: 6u.18.7.1 (d2836e0) moved the PDR7 field-name gate into the shared helper so a ^prj Depends-On line link into its own note no longer warns (contradicts PDR7/§13.2/§13.6; test flipped), recovery_tests.rs CRLF assertion never strengthened (reported done), PDB4/PDB6 variants dropped, and the task_complete close paths still match ^PRJ case-insensitively; 6u.18.7.2 (e45c3ab) nested link_guard leaks removed_pomodoro_links/day_file, consumed @r:id human printer untested, + rendering treats unconfigured statuses as open, docs/capture.md wrong at link-then-close/@r:id day_file/Ensure Next; 6u.18.7.3 (d34e078) the ? gate in promoteMovePrerequisiteTarget runs before the ^prj walk-through so the consistent [?] Q ^prj case promotes nothing, post-write reversal link-rewrite failures are swallowed and the project note trashed anyway, schedule-tag and counted/roll recovery tests pass on a7fafed, Task Link batch (500) recovery-writer test missing; 6u.18.7.4 (39fd9b1) projectHasRemainingBlockingReason treats every cross-note Depends-On id as open so Alt+] recovers residents only for dependency-free ^prj, Alt+[ to Cancelled and transcluded ^prj skip resident recovery, block-id resident case not split, cycler README row still nav text. 6u.18.7.5: host rollout verified (bob 12abfd7, 6 plugins 0 drift); MacBook unreachable again (ssh timed out at land time), Mac install unverified and Mac plugins not synced. Remaining work planned as child epic 'Finish ^prj project blocking — fix what the bob-cli-6u.18.7 land audit found' (parent_bead bob-cli-6u.18.7).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.land.md) | [bob-cli-6u.18.7](bob-cli-6u.18.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.7.3][1] | Need epic DECISIONS and sibling phase status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.3/README.md

<!-- sase:referenced-by:end -->
