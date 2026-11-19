# Bead: bob-cli-nh.4.1 — Preserve intention links through vault rewrites

[Bead Pages](../README.md) / [bob-cli-nh.4](bob-cli-nh.4.md) / bob-cli-nh.4.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.md) · **Assignee:** `bob-cli-nh.4.1.land`
**Created:** 2026-11-19 13:01:12 EST
**Plan:** [202611/intention\_link\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/intention_link_repair.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/intention_link_repair.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/intention_link_repair.md

<!-- sase:links:end -->

## Description

Links inside daily and period intentions, summaries, and reflections survive archive, task, and reference rewrites with valid YAML and correct provenance; the shared periods problems report identifies malformed or stale period text.

## Notes

[2026-11-19T22:35:13Z · bob-cli-nh.4.1.land] LAND AUDIT / FOLLOW-UP TRIAGE (before remaining-work tale): Read this epic (no own DECISIONS or prior notes), all four child scopes and all six prior child notes, plan:202611/intention_link_repair.md and enclosing period_intentions.md, plus parent phase nh.4 and its final decisions. day_summary_cap=sixty remains intact; no memory edits, deployments, or live vault edits. Reviewed 749efc28 (typed repair/archive/digest carry), ea538f78 (reference rename/overwrite), 992fd33d (report-only findings/docs), and recovered task_repair 0f990b1d7fc39dec993aa7e921a72d78121dea59 from this checkout reflog: it was committed detached at 17:26, then checkout switched to master 992fd33d, leaving it absent from master/origin/master. Applied that commit with cherry-pick --no-commit, cleanly merging reference phase changes; finalizer will preserve this integration. cargo fmt --all -- --check and git diff --cached --check pass; integrated just check/docs-check and fixture acceptance are still pending, not claimed green. Caller inventory: archive moved-block/rename adapter; move pure planner shared by direct/capture/Gmail; merge copy-and-retire retains source anchors and bare-note relocation uses move; split vault postimages; ref rename plus overwrite identity/highlight/frozen paths; generic vault_rewrite callers themes rename/split/migrate, relation rename/reverse, periods ensure/migrate. Examined intervening 5b547f13/c94a718d bank imports (no target retargeting), a29a64f6 summary drafting (integration gap below), and earlier-since-creation logs/update/glossary work. Remaining source-confirmed gaps: reference canonical_frontmatter_end returns None for unclosed YAML so raw pass rewrites protected properties; repair_owned_postimages skips digest carry when only body links changed; split gates fragment repair on nonempty moved_targets and feeds individual lines, losing stayed-anchor qualification for minted selections and multiline fence/comment context; newer apply_with_review duplicates the old trim()-based delimiter rescan unlike corrected apply/split_document and can mistake an indented --- in a reflection scalar for the YAML close. A single medium tale will add regressions, fix these bounded paths, perform integrated acceptance, and close nh.4.1 then phase nh.4 in that coding turn. No epic symbols for nh.4.1 or nh.4; no symvision recipe presently. FOLLOW-UP OUTCOMES: .2 #1, .3 #1, .4 #2 are one repeated seven-test proposal, separated by causal owner: four capture expectations attached as DISCOVERED ISSUE to active nj (nj.6 ddf28f64); catalog/completion registration and wrong ordered-op assertion attached to active nh (nh.2 a0b91a8d). Source/history corroborated the agents' clean-base reproductions; no new task because active epics own these causes. .4 #1 docs overages corroborated existing ready bob-cli-jz (+1): independently counted Mac b6b7f6cf capture-previews 6171, keyboard 6027 vs 6000. Also attached +75 capture-previews growth from nj.7 ddeab6c8 (6096->6171) to active nj. No proposal discarded; duplicate new tasks declined because of these existing causal owners/duplicate. Task search across all statuses, last-week sweep, and active-epic review completed through sase_new_task.

[2026-11-19T22:37:10Z · bob-cli-nh.4.1.land] Remaining-work tale sase_plan_intention_link_landing.md validated with zero warnings after the required explain/edit/revalidate loop. It contains four bounded source fixes, integrated just check/docs-check and archive-to-problems acceptance, then normal closeout of this epic, its plan status, and parent phase bob-cli-nh.4 in the coding turn before finalization. Audit wording correction: reviewed all EIGHT child notes (1+2+2+3), not six. No current integrated Rust/doc gate pass is claimed; only formatting and diff checks passed. All proposed follow-ups were triaged and recorded in the preceding note before proposal.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.4.1.land/README.md) | [bob-cli-nh.4.1](bob-cli-nh.4.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8bbb304`](https://github.com/bobs-org/bob-cli/commit/8bbb3041cd33412e67f297c0e481534e927b0b3f) | feat(intentions): recover task rewrite integration | [bob-cli-nh.4.1](bob-cli-nh.4.1.md) | 2026-11-19 17:38:16 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.4.1.2][1] | Need parent epic scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.4.1.2/README.md

<!-- sase:referenced-by:end -->
