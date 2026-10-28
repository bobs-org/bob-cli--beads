# Bead: bob-cli-df.4.1 — Preserve full worktrees across failed-close relaunches

[Bead Pages](../README.md) / [bob-cli-df.4](bob-cli-df.4.md) / bob-cli-df.4.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.md) · **Assignee:** `bob-cli-df.4.1.land`
**Created:** 2026-10-27 21:39:18 EDT
**Plan:** [202610/preserve\_failed\_close\_worktrees.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/preserve_failed_close_worktrees.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/preserve_failed_close_worktrees.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:40409c9e03e43f92b43cbaf8 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/preserve_failed_close_worktrees.md

<!-- sase:links:end -->

## Description

Failed finalization and subsequent workspace preparation retain recoverable tracked, staged, and untracked work before destructive Git operations, with durable recovery locations in failure evidence.

## Notes

[2026-10-28T03:53:09Z · bob-cli-df.4.1.land] LAND AUDIT / FOLLOW-UP TRIAGE (before remaining-work tale): reviewed all notes on this epic and phases .1-.4, both linked plans, actual source/tests, and commits 42512dc116 (snapshot), 55ebb614f2 (relaunch), 2bb3e813d3 (reset replay), dcb7d2a6e7 (failed-close evidence). Clean external SASE checkout fast-forwarded from daf54c5b2d to origin/master dcb7d2a6e7. The sole non-epic commit since the first epic commit is 067eeeb17b (Footprint facades, core pin, docs, whitelist); no new recovery caller/conflict, but it re-keys Overlay/load_overlay to open sase-1p1.8. No discretionary DECISIONS or memory edits were authorized. FOLLOW-UP DISPOSITIONS: .1 #2/.2 #1/.3 #1/.4 #1 Symvision reports consolidated into a DISCOVERED ISSUE note on active causal epic sase-1p1 and supplementary impact on existing sase-o7; no new task. Overlay/load_overlay part declined as already re-keyed to audited open .8; other_id/custom_id now have production callers but remain exempted, for Footprint to resolve. .1 #3/.3 #2/.4 #1 missing plans sidecar independently reproduced by sase validate on clean dcb7d2a6e7 (only failed stage plan links validate, invalid-root); new large ready bug bob-cli-dg after duplicate and active-epic triage. .4 #1 close_provenance API-change proposal declined as stale-environment evidence: current installed sase-core-rs 0.43.0 bead_close has the tenth close_provenance parameter; the original 0.42.7 failure is not evidence to alter the facade. The tale must provision its isolated test environment and actually execute the previously blocked end-to-end tests. REMAINING EPIC WORK reproduced: delete/modify DU conflict (stages 1 and 3, no stage 2) snapshot succeeds but restore omits unique edited conflict.txt; and a clean parent ignoring sase/repos permits recreate_managed_workspace to delete a dirty linked child after rescue_git_repo returns None. These violate the approved conflict and nested-repository guarantees, so epic and parent df.4 stay open. epic-symbols bob-cli-df.4.1 currently empty. No source changes, full gate, or successful landing claimed.

[2026-10-28T03:57:20Z · bob-cli-df.4.1.land] Remaining-work evidence is file:explicit:40409c9e03e43f92b43cbaf8. Authored one medium tale, Finish failed-close preservation and land bob-cli-df.4.1, for conflict-stage worktree coverage and strict nested-repository preservation before relaunch/reclone/clear removal. Validation with --explain identified missing required title/goal and an inert tale parent_bead field; corrected them and revalidated successfully with zero warnings. The tale explicitly owns this epic close, post-close Symvision, original plan status done, and normal close of parent phase bob-cli-df.4; it must not close df or cv, and must not wait on its own future commit. No source changes or full test pass claimed; submitting through sase plan propose.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.land.md) | [bob-cli-df.4.1](bob-cli-df.4.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.4.1.1--1][1] | Need DECISIONS from parent epic | 1 |
| read-by | [agent:bob-cli-df.4.1.3][2] | Need epic DECISIONS and plan context for phase 4.1.3 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md

<!-- sase:referenced-by:end -->
