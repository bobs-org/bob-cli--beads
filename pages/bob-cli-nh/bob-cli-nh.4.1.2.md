# Bead: bob-cli-nh.4.1.2 — Task move, merge, and split link parity

[Bead Pages](../README.md) / [bob-cli-nh.4.1](bob-cli-nh.4.1.md) / bob-cli-nh.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.md) · **Assignee:** `bob-cli-nh.4.1.2` · **Size:** medium
**Created:** 2026-11-19 13:01:12 EST · **Closed:** 2026-11-19 17:25:03 EST
**Plan:** [202611/intention\_link\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/intention_link_repair.md)

## Description

task_repair: cover task move source/destination/bystander notes, preserve merge's retained source identities, and repair cross-note split anchors using the shared adapter and existing body resolvers. Verify previews, postimages, counts, cursor positions, and drafted versus edited/reflected provenance.

## Notes

[2026-11-19T22:22:06Z · bob-cli-nh.4.1.2] PROPOSED FOLLOW-UP: 7 pre-existing test failures reproduce identically on the clean HEAD tree (749efc28) and at ddf28f64, so they pre-date owned_repair and task_repair: capture_complete drawers/output (3 lib + 1 cli: bullet_starts_that_cannot_name_a_drawer_are_empty_successes, close_bullet_lines_suppress_wikilink_block_but_keep_note, close_items_and_suffixes_request_no_completion), catalog public_leaves_are_entries_or_excluded, completion kinds every_value_arg_has_a_decision, periods update planning_applies_ordered_intention_ops_and_reports_bad_indexes. No tracking bead found. Likely fallout from the capture-completion commits between e7aa392d (where sampled tests pass) and ddf28f64. Land agent to triage.

[2026-11-19T22:25:03Z · bob-cli-nh.4.1.2] task_repair done: shared rewrite_owned_moved_links adapter in intentions/repair.rs; move wires it plus draft-digest carry into the destination-before-insert pass (landings located after YAML expansion) and source/bystander postimages with counts in repaired_files; merge audited as copy-and-retire with empty moved targets (only the move planner relocates) plus digest carry at finalization; split derives cross-note relocation identities (retained descendants, minted/same-note excluded), repairs payload fragments, and runs vault-wide body plus owned plus carry before task/cursor reporting, surfacing repaired_files in JSON and human preview. Tests: move 86, merge 58, split 3 (incl. 31 byte-identical vectors) green; fmt clean; zero new clippy warnings; full workspace shows only 7 pre-existing failures recorded as PROPOSED FOLLOW-UP. Capture/gmail move entries share plan_task_move; split stays in its single transaction.

## Dependencies

- **Depends on:** [bob-cli-nh.4.1.1](bob-cli-nh.4.1.1.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.4.1.2/README.md) | [bob-cli-nh.4.1.2](bob-cli-nh.4.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.4.1.2][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-nh.4.1.land][2] | Need the child scope and notes | 1 |
| read-by | [agent:bob-cli-nh.4.1.land--1][2] | Compare integrated check results against the clean-base failures already recorded on this phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.4.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.1.land.md

<!-- sase:referenced-by:end -->
