# Bead: bob-cli-ph.6.1.3 — Preserve selected titles and prefer explicit catalog spellings

[Bead Pages](../README.md) / [bob-cli-ph.6.1](bob-cli-ph.6.1.md) / bob-cli-ph.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.md) · **Assignee:** `bob-cli-ph.6.1.3` · **Size:** medium
**Created:** 2026-11-25 08:39:53 EST · **Closed:** 2026-11-25 13:26:05 EST
**Plan:** [202611/capture\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_true_case_drawers.md)

## Description

place-titles: complete the shared create-title rule for quoted, glued, flag, and slug selectors; use explicit catalog spellings and notebook-style fallback. Route completion and refusal decisions through the same resolver and prove replacement, parse, preview, and commit agree for every menu row kind.

## Notes

[2026-11-25T18:17:01Z · bob-cli-ph.6.1.3] PROPOSED FOLLOW-UP: CLI capture_project_note tests expect pre-settle Tasks sections; 9 tests fail identically on clean HEAD after capture-settle (bob-cli-q4.6 / 08a708d3), including capture_project_note_task_links_write_the_worked_example — actual notes now have ### Next & In Progress chips and shifted line numbers. This phase does not change project-note layout.

[2026-11-25T18:17:15Z · bob-cli-ph.6.1.3] PROPOSED FOLLOW-UP: Existing docs headroom task bob-cli-ob still covers the fatal docs-check overage on unchanged docs/reference/plugins/bob-navigation-hotkeys.md (6068/6000); already recorded by bob-cli-ph.6.1.2 and bob-cli-ph.5. This phase does not edit that page.

[2026-11-25T18:19:53Z · bob-cli-ph.6.1.3] PROPOSED FOLLOW-UP: Same capture-settle fixture drift as note #1 also fails inbox_route (ir_dependency_touch_follows_its_routed_task, ir_routed_link_moves_with_repair_stamp_follow_and_open_notes), note_pull (np2_pick_all_matches_cli_json_and_human_fixtures, np_move_groups_follow_requested_sources_in_cli_fixtures, np16_inbox_choice_and_routed_pick_match_cli_fixtures), and task_theme_writes::new_named_task_reports_and_writes_the_resolved_theme_exception — all shifted by ### Next & In Progress chips; this phase does not change those writers.

[2026-11-25T18:26:05Z · bob-cli-ph.6.1.3] Unquoted slugs create notebook-style or catalog-explicit titles; quoted selectors and --drawer preserve authored case; glued #slug replacements quote when they would not parse back. Verified: 97 lib drawer/place tests, capture parse/complete/transfer/help CLI tests, docs-gen CLI goldens, cargo fmt, clippy gate. Pre-existing capture-settle fixture failures (project_note, inbox_route, note_pull, task_theme_writes) recorded as PROPOSED FOLLOW-UP citing bob-cli-q4.6. docs-check nav-hotkeys overage still tracked by bob-cli-ob. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-ph.6.1.2](bob-cli-ph.6.1.2.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.6.1.4](bob-cli-ph.6.1.4.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.3/README.md) | [bob-cli-ph.6.1.3](bob-cli-ph.6.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8a1d16a`](https://github.com/bobs-org/bob-cli/commit/8a1d16a621f7829bf94b3ccabf49c04ab9192fd5) | feat(capture): prefer catalog spellings and preserve authored drawer titles | [bob-cli-ph.6.1.3](bob-cli-ph.6.1.3.md) | 2026-11-25 13:27:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.6.1.3][1] | Need the phase scope, design file, notes, and epic DECISIONS | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.3/README.md

<!-- sase:referenced-by:end -->
