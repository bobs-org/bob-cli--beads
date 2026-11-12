# Bead: bob-cli-kj.3 — Stats RefCell double-borrow panic

[Bead Pages](../README.md) / [bob-cli-kj](README.md) / bob-cli-kj.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.3` · **Size:** small
**Created:** 2026-11-11 17:20:03 EST · **Closed:** 2026-11-11 18:19:19 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

## Description

stats-borrow: restructure HomesEngine::finish so remember/ensure_root never re-borrow the resolver, add a regression test for single-metric ranges covering today, and record bob-cli-hp close evidence from just check (beads bob-cli-jr, bob-cli-hp).

## Notes

[2026-11-11T22:42:08Z · bob-cli-kj.3] HomesEngine::finish collects global-inspect homes and extra areas, then remember() after the resolver borrow drops so ensure_root never re-borrows. Regression native::stats::homes::tests::single_metric_worked_today_resolves_unseen_inspect_roots panicked at homes.rs:412 "RefCell already borrowed" before the fix and passed after on Explicit(["worked"]) range 2026-10-18..2026-10-18 (today). bob-cli-hp close evidence: cargo test -p bob-obsidian --lib --exact native::completion::kinds::tests::every_table_entry_matches_the_tree and native::catalog::tests::public_leaves_are_entries_or_excluded both passed.

[2026-11-11T23:18:47Z · bob-cli-kj.3--1] PROPOSED FOLLOW-UP: subprocess_runner detached-grandchild drain tests flake under full just check — native::subprocess_runner::tests::run_bounds_pipe_drain_when_detached_grandchild_holds_output and raw_run_bounds_pipe_drain_when_detached_grandchild_holds_output failed (stderr missing "output truncated" / output_incomplete false) in just check on -p bob-obsidian --lib (6645 passed, 2 failed, exit 101). Same two tests passed on clean HEAD in isolation in 2.01s. bob-cli-kf.land already recorded this as a transient drain flake that passed on rerun; no dedicated task bead.

[2026-11-11T23:19:19Z · bob-cli-kj.3--1] HomesEngine::finish collects global-inspect homes and extra areas, then remember() after the resolver borrow drops so ensure_root never re-borrows. Regression native::stats::homes::tests::single_metric_worked_today_resolves_unseen_inspect_roots passed (Explicit(["worked"]) range 2026-10-18..2026-10-18). bob-cli-hp close evidence: native::completion::kinds::tests::every_table_entry_matches_the_tree and native::catalog::tests::public_leaves_are_entries_or_excluded passed. just check later failed two subprocess_runner drain tests that pass on clean HEAD in isolation; recorded as PROPOSED FOLLOW-UP. No --epic-symbol leftovers. Task beads bob-cli-jr and bob-cli-hp stay open for the land agent.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.3.md) | [bob-cli-kj.3](bob-cli-kj.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3ba40fc`](https://github.com/bobs-org/bob-cli/commit/3ba40fc5444e0b593f5805d9af6742bfd989b953) | fix(stats): drop HomesEngine resolver borrow before remember | [bob-cli-kj.3](bob-cli-kj.3.md) | 2026-11-11 18:42:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kj.3--2][1] | Need phase status, notes, and whether close already landed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.3.md

<!-- sase:referenced-by:end -->
