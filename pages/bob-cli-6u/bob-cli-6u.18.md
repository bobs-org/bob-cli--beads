# Bead: bob-cli-6u.18 — Finish landing ^prj project blocking — fix the defects the land audit found

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.18

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.land.md) · **Assignee:** `bob-cli-6u.18.land`
**Created:** 2026-10-12 18:07:06 EDT
**Plan:** [202610/prj\_line\_blocking\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_landing_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/prj_line_blocking_landing_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_landing_fixes.md

<!-- sase:links:end -->

## Description

Every defect that bob-cli-6u (project blocking from the ^prj line, #prj_is_blocked, and [unblocked::]) introduced is fixed in bob-cli and bob-plugins. bob-cli `just check` fails only the bob-cli-6m percent-listen tests. bob-plugins `npm test` fails only the known pre-epic failures (bob-cli-6v, bob-cli-6w, plus the bob-cli-3w timing flake). The fixed bob and plugins are installed on the MacBook and on this host.

## Notes

[2026-10-13T00:24:18Z · bob-cli-6u.18.land] FOLLOW-UP TRIAGE (land agent): (a) percent-listen CLI failures proposed by 6u.18.1/.2/.3 = duplicate of bob-cli-6m; no new task, +1 recorded with land-agent repro on b09612e (ref.rs:942/:991, 1405 pass / 2 fail). (b) 6u.18.5 'revisit pre-epic plugin failures' = duplicates of bob-cli-6v (4 unblocked-glyph cases), bob-cli-6w (Keep counts once), bob-cli-3w (stage-ranker timing); no new task, +1 recorded on each with land-agent repro on bob-plugins a7fafed (npm test: exactly those 6 failures). No other PROPOSED FOLLOW-UP notes exist. Audit-found defects are epic-caused and stay epic work (child epic plan).

[2026-10-13T00:30:01Z · bob-cli-6u.18.land] MAC ROLLOUT (land agent, 2026-10-13): Mac reachable briefly; its bob-cli checkout was clean at 7a44aa7 (pre-6u.18), origin/master b09612e; bob plugins list there showed block-id-prompt/bob-navigation-hotkeys/task-status-cycler in drift. Started a detached 'git pull --ff-only && just install' on the Mac (log /tmp/bob-6u18-install.log); ssh then timed out repeatedly, so the install result and Mac dry-runs are UNVERIFIED and Mac plugins were NOT synced. The child epic's rollout phase owns finishing this.

[2026-10-13T00:31:55Z · bob-cli-6u.18.land] LAND VERIFICATION (steps 1-2): Integration: no non-epic commits landed in bob-cli (since 414b802) or bob-plugins (since f1d5a4e) after the epic started, so nothing to integrate. Baselines: bob-cli b09612e just check = only bob-cli-6m pair; bob-plugins a7fafed npm test = only 6v x4, 6w, 3w. epic-symbols: none (6u.18 and 6u). Source audit of every phase commit found epic-caused defects still open: 6u.18.1 (54ac68b) inherited resident edges ignore same-note filter, spurious/double project_internal_dependency warnings, internal-id filter ignores project recognition and over-matches block ids, CRLF/PDT10 tests pass on old code, no status-only-flip test, stale §12.10/§13.4/task-status-hooks docs; 6u.18.2 (b09612e) project_schedule_for_sync lets frontmatter scheduled bypass the hoist gate (live sync exit 1 with no ^prj), ^prj case-insensitive in blocking.rs only, docs overclaim, CRLF EOF insert; 6u.18.3 (53af9cb) toggle insert counts struck links (false link claim), hardcoded closed statuses in + rendering, consumed @r:id prints 'captured', fenced-index test does not catch the bug; 6u.18.4 (a7fafed) HIGH reversal rewrites #^prj links before the parent write (repro'd: fails where a7fafed^ succeeded), schedule tag kept when only closed Depends-On links remain, move promotion raises another project's ^prj (ADJ-11), README cycler row not restored, many requested tests missing; 6u.18.5 (f1d5a4e) recovery strips tag from closed lines, successor path still refuses recovery without ledger v12, block-id resident test retargeted, Alt+] clearing a ^prj date leaves residents tagged. Mac rollout (6u.18.6) unfinished. Planned as child epic 'Finish ^prj project blocking — fix what the bob-cli-6u.18 land audit found' (parent_bead bob-cli-6u.18).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.land.md) | [bob-cli-6u.18](bob-cli-6u.18.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.4][1] | need parent epic notes and remaining work | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.4/README.md

<!-- sase:referenced-by:end -->
