# Bead: bob-cli-n7.1 — Make case-sensitive collision tests portable to macOS

[Bead Pages](../README.md) / [bob-cli-n7](README.md) / bob-cli-n7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-n5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n5.land.md) · **Assignee:** `bob-cli-n7.1` · **Size:** medium
**Created:** 2026-11-18 01:55:52 EST · **Closed:** 2026-11-18 07:25:33 EST
**Plan:** [202611/backlog\_triage\_t4.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t4.md)

## Description

macos-case: Resolve bob-cli-l9 (album, record, and highlights-scan collision tests that assume a case-sensitive filesystem) without weakening any collision protection.

## Notes

[2026-11-18T12:25:16Z · bob-cli-n7.1] PROPOSED FOLLOW-UP: Remaining macOS failures are already tracked by bob-cli-n6 (phase bob-cli-n7.2) and bob-cli-kl (phase bob-cli-n7.3) — fixed-tree CI 44273496460 at 509d8572b50c753743ee5082d566e7c9adf342e5 fails only note_catalog::golden_listed_set_and_canonical_order (extra xlib/q.md), shared_path_tiers_agree_with_the_living_walk (Living vs Hidden), capture::note_goto::capture_complete_note_goto_reports_shape_without_query (/private/var vs /var), subprocess_runner::run_bounds_pipe_drain_when_detached_grandchild_holds_output (output truncated absent), and raw_run_bounds_pipe_drain_when_detached_grandchild_holds_output (output_incomplete false). Compared macOS job 134695683540 with clean pre-fix master job 134543984421 in run 44227364061 at 2f14eef5: the same five assertions fail identically, apart from temporary path/process identifiers. No new task needed; retain these for the already-scoped later phases. https://github.com/bobs-org/bob-cli/actions/runs/44273496460 https://github.com/bobs-org/bob-cli/actions/runs/44227364061

[2026-11-18T12:25:21Z · bob-cli-n7.1] Verified the earlier implementation already landed as 509d8572b50c753743ee5082d566e7c9adf342e5; its tree c1fa2d57ebf2275ffe7b4f0e1e85c282ff439e11 exactly matches the original macos-ci-check snapshot 1bc994300ded501a629e1196e31c483f8f96d42c. All six changed files remain unchanged at current HEAD ce6425f5. Recovered prior focused Linux success and checked ToolRun 812661dbec94f1b6f1732f85407df85c: just check succeeded, exit 0, 370 seconds, complete evidence. Completed master CI run 44273496460 verifies the exact landed tree: lint, ubuntu tests, and package pass; macOS job 134695683540 explicitly reports ok for all seven required nodes (albums create stale_plan_notices_a_collision_introduced_after_planning; album registry stem_noun_and_case_insensitive_folder_collisions_invalidate_all_claims; albums_create create_normalizes_mixed_case_stems_and_takes_path_qualified_parents; capture record record_exists_fix_uses_a_staged_target_but_not_an_incomplete_or_unsafe_one; scan_interleave queued_existing_output_collision_rejects_without_overwrite, queued_queued_output_collision_rejects_without_publication, and post_recovery_replan_failure_keeps_direct_output). Ubuntu job 134695683695 also reports all seven ok. Earlier precommit CI attempts were canceled during compilation; this completed exact-tree master run supplies their missing evidence. Reviewed portable snapshot collision, stored filename assertions, volume capability probe, no-overwrite byte/receipt assertions, and portable queued/existing recovery fixture. No product changes or new edits needed. Source task bob-cli-l9 has completion evidence here for the lander; this worker closes only the assigned phase, per the current prompt.

[2026-11-18T12:25:33Z · bob-cli-n7.1] Completed and verified existing commit 509d8572. All seven collision regression nodes pass on Linux and macOS in exact-tree CI 44273496460; prior just check ToolRun 812661dbec94f1b6f1732f85407df85c passed. The five unrelated macOS failures match unchanged pre-fix baseline code and assertions and are recorded as PROPOSED FOLLOW-UP evidence for existing bob-cli-n6 and bob-cli-kl. No epic-symbol entries remain. Closed only bob-cli-n7.1; source task and parent remain for their authorized lander.

## Dependencies

- **Blocks:** [bob-cli-n7.2](bob-cli-n7.2.md) ◐ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n7.1.md) | [bob-cli-n7.1](bob-cli-n7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`509d857`](https://github.com/bobs-org/bob-cli/commit/509d8572b50c753743ee5082d566e7c9adf342e5) | test(collision): normalize filesystem-sensitive cases for macOS | [bob-cli-n7.1](bob-cli-n7.1.md) | 2026-11-18 04:10:47 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-n7.1--3][1] | Need phase status and prior evidence before deciding whether this phase may close | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n7.1.md

<!-- sase:referenced-by:end -->
