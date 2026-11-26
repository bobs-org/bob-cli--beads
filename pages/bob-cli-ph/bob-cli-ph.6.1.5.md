# Bead: bob-cli-ph.6.1.5 — Verify the complete capture contract and publish its documentation

[Bead Pages](../README.md) / [bob-cli-ph.6.1](bob-cli-ph.6.1.md) / bob-cli-ph.6.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.md) · **Assignee:** `bob-cli-ph.6.1.5` · **Size:** medium
**Created:** 2026-11-25 08:39:53 EST · **Closed:** 2026-11-25 16:46:07 EST
**Plan:** [202611/capture\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_true_case_drawers.md)

## Description

capture-acceptance: run the cross-context scratch-vault acceptance matrix, finish capture and JSON documentation, and run formatting, docs, and repository gates. Record evidence and unresolved baseline failures for the child epic land agent, which alone verifies and closes bob-cli-ph.6.

## Notes

[2026-11-25T21:17:17Z · bob-cli-ph.6.1.5] PROPOSED FOLLOW-UP: just docs-check still fails on unchanged mounted plugin references at this phase base: docs/reference/plugins/bob-ledger-tools.md is 6002/6000 (existing tracker bob-cli-il) and docs/reference/plugins/bob-navigation-hotkeys.md is 6068/6000 (bob-cli-ob). docs/develop/plugins/plugin-apis.md is 9279/8000, warning-only and tracked by bob-cli-ob. Capture syntax was trimmed from 6011 to 5998 and no longer fails. Reproduction: just docs-check after just docs-gen; these mounted pages are unchanged from the initially clean checkout.

[2026-11-25T21:45:42Z · bob-cli-ph.6.1.5--1] PROPOSED FOLLOW-UP: just check ToolRun c9e29a4e24c0b6769b38ccbda59ca2ac (monitor e0bw5ycq5bpy, 2026-11-25) exited 101 solely on the same clean-base capture failures documented in bob-cli-ph.6.1.3 notes #1/#3 and bob-cli-ph.6.1.4 notes #1/#2. bob-obsidian --lib: 8180 passed, 2 failed, 5 ignored; failures were native::capture_complete::tests::routes_tasks::three_component_marker_keeps_route_and_task_contexts and native::task_merge::tests::task_drawers_and_project_h2_drawers_resolve_for_merge. bob-obsidian --test cli: 4133 passed, 18 failed, 0 ignored; failures were capture::inbox_route::ir_dependency_touch_follows_its_routed_task, capture::inbox_route::ir_routed_link_moves_with_repair_stamp_follow_and_open_notes, capture::note_pull::np2_pick_all_matches_cli_json_and_human_fixtures, capture::note_pull::np_move_groups_follow_requested_sources_in_cli_fixtures, capture::note_pull::np16_inbox_choice_and_routed_pick_match_cli_fixtures, capture::project_note::capture_move_landing_repairs_moved_reports_after_child_edits, capture::project_note::capture_project_note_choice_answers_match_authored_bullets, capture::project_note::capture_project_note_task_links_write_the_worked_example, capture::project_note_offer::offer_duplicate_picks_without_later_context_keep_every_offer, capture::project_note_offer::offer_equal_descriptions_stay_distinct_from_an_authored_id_twin, capture::project_note_offer::offer_picking_several_duplicates_keeps_the_rest_and_matches_authored, capture::project_note_offer::offer_selected_pick_keeps_frozen_identity_across_line_shift, capture::project_note_offer::offer_two_equal_descriptions_survive_picking_the_first_or_last, capture::project_note_offer::offer_three_equal_descriptions_survive_picking_first_middle_or_last, capture::task_theme_writes::new_named_task_reports_and_writes_the_resolved_theme_exception, completion::capture_text::drawers_complete_after_id_hash, ref_library::today::today_matches_unnamed_capture_and_named_capture_remembers_theme, task_status_hooks::sync::task_status_hooks_groups_area_project_tasks_after_final_statuses. All other just check targets passed; this run adds no failure beyond those prior clean-base results.

[2026-11-25T21:46:07Z · bob-cli-ph.6.1.5--1] Verified: just docs-gen passed and regenerated the docs inventory. just docs-check reports capture-syntax.md at 5998/6000; its only errors remain unchanged plugin pages bob-ledger-tools.md (6002/6000, tracked by bob-cli-il) and bob-navigation-hotkeys.md (6068/6000, tracked by bob-cli-ob); plugin-apis.md is a warning only. just check exited 101 only on the 2 lib and 18 CLI clean-base capture failures recorded above, matching bob-cli-ph.6.1.3 notes #1/#3 and bob-cli-ph.6.1.4 notes #1/#2; all other targets passed. epic-symbols had no leftovers.

## Dependencies

- **Depends on:** [bob-cli-ph.6.1.4](bob-cli-ph.6.1.4.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.6.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.1.5.md) | [bob-cli-ph.6.1.5](bob-cli-ph.6.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d67a5b7`](https://github.com/bobs-org/bob-cli/commit/d67a5b7b8135af40ba8f345e90cb9a12f3fe0812) | docs(capture): complete drawer contract references | [bob-cli-ph.6.1.5](bob-cli-ph.6.1.5.md) | 2026-11-25 16:19:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.6.1.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.land/README.md

<!-- sase:referenced-by:end -->
