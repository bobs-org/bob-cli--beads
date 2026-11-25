# Bead: bob-cli-q5.1.1.2 — Pure add, drop, and never-running wake planners

[Bead Pages](../README.md) / [bob-cli-q5.1.1](bob-cli-q5.1.1.md) / bob-cli-q5.1.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.md) · **Assignee:** `bob-cli-q5.1.1.2` · **Size:** medium
**Created:** 2026-11-25 10:36:15 EST · **Closed:** 2026-11-25 13:37:50 EST
**Plan:** [202611/snooze\_wake\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_wake_engine.md)

## Description

mutation-planners: implement pure add/drop/wake plans, identity-based subtree moves, row deduplication and history, and opt-in never-running placement without changing ordinary link placement. Finish snooze/wake/cleanup vectors, preserve notes and recorded time, and prove task lines never change on wake. Export reusable planners for the outer epic's capture phase.

## Notes

[2026-11-25T18:37:03Z · bob-cli-q5.1.1.2] PROPOSED FOLLOW-UP: just check CLI grouping 17 failures — capture inbox_route/note_pull/project_note/project_note_offer/task_theme_writes/ref_library::today/task_status_hooks fail identically on clean HEAD cd594550 (isolated CARGO_BUILD_BUILD_DIR); already DISCOVERED ISSUE on bob-cli-q4 from bob-cli-ph.7.1.land

[2026-11-25T18:37:07Z · bob-cli-q5.1.1.2] PROPOSED FOLLOW-UP: capture_complete drawer unit tests bullet_menu_on_a_prj_task_lists_sections_and_refuses_structural_ones and bullet_rows_refuse_with_the_exact_resolvers_reason panic with empty menus identically on clean HEAD cd594550 (isolated build-dir, --test-threads=1)

[2026-11-25T18:37:12Z · bob-cli-q5.1.1.2] PROPOSED FOLLOW-UP: wispr_summary_renders_one_or_two_pages_with_stable_words fails identically on clean HEAD (pdftotext kicker "M E E T I N G N OT E S"); already recorded on bob-cli-q5.1.1.1

[2026-11-25T18:37:16Z · bob-cli-q5.1.1.2] PROPOSED FOLLOW-UP: just docs-check lint fails on untouched files identically with this phase (bob-navigation-hotkeys.md 6068/6000 already on bob-cli-q5.1.1.1; bob-ledger-tools.md 6012/6000 also over cap; plugin-apis.md 9961/8000 advisory)

[2026-11-25T18:37:50Z · bob-cli-q5.1.1.2] Mutation planners done. src/native/snooze/plan.rs implements plan_add/plan_drop/plan_wake/plan_cleanup as pure snapshots→postimages (identity consume/dedup/history, Ready→Next via plan_task_link, notes+recorded time kept, wake never edits task lines). PlaceInput.never_running is opt-in (ordinary routing/MEET/append callers pass false). SubtreeInsert::FirstChild + insert_unnamed_placeholder cover never-running wake placement. Consecutive-row parse fix in parse.rs. docs/snooze.md and snooze/wake/cleanup vectors populated. Verified: 27 focused snooze tests pass (including snooze_wake_cleanup_vectors and consecutive_active_rows); never_running routing tests pass; just lint and cargo fmt green; sase bead epic-symbols empty. just check 3 lib + 17 cli failures and docs-check reference budgets reproduce identically on clean HEAD cd594550 (isolated CARGO_BUILD_BUILD_DIR); recorded as PROPOSED FOLLOW-UPs citing bob-cli-q4 and bob-cli-q5.1.1.1. CLI/receipts/tick left to later phases. No ancestor closed. No memory edits.

## Dependencies

- **Depends on:** [bob-cli-q5.1.1.1](bob-cli-q5.1.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.1.1.3](bob-cli-q5.1.1.3.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.1.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.2/README.md) | [bob-cli-q5.1.1.2](bob-cli-q5.1.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e6eb52a`](https://github.com/bobs-org/bob-cli/commit/e6eb52a103656add99a1a49f2f0b3d791536abc4) | feat(snooze): add pure add, drop, and never-running wake planners | [bob-cli-q5.1.1.2](bob-cli-q5.1.1.2.md) | 2026-11-25 13:38:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.7.1.land--2][1] | Match the just check library and CLI target failures to existing baseline triage | 1 |
| read-by | [agent:bob-cli-q4.9.1.1][2] | Check whether just-check CLI grouping failures are already tracked | 1 |
| read-by | [agent:bob-cli-q5.1.1.2][3] | Need DECISIONS, notes, and remaining work from earlier agents | 6 |
| read-by | [agent:bob-cli-q5.1.1.4][4] | Cite existing follow-up notes for CLI grouping failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ph.7.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.9.1.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.2/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.4/README.md

<!-- sase:referenced-by:end -->
