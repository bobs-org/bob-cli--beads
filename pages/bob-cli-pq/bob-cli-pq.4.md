# Bead: bob-cli-pq.4 — Obsidian successor cards wear the diamond

[Bead Pages](../README.md) / [bob-cli-pq](README.md) / bob-cli-pq.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1f8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1f8.md) · **Assignee:** `bob-cli-pq.4` · **Size:** small
**Created:** 2026-11-23 03:54:18 EST · **Closed:** 2026-11-23 11:12:51 EST
**Plan:** [202611/task\_reqs\_criterion\_diamond.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_reqs_criterion_diamond.md)

## Description

obsidian-cards: Navigation Hotkeys draws the shared mark on requirement rows and the group heading, flips it with the staged verdict, and uses a diamond header icon on requirements-only cards.

## Notes

[2026-11-23T16:12:21Z · bob-cli-pq.4] PROPOSED FOLLOW-UP: Reconsider adding decisions:requirements-wear-the-criterion-diamond after the epic lands (declined memory_req_mark_record: one constant mark, state by fill, depth-only indentation, Mac draft never hides bytes, marks from bob state; rejected depth-counted runs and constant ⌗⌗; link to task-reqs-are-met-with-their-task).

[2026-11-23T16:12:28Z · bob-cli-pq.4] PROPOSED FOLLOW-UP: Re-sync plugin task_reqs fixtures to bob-cli canonical (test-task-reqs-twin-copies fails on README.md/vectors.json drift: canonical has RQ22/RL61 from drawer work, plugin copies do not; pre-existing on clean tree).

[2026-11-23T16:12:32Z · bob-cli-pq.4] PROPOSED FOLLOW-UP: Fix 3 pre-existing bob-cli tools/docs contract-test failures (test_current_registry_and_generated_nav_are_complete_and_unique, test_llmstxt_contracts_section_lists_exactly_registry_stems, test_readme_table_matches_original_contract_index_snapshot; fail identically on clean tree).

[2026-11-23T16:12:37Z · bob-cli-pq.4] PROPOSED FOLLOW-UP: Run real-Obsidian obsidian-req-close-card-e2e plus light/dark card screenshots (Met/Drop/Own-task rows) on a Mac; data-state assertions are in place but unverified here.

[2026-11-23T16:12:41Z · bob-cli-pq.4] PROPOSED FOLLOW-UP: Vault sync of bob-navigation-hotkeys still pending (bob plugins sync refused by live ws-15 bob-cli-ph.7 deploy 3141cf6; re-run bob plugins sync -p bob-navigation-hotkeys after that agent lands, no -F).

[2026-11-23T16:12:51Z · bob-cli-pq.4] obsidian-cards done: successor rows and group heading render shared span.bob-req-mark with staged-outcome data-state (pending/dropped/carried) and taskReqGlyph text; owner ink sets --bob-req-ink; requirements-only cards use the diamond icon; 42px monospace run slot removed (depth indentation, staged cues, conflict rings kept). Verified: new unit test (mark flips for Met/Drop/Carry/Pull-in, heading mark, diamond icon, Unicode fallback) + picker/verdicts/e2e-wrapper/plugin-build suites 110/110 pass; build:check, docs-inventory:check, docs lint all pass (reference page at 6000-word cap after condensing added prose); e2e data-state assertions added. Pre-existing failures recorded as follow-ups (fixture twin drift, docs contract tests); real-Obsidian screenshots and vault sync still pending (sync blocked by live ws-15 deploy).

## Dependencies

- **Depends on:** [bob-cli-pq.1](bob-cli-pq.1.md) ✓ · ⧖ 2026-11-23
- **Depends on:** [bob-cli-pq.3](bob-cli-pq.3.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pq.7](bob-cli-pq.7.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pq.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pq.4/README.md) | [bob-cli-pq.4](bob-cli-pq.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b2c3710`](https://github.com/bobs-org/bob-plugins/commit/b2c371025c637722abbdc045573b92976141573b) | feat(nav): draw the criterion diamond on successor requirement cards | [bob-cli-pq.4](bob-cli-pq.4.md) | 2026-11-23 11:13:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pq.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pq.4/README.md

<!-- sase:referenced-by:end -->
