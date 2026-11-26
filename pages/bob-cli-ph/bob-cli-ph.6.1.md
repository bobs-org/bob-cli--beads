# Bead: bob-cli-ph.6.1 — True-case capture drawers and one place resolver

[Bead Pages](../README.md) / [bob-cli-ph.6](bob-cli-ph.6.md) / bob-cli-ph.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.md) · **Assignee:** `bob-cli-ph.6.1.land`
**Created:** 2026-11-25 08:39:52 EST · **Closed:** 2026-11-25 18:24:07 EST
**Plan:** [202611/capture\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_true_case_drawers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_true_case_drawers.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_true_case_drawers.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ph.6 with shared place resolution, bold container drafts, preserved titles, accurate completion and preview metadata, and verified capture grammar and documentation.

## Notes

[2026-11-25T18:49:06Z · bob-cli-q4.8.1.land] DISCOVERED ISSUE: Triaged bob-cli-q4.8.1.3 PROPOSED FOLLOW-UP note #2 during q4.8.1 landing. Independent bob_docs.markdown.count_words finds docs/reference/capture-syntax.md 5998 at 5c0f8160, 6000 at 0742684d, and 6011 at current e6eb52a1. Its only intervening edits are 22fea308 (ph.6.1.2) and 8a1d16a6 (ph.6.1.3); the settle-provider child touches neither. Please bring the page under the hard 6000-word reference budget in ph.6.1.5 acceptance without dropping grammar facts. No standalone task filed because this active epic owns the causal additions.

[2026-11-25T18:58:12Z · bob-cli-q6.1] DISCOVERED ISSUE: An independent bob-plugins npm run docs:check run during conflict repair, with the plugin checkout explicitly mounted, still reports docs/reference/capture-syntax.md at 6011/6000 words. The same failure repeated after refreshing the delegated bob-cli docs checkout from 8a1d16a to e6eb52a; this source page is outside bob-plugins and current target edits did not change it. This corroborates the existing assignment to phase ph.6.1.5, not a separate task.

[2026-11-25T23:24:07Z · bob-cli-ph.6.1.land] Landing verification (bob-cli-ph.6.1.land, base d67a5b7b).

VERIFIED: All 5 phases are closed and every child note was reviewed. The epic's commits are 45a54345 (shared place.rs with TaskDrawer/ProjectSection/NotebookSection adapters), 22fea308 (whole-bold drafts in all four container families, caps_drawer_retired/empty_drawer_bullet, GRAMMAR_REVISION 30), 8a1d16a6 (create-title rule, explicit catalog spelling via spelling_markers, quoted/--drawer verbatim), dfc7facb (RewriteRule::ExpandDrawerMarker, DrawerJson.marker, BlockLineJson.drawer) and d67a5b7b (docs). I read the source for each contract point. Scratch-vault walkthrough with the built bob: @foo+bar + `- **API Design**` + nested writes `- **API Design**`; `#notes` appends to legacy `- NOTES` without re-marking it; `- #api-design` menu row inserts `**API Design**` from the catalog's explicit spelling and commits it; childless bold refuses with empty_drawer_bullet (teaches __Title__); `- FUTURE WORK` with notes refuses with caps_drawer_retired plus a bold hint; capture-drawers prints verbatim titles. epic-symbols: none.

EPIC WORK FINISHED IN LANDING: (1) Three tests the epic broke, which children misreported as clean-base failures, are fixed. I proved they pass at 08a708d3 (pre-ph.6.1.2) and fail after: lib task_merge::task_drawers_and_project_h2_drawers_resolve_for_merge (unquoted create is now `**Requirements**`), lib capture_complete routes_tasks::three_component_marker_keeps_route_and_task_contexts, and CLI completion::capture_text::drawers_complete_after_id_hash. The last two now expect the documented ph.6.1.3 contract: a glued `#slug` completes only when it parses back to the row's title, so legacy titles complete as `#"REQUIREMENTS"` / `#"FIRST STEPS"`. (2) docs/completion.md and docs/capture.md said "#slug when it resolves back to exactly that drawer", which contradicted task-drawers.md, capture.md and the code. Both now say "parses back to the row's title".

INTEGRATION: Concurrent snooze commit cd594550 (bob-cli-q5.1.1.1) made the task commit resolver refuse structural H2 keys (Snoozed, Pomodoros, Events, Highlights, status groups). capture-parse still accepted `- #snoozed` / `- #pomodoros` / `- #"Blocked"` bullets, which breaks the epic's parse/preview/commit agreement. Added capture_drawers::is_task_drawer_unwritable_key, shared by reserved_selector_key (lexical parse) and the TaskDrawer resolver. Updated the drawer_bullet lib tests and the CLI reserved_new_task_drafts_agree_across_parse_preview_and_commit cases. Reviewed the other concurrent commits: q4.3/.5/.6/.7 settle, q4.4 drift meter, q5.1.1.2/.3 snooze, ph.7.1.4 task-drawers docs. None writes ALL-CAPS drawer headers or conflicts with place.rs; the snooze CLI's to_ascii_uppercase is type-key casing. The 22fea308/8a1d16a6 grammar-30 break landed without `!`. No release has been cut since v0.6.0, so the landing commit is marked feat(capture)! to carry the Breaking changelog entry the parent plan requires.

GATES: just check: fmt and clippy clean; lib 8182 passed / 0 failed; every other test binary green; tests/cli 4134 passed / 17 failed. Those 17 are exactly the settle-drift set (inbox_route x2, note_pull x3, project_note x3, project_note_offer x6, task_theme_writes, ref_library::today, task_status_hooks::sync), and the identical 17 fail at 08a708d3 before any ph.6.1 behavior change. The drawer output inside them is correct. just docs-check: capture-syntax.md 5998/6000 resolves epic notes #1/#2; the only errors are mounted bob-ledger-tools.md 6040/6000 and bob-navigation-hotkeys.md 6068/6000, plus a plugin-apis.md 9279/8000 warning.

FOLLOW-UP TRIAGE: ph.6.1.2 #1, ph.6.1.3 #2, ph.6.1.4 #3 (plugin pages) and ph.6.1.5 #1 (nav-hotkeys/plugin-apis) went to bob-cli-ob as a +1 with a fresh docs-check. ph.6.1.5 #1 (bob-ledger-tools) went to bob-cli-il as a +1. ph.6.1.3 #1/#3, ph.6.1.4 #2 (17 of 18) and ph.6.1.5 #2 are settle drift caused by active epic bob-cli-q4 (q4.6/q4.7). They were already recorded there by ph.7.1.land, and I added a fresh-reproduction DISCOVERED ISSUE note on bob-cli-q4. No standalone task was created. Declined as follow-ups because the epic caused them and they are fixed above: ph.6.1.4 #1 (both lib failures), ph.6.1.4 #2's drawers_complete_after_id_hash, and ph.6.1.4 #3's capture-syntax overage, which ph.6.1.5 fixed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.land/README.md) | [bob-cli-ph.6.1](bob-cli-ph.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@5d3da5e`](https://github.com/bobs-org/bob-cli--plans/commit/5d3da5e0e76637aea0e969935c58ed7da97e1192) | chore(plans): mark capture\_true\_case\_drawers done | [bob-cli-ph.6.1](bob-cli-ph.6.1.md) | 2026-11-25 18:27:16 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.6.1.1][1] | Need parent epic DECISIONS and child phase status | 2 |
| read-by | [agent:bob-cli-ph.6.1.2][2] | Need parent epic decisions that govern this phase | 3 |
| read-by | [agent:bob-cli-ph.6.1.3][3] | Need epic DECISIONS for place-titles phase | 1 |
| read-by | [agent:bob-cli-ph.6.1.land][4] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.land/README.md

<!-- sase:referenced-by:end -->
