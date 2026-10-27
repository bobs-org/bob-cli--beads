# Bead: bob-cli-an.6.6.6.5.6.5.5 — Backlog batch 8: listen manifest state, red macOS XCTests, and two recurring test flakes

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5](bob-cli-an.6.6.6.5.6.5.md) / bob-cli-an.6.6.6.5.6.5.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.land`
**Created:** 2026-10-25 07:49:26 EDT · **Closed:** 2026-10-25 08:34:58 EDT
**Plan:** [202610/backlog\_batch8\_listen\_manifest\_mac\_ci\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch8_listen_manifest_mac_ci_flakes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch8_listen_manifest_mac_ci_flakes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch8_listen_manifest_mac_ci_flakes.md

<!-- sase:links:end -->

## Description

Close five existing task beads by marking retried listen episodes published in their source library, making the two deterministic macOS XCTest failures pass, and removing the stage-ranker timing flake and the lib-test ETXTBSY stub race. Continue the bounded backlog campaign until all project task beads are resolved.

## Notes

[2026-10-25T12:34:58Z · bob-cli-an.6.6.6.5.6.5.5.land] Batch-8 landing verified by bob-cli-an.6.6.6.5.6.5.5.land.
STEP 1 VERIFY: read all 5 phases and every note. Each target was rechecked independently against its own acceptance, with source and commits read:
- .1/bq: sase-listen ba0613d. flush_pending marks the source manifest after a successful push, before dropping the outbox. Failed push and mark failure stay queued with published:false. tests/test_feedhost.py 31/31 rerun. bq closed.
- .2/bv: bob-mac-capture 2b20d89, a fixture-only fix (a busy hold is banner-only by documented contract; a refreshed savedFirst note supplies the clause). Assertion unchanged. macOS CI PASS on 2b20d89 (40191681188) and landed 8fda38d (40191868649). bv closed.
- .3/bw: bob-mac-capture 8fda38d. A route-only confirm omits --require-pull-in-choice. The exact argv assertion is unchanged and matches bob's capture contract. macOS CI PASS on 8fda38d. Recorded tradeoff: pull-in offers that first appear while the route card is open are reported, not refused (never auto-linked). bw closed.
- .4/3w: bob-plugins ab71502, 3 warm-ups then best-of-7 against the same 16 ms budget. Lander ran full npm test twice under load (avg 13-15): 3648/3648 both times. 3w closed.
- .5/5l: bob-cli f4f6a9ca, shared #[cfg(test)] write_executable_stub (scratch+cp, fork-stress test) used by all 8 lib stub writers. grep finds no remaining test exec writers. cargo test --lib --test-threads=64 x3: 3412/0 each. just check exit 0 (5644 passed, 0 failed; warnings are existing clippy lints). 5l closed.
Mac CI 40191868649 on landed 8fda38d: 3087 tests, 1 failure. It is testHiddenLibraryRefreshDoesNotHydrateInspector (RefsPanelModelTests:2414), intermittent before this epic (failed a49a08b, passed 556bb67/569cb36/2b20d89) and not touched by the epic.
STEP 2 INTEGRATE: since epic start (07:49) the only commits in bob-cli, bob-mac-capture, bob-plugins, and sase-listen are the epic's own five. Nothing to integrate; no duplicate stub writer remains (tests/cli/support.rs is a separate crate).
FOLLOW-UPS: phases recorded no PROPOSED FOLLOW-UP entries. Lander discoveries were routed through /sase_new_task (no duplicates, no causal active epic): created bob-cli-c0 (flake, large: the Mac hidden-library refresh test above) and bob-cli-c1 (bug, small: explicit sase-listen publish never marks the source manifest; sibling of bq). Not filed: the bw guard tradeoff, an accepted contract-compatible design choice recorded on bw.
epic-symbols: none. No Justfile symvision recipe in bob-cli.
Limitation: Athena's three stale listen manifests need the manual one-shot repair in phase .1 note #1 (no reconcile command; plan forbids live edits).

[2026-10-25T12:37:31Z · bob-cli-an.6.6.6.5.6.5.5.land] POST-CLOSE TRIAGE ADDENDUM (lander): base-branch CI review found bob-cli macOS CI run 40190123972 on a75c55f9 (pre-epic) failing ref_library::migrate_tasks::unmapped_refuses_write_and_map_wins with a NotFound in worktree_snapshot. It passed on epic SHA f4f6a9ca (run 40191854741). Not caused by this epic. Routed via /sase_new_task: no duplicate and no causal active epic, so created bob-cli-c2 (flake, small). Final follow-up outcomes: c0, c1, c2 created; no phase proposals existed; bw guard tradeoff not filed (accepted design, recorded on bw).

[2026-10-25T12:43:04Z · bob-cli-an.6.6.6.5.6.5.5.land] CONTINUATION (lander): fresh enumeration after landing shows 129 unresolved tasks (125 ready, 4 snoozed: 3o, 6q, aa, ah). Proposing successor epic 'Backlog batch 9' (scratch sase_plan_backlog_batch9_epipe_listen_publish_refresh_flakes.md, parent_bead bob-cli-an.6.6.6.5.6.5.5). It owns bob-cli-bl (EPIPE quiet exit; decision epipe_status, default exit 0, no SIGPIPE disposition change), bob-cli-c1 (explicit listen publish marks manifest), bob-cli-c0 (Mac hidden-refresh flake), bob-cli-bo (capture-related perf gate), and bob-cli-c2 (ref_library .git snapshot race). 8q was excluded because active epic bob-cli-3j owns the PTY drivers. The plan validated clean, and the continuation contract is copied verbatim with refreshed candidate guidance. Plans sidecar status:done committed before the proposal.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md) | [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@1fd04a0`](https://github.com/bobs-org/bob-cli--plans/commit/1fd04a079b3b88d14acb0201086d54c715686c9e) | chore(plans): mark backlog batch 8 epic plan done | [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) | 2026-10-25 08:41:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.2][1] | parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.3][2] | parent epic context | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land][3] | Landing: check plan-ancestor closure status | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.land][4] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md

<!-- sase:referenced-by:end -->
