# Bead: bob-cli-gl.5.1 — Complete capture project-note move execution

[Bead Pages](../README.md) / [bob-cli-gl.5](bob-cli-gl.5.md) / bob-cli-gl.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-gl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.md) · **Assignee:** `bob-cli-gl.5.1.land`
**Created:** 2026-11-03 16:14:53 EST · **Closed:** 2026-11-03 21:26:52 EST
**Plan:** [202611/capture\_move\_execution.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_execution.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_move_execution.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_execution.md

<!-- sase:links:end -->

## Description

Project-note capture moves complete parent task blocks atomically, links and offers them in draft order, and reports accurate previews and CLI output for bob-cli-gl.5.

## Notes

[2026-11-04T01:35:46Z · bob-cli-gl.5.1.land] LAND AUDIT: Read the epic, all three children and every note, both governing plan artifacts, source and epic commits 6650faa3/14a57732/ddb0a73f. DECISIONS honored: retain landed grammar bump, no further revision or schema bump, no memory edits. Stable topological writes, collision refusal, snapshot guards, rollback, staged chains, slot rendering, dependency repairs and base MV coverage are present. Current master equals origin/master at ddb0a73f. Reviewed intervening transplant, note-pull settlement, target-run activation, attachment catalog, merge-preparation and split commits. No stale epic-symbol entries for gl.5.1 or parent phase gl.5; no symvision recipe. Landing remains open: isolated CLI probes confirm hidden-offer off-by-one eligibility (hidden a selected by -p all, visible a suppressed by following hidden b), raw substring/live-link errors (prose mention or co-moved ab suppresses colon a; historical link suppresses offer after earlier item loads day), and stale moved-task landing lines after a dependency-drop removes child text (c reports 15, actual 14). Also investigate inherited blocking and preserve the newer batch offer-settlement path. A medium repair tale will own remaining code and complete gl.5.1 plus only parent phase gl.5.

[2026-11-04T01:38:50Z · bob-cli-gl.5.1.land] REMAINING WORK CONFIRMED: With write_toggle_task_settings-equivalent status config, parent cash is an active project with a future scheduled ^prj and Blocked tagged resident ^a: direct @cash:a correctly returns project_schedule, but Project @cash^x@ + - :a creates a link and makes a Next because the new ^prj has no inherited-block proxy. Also integration probe @cash+a @cash+b A shared note, blank line, Project @cash^x@, - ^a panics at capture/task_blocks.rs:163 (tracked task headline lost without a ref), exit 101 even for dry-run; vault unchanged. Project moves do not feed TaskBlockTracker remapping, unlike inbox moves. A mixed note-pull then project-move dry-run succeeds and writes nothing. These defects belong to this epic and must be repaired before close.

[2026-11-04T01:39:23Z · bob-cli-gl.5.1.land] FOLLOW-UP TRIAGE (sase_new_task): Reviewed all PROPOSED FOLLOW-UP entries and same-type/all-type searches, recent task sweeps, and active-epic scopes. gl.5.1.2 notes #1-2 are one catalog-count issue already corroborated on bob-cli-de; dd90f8c7 repairs both assertions to 69, so decline a new duplicate or stale +1 and record resolution evidence there. gl.5.1.3 note #1 docs generation still fails unchanged on ddb0a73f; attached independent just docs-check reproduction to causal owner bob-cli-go (same issue as its notes #1-2), no separate task and no memory edits. gl.5.1.3 note #3 unused prepare_task_merge import is resolved by 672954d4 and absent from current clippy errors; decline new task or duplicate escalation. Current check additionally finds five task-split/command-shell lint failures from 734214e9, recorded with run 21a7758643f1dbbd1810737832a1c896 on active bob-cli-go, no standalone task. gl.5.1.3 timing note #2 is adequate labeled synthetic-fixture evidence (72.64 ms median); no follow-up required. Retain these outcomes in the eventual close note. Existing phase completion notes verify their basic implemented cases, but the confirmed move defects in landing notes remain this epic work, not follow-up tasks.

[2026-11-04T01:41:31Z · bob-cli-gl.5.1.land] Focused verification on ddb0a73f completed: cargo test -q -p bob-obsidian --test cli project_note passed 79/79; catalog::protocol_1_parses_with_schema_version_one passed 1/1. These cover existing behavior but lack the five reproduced repair families. The inherited-blocking comparison is confirmed using recognized custom statuses: direct @cash:a guards a future-scheduled parent resident, while moving it through - :a bypasses the guard. The medium repair tale covers tracker integration, exact live-link semantics, hidden eligibility, inherited blocking and final move metadata; its final step closes this epic and only parent phase bob-cli-gl.5.

[2026-11-04T02:26:52Z · bob-cli-gl.5.1.land] Completed capture move landing repairs: tracker remap forwards moved/carried roots before Myers (dry-run agrees, no writes, shared note preserved); exact ledger identities for follows/offers (prose/historical/fenced/struck/nested ignored, prefix ab vs a fixed, staged-aware day loading, candidates frozen up front, net pass retained); hidden off-by-one fixed (1-based MovableRoot vs 0-based lines, hidden folds, explicit hidden moves still move, no daily-note requirement when no links); inherited blocking via staged parent schedule/proxy with child ^prj+residents [?]+tag, colon moves stay unlinked with truthful guards, local-only MV16 still links, needs_reconcile preserved; re-resolve all moved rows by block ID after links plus followed entry refresh and offer sync. Intervening integration reviewed since ddb0a73f. Checks: 5 new focused regressions pass; existing project_note 84 pass; just check has only the 5 pre-existing task-split clippy errors from 734214e9 already on bob-cli-go (unchanged, no new task); docs-check lint passes, generated drift fails on pre-existing glossary/task-merge frontmatter already on bob-cli-go (no new task, no memory edits). No new syntax, no Mac work, grammar rev 9 retained, additive envelope kept.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.land.md) | [bob-cli-gl.5.1](bob-cli-gl.5.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b738d8f`](https://github.com/bobs-org/bob-cli/commit/b738d8f23b21ac855d83745bdd415af52dfbdc98) | feat(capture): repair project-note move landing integration | [bob-cli-gl.5.1](bob-cli-gl.5.1.md) | 2026-11-03 21:29:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.5.1.1--2][1] | Review governing epic DECISIONS before phase closure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.1.md

<!-- sase:referenced-by:end -->
