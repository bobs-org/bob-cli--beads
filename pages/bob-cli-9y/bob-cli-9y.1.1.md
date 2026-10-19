# Bead: bob-cli-9y.1.1 — Build bob task move with guarded writes and reference repair

[Bead Pages](../README.md) / [bob-cli-9y.1](bob-cli-9y.1.md) / bob-cli-9y.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-9y.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9y.1.md) · **Assignee:** `bob-cli-9y.1.1.land`
**Created:** 2026-10-19 16:37:59 EDT · **Closed:** 2026-10-19 19:24:45 EDT
**Plan:** [202610/task\_move.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_move.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/task_move.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_move.md

<!-- sase:links:end -->

## Description

Complete bob-cli-9y.1 with a dry-runnable bob task move that preserves task review state, repairs vault-wide references, and safely syncs scoped writes.

## Notes

[2026-10-19T22:28:11Z · bob-cli-9y.1.1.land] LANDING REVIEW: Read this epic, both children bob-cli-9y.1.1.1 and bob-cli-9y.1.1.2, every child note, plan:202610/task_move.md, and the authoritative move-cli section of plan:202610/sase_hub_split.md. Reviewed commits bfca3419 and 8b0f3782 and the planner, live adapter, shared archive helpers, tests, routing/completion and documentation. The temporary test-only production gate is removed; task state preservation, explicit reconciliation, destination-first/source-last ordering, full read-set/membership guards, scoped commits and documented surfaces are present. Parent decisions later_notes=hub, move_in_flight=yes, installs_backlog=yes, personal_homes=routed, widen_plans_prj=yes remain honored; no vault migration or memory edits belong here. Fetched origin: master and origin/master are 8b0f3782; bfca3419..origin/master contains only the epic's own second commit, so no unrelated post-start integration was needed.

Remaining epic work found by source inspection: the CLI selector ArgGroup omits multiple(true), contradicting mixed -b/-m support; tasks_intake_insert_byte scans fenced task examples/headings and inserts after the last task rather than the last intake line; command note resolution can fall back from a nonexistent explicit path and silently prefer a root note for an ambiguous bare stem; CLI resolution and the case-sensitive archive resolver used for self-dependency/link repair disagree; final dependency-id errors become empty strings and vault-wide encoded identity collisions are not checked; only the first existing id field is validated; moved anchor enumeration and Markdown-link repair can mutate authored code examples. The live adapter erases typed initial-scan errors before the retry loop, and an existing partial-apply error suppresses later commit errors. Required normal sync/peer drift, pre-write staging failure, early partial outcome, conflict, and move-then-archive/reconcile integration coverage is incomplete. These are remaining requirements of this epic, not separate follow-ups. A medium tale will repair them and finish this epic and parent phase in its own turn.

Verification evidence: child bob-cli-9y.1.1.2 note reports a just check pass; I did not rerun the full gate or claim a new pass. A temporary-fixture runtime probe could not start because the current CARGO_TARGET_DIR has no built bob binary; fixtures were removed. No live vault was accessed. sase bead epic-symbols bob-cli-9y.1.1 found no entries; this checkout has no symvision recipe.

[2026-10-19T22:28:15Z · bob-cli-9y.1.1.land] FOLLOW-UP TRIAGE BEFORE REPAIR TALE: Reviewed every note on proposing phases bob-cli-9y.1.1.1 and bob-cli-9y.1.1.2. Neither contains a PROPOSED FOLLOW-UP entry (zero proposals). No independent out-of-scope follow-up was found: all landing gaps recorded above are caused by the new mover or are unmet requirements of its approved plan, including unsafe reuse in this command. Thus no duplicate corroboration, active-epic attachment outside this epic, new task creation, or declined proposal is needed. Keep these fixes on bob-cli-9y.1.1. The repair coder must include this triage outcome in the close note.

[2026-10-19T23:24:45Z · bob-cli-9y.1.1.land] Landing repairs complete; nested epic bob-cli-9y.1.1 is done.

Read this epic, closed children bob-cli-9y.1.1.1 and bob-cli-9y.1.1.2, every child note, plan:202610/task_move.md, plan:202610/task_move_landing_repairs.md, and the authoritative move-cli section of plan:202610/sase_hub_split.md. Reviewed notes/decisions task-move-never-advances-the-walk, task-status-is-derived, task-lanes-are-sticky, task-deps-are-depends-on-links, projects-block-from-prj-line, ready-is-freshness-gated, today-is-read-from-the-ledger, plus cli_rules, sase_beads, sase_artifacts, and glossary terms for task-dependency-link, task-link, project-note, project-task, task-freshness, and area-note. Parent decisions later_notes=hub, move_in_flight=yes, installs_backlog=yes, personal_homes=routed, widen_plans_prj=yes remain honored. No vault migration, plugin, or memory edits.

Original commits: bfca3419 (pure planner) and 8b0f3782 (guarded command). This tale kept command, pure planner, guarded writer, and JSON schema v1, and repaired the remaining epic gaps: clap ArgGroup multiple(true) for mixed -b/-m; mover-specific resolve_note (explicit-path case-insensitive exact match, no basename fallback, ambiguous bare stems); Markdown-aware intake (unfenced ## Tasks body, badge strip, dest EOF); live identities and link repair skip fences/frontmatter/inline code; required_dependency_id plus validate_mapped_identities before rewrite (encoded collisions, every live [id::], unrepresentable dest); typed ScanError retry of CaptureError::Unstable; Report::fail additive warnings for secondary commit/sync after a retained primary partial-apply error; destination-first/source-last via output_rank.

Follow-up triage (epic note #2): proposing phases bob-cli-9y.1.1.1 and bob-cli-9y.1.1.2 contain zero PROPOSED FOLLOW-UP entries; remaining gaps were unfinished epic requirements, not new tasks. No independent out-of-scope follow-up, duplicate corroboration outside the ETXTBSY flake, or declined proposal.

Post-start origin: HEAD is still 8b0f3782; origin/master is f0f6e0c5. Range bfca3419..origin/master is 8b0f3782 then c7df845f (MIT license, Cargo.toml+LICENSE) then f0f6e0c5 (docs package/contract site). Neither later commit touches mover code; f0f6e0c5 already lists stem task-move in docs/_meta/contracts.yml and mkdocs nav from 8b0f3782. No mover integration required.

Verification: cargo test --lib task_move 47 passed; cargo test --lib collect_done 69 passed; cargo test --test cli mover/archive/help/completion filter 31 passed. Landing-repair coverage includes clap mixed selectors; missing selector exit 2; Report::fail primary+warning; retryable/fatal/zero-budget scans; fail_staging recovery; dest-then-fail deferred source/backlinks; ordinary commit-msg hook skips post-sync; secondary commit after partial apply; planner explicit-path/missing-path/case-variant dest-prj; intake after prose/fenced examples/badge strip; dest without final newline; fenced identities; encoded collision; unrepresentable dest space.md; stale second [id::]; nested child/co-move review fields; CLI mixed selectors; Git dry-run; identity refusals write nothing; ordinary commit failure -o; pre-sync peer snapshot with scoped move commit; post-sync conflict remote-wins plus _conflicts/ and standing local commit; co-move then bob task reconcile -r 0 via write_blocked_tasks_settings. randomize_post_sync_conflict_keeps_local_commit_and_warns ok. First just check failed only the unrelated ETXTBSY flake native::highlights_ref::fetch::tests::curl_pins_the_checked_address_with_resolve (Text file busy); isolated rerun passed; second just check passed (fmt, clippy, lib, 1860 CLI, dataview/gkeep/randomize/tasks parity). Corroborated semantic duplicate bob-cli-5l with +1; did not create a new task. sase bead epic-symbols bob-cli-9y.1.1 found no entries; just --summary has no symvision recipe. No live vault accessed. Parent phase bob-cli-9y.1 is closed in the same turn after this bead; outer epic bob-cli-9y stays open.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9y.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9y.1.1.land.md) | [bob-cli-9y.1.1](bob-cli-9y.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`24f4395`](https://github.com/bobs-org/bob-cli/commit/24f43958e8b9ba5d05b5210298a8ac8ad2bf26f5) | fix(task-move): repair landing gaps for selectors, identities, and sync | [bob-cli-9y.1.1](bob-cli-9y.1.1.md) | 2026-10-19 19:26:33 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9y.1.1.1][1] | Need parent epic DECISIONS and design for move-planner phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9y.1.1.1/README.md

<!-- sase:referenced-by:end -->
