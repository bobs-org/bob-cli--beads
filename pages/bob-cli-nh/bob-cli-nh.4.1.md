# Bead: bob-cli-nh.4.1 — Preserve intention links through vault rewrites

[Bead Pages](../README.md) / [bob-cli-nh.4](bob-cli-nh.4.md) / bob-cli-nh.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.md) · **Assignee:** `bob-cli-nh.4.1.land`
**Created:** 2026-11-19 13:01:12 EST · **Closed:** 2026-11-19 18:51:50 EST
**Plan:** [202611/intention\_link\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/intention_link_repair.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/intention_link_repair.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/intention_link_repair.md

<!-- sase:links:end -->

## Description

Links inside daily and period intentions, summaries, and reflections survive archive, task, and reference rewrites with valid YAML and correct provenance; the shared periods problems report identifies malformed or stale period text.

## Notes

[2026-11-19T22:35:13Z · bob-cli-nh.4.1.land] LAND AUDIT / FOLLOW-UP TRIAGE (before remaining-work tale): Read this epic (no own DECISIONS or prior notes), all four child scopes and all six prior child notes, plan:202611/intention_link_repair.md and enclosing period_intentions.md, plus parent phase nh.4 and its final decisions. day_summary_cap=sixty remains intact; no memory edits, deployments, or live vault edits. Reviewed 749efc28 (typed repair/archive/digest carry), ea538f78 (reference rename/overwrite), 992fd33d (report-only findings/docs), and recovered task_repair 0f990b1d7fc39dec993aa7e921a72d78121dea59 from this checkout reflog: it was committed detached at 17:26, then checkout switched to master 992fd33d, leaving it absent from master/origin/master. Applied that commit with cherry-pick --no-commit, cleanly merging reference phase changes; finalizer will preserve this integration. cargo fmt --all -- --check and git diff --cached --check pass; integrated just check/docs-check and fixture acceptance are still pending, not claimed green. Caller inventory: archive moved-block/rename adapter; move pure planner shared by direct/capture/Gmail; merge copy-and-retire retains source anchors and bare-note relocation uses move; split vault postimages; ref rename plus overwrite identity/highlight/frozen paths; generic vault_rewrite callers themes rename/split/migrate, relation rename/reverse, periods ensure/migrate. Examined intervening 5b547f13/c94a718d bank imports (no target retargeting), a29a64f6 summary drafting (integration gap below), and earlier-since-creation logs/update/glossary work. Remaining source-confirmed gaps: reference canonical_frontmatter_end returns None for unclosed YAML so raw pass rewrites protected properties; repair_owned_postimages skips digest carry when only body links changed; split gates fragment repair on nonempty moved_targets and feeds individual lines, losing stayed-anchor qualification for minted selections and multiline fence/comment context; newer apply_with_review duplicates the old trim()-based delimiter rescan unlike corrected apply/split_document and can mistake an indented --- in a reflection scalar for the YAML close. A single medium tale will add regressions, fix these bounded paths, perform integrated acceptance, and close nh.4.1 then phase nh.4 in that coding turn. No epic symbols for nh.4.1 or nh.4; no symvision recipe presently. FOLLOW-UP OUTCOMES: .2 #1, .3 #1, .4 #2 are one repeated seven-test proposal, separated by causal owner: four capture expectations attached as DISCOVERED ISSUE to active nj (nj.6 ddf28f64); catalog/completion registration and wrong ordered-op assertion attached to active nh (nh.2 a0b91a8d). Source/history corroborated the agents' clean-base reproductions; no new task because active epics own these causes. .4 #1 docs overages corroborated existing ready bob-cli-jz (+1): independently counted Mac b6b7f6cf capture-previews 6171, keyboard 6027 vs 6000. Also attached +75 capture-previews growth from nj.7 ddeab6c8 (6096->6171) to active nj. No proposal discarded; duplicate new tasks declined because of these existing causal owners/duplicate. Task search across all statuses, last-week sweep, and active-epic review completed through sase_new_task.

[2026-11-19T22:37:10Z · bob-cli-nh.4.1.land] Remaining-work tale sase_plan_intention_link_landing.md validated with zero warnings after the required explain/edit/revalidate loop. It contains four bounded source fixes, integrated just check/docs-check and archive-to-problems acceptance, then normal closeout of this epic, its plan status, and parent phase bob-cli-nh.4 in the coding turn before finalization. Audit wording correction: reviewed all EIGHT child notes (1+2+2+3), not six. No current integrated Rust/doc gate pass is claimed; only formatting and diff checks passed. All proposed follow-ups were triaged and recorded in the preceding note before proposal.

[2026-11-19T23:51:50Z · bob-cli-nh.4.1.land--1] Implemented and verified the approved intention-link landing. Source audit: HEAD 8bbb3041 integrates 749efc28 (archive and digest carry), ea538f78 (reference rewrites), 992fd33d (findings and docs), plus recovered task-repair 0f990b1d7fc39dec993aa7e921a72d78121dea59 through the prior no-commit integration. The intended six source and test files remain modified; no version, changelog, docs, or parent plan changes. Closeout fixes removed two cmp_owned findings in split assertions, corrected the borrowed Path comparison after an intermediate PathBuf-to-string type error, and removed six needless YAML lookup borrows. Drift review confirms the edits stay within task move/split and intention/reference rewrite coverage.

Focused suites passed: intentions 21; periods note 8 and draft 1; archive 191; move 84; merge 59; split 5; reference rename 42; overwrite 82. The temporary archive fixture planned and applied three owned-link repairs, verified exact postimages and drafted weekly state, found no dangling_period_link or intentions_shape, and confirmed findings left Markdown bytes unchanged. Final just check ToolRun c8bdb3af80ca97a7d2d15e333be09751 exited 101 after formatting and Clippy passed: library 7466 passed, six failed, four ignored; CLI 3858 passed, one failed. These are exactly the clean-base failures recorded earlier: library capture_complete drawers bullet_starts_that_cannot_name_a_drawer_are_empty_successes, capture_complete output close_bullet_lines_suppress_wikilink_block_but_keep_note, capture_complete output close_items_and_suffixes_request_no_completion, catalog public_leaves_are_entries_or_excluded, completion every_value_arg_has_a_decision, and periods update planning_applies_ordered_intention_ops_and_reports_bad_indexes; CLI capture complete_drawers bullet_starts_that_cannot_name_a_drawer_are_empty_successes. The initial gate surfaced landing-owned Clippy errors; all were fixed before this final run.

just docs-check still fails only on unchanged Mac Capture word budgets: capture-previews 6171 and keyboard 6027 against 6000. Follow-up dispositions remain on existing work: four capture expectations on nj.6 ddf28f64; catalog, completion, and periods update on nh.2 a0b91a8d; docs budget on existing jz; the +75 capture-previews growth on nj.7 ddeab6c8. No duplicate tasks were created. epic-symbols is empty for bob-cli-nh.4.1 and bob-cli-nh.4; just has no symvision recipe. Only the approved plan status was changed to done. The parent period_intentions.md, containing epic bob-cli-nh, memory, deployment, and live vault were untouched.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.1.land.md) | [bob-cli-nh.4.1](bob-cli-nh.4.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8bbb304`](https://github.com/bobs-org/bob-cli/commit/8bbb3041cd33412e67f297c0e481534e927b0b3f) | feat(intentions): recover task rewrite integration | [bob-cli-nh.4.1](bob-cli-nh.4.1.md) | 2026-11-19 17:38:16 EST |
| bob-cli | [`f811397`](https://github.com/bobs-org/bob-cli/commit/f811397d5a98c56490adc68bd3e6b88d4be4b547) | fix(intentions): preserve links through vault rewrites | [bob-cli-nh.4.1](bob-cli-nh.4.1.md) | 2026-11-19 18:54:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.4.1.2][1] | Need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-nh.4.1.land][2] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.4.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.1.land.md

<!-- sase:referenced-by:end -->
