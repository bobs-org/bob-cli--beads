# Bead: bob-cli-n7.2 — Fix the macOS /var symlink path failures in note catalog and note goto

[Bead Pages](../README.md) / [bob-cli-n7](README.md) / bob-cli-n7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-n5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n5.land.md) · **Assignee:** `bob-cli-n7.2` · **Size:** medium
**Created:** 2026-11-18 01:55:52 EST · **Closed:** 2026-11-18 09:00:10 EST
**Plan:** [202611/backlog\_triage\_t4.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t4.md)

## Description

macos-symlink: Resolve bob-cli-n6 (note_catalog xlib tier and note_goto vault_root under the /var -> /private/var temp symlink), fixing product canonicalization where it is a real bug.

## Notes

[2026-11-18T12:48:04Z · bob-cli-n7.2] Linux verification done: fixed TierContext::for_vault and ClassifyContext::new to canonicalize library/ref paths before relativizing against the canonical vault_root (lexical bob_dir fallback when path missing). note_goto vault_root test now compares canonical forms. New regression native::note_catalog::tests::symlinked_vault_root_keeps_library_tiers_hidden passes via symlink alias on Linux. Focused: 3 note_catalog lib tests ok, capture_complete_note_goto_reports_shape_without_query ok. just check exit 0. Starting macos-ci-check monitor for the 3 macOS nodes.

[2026-11-18T12:53:04Z · bob-cli-n7.2] Follow-up check: macos-ci-check monitor 2zdrzg still staged with no output at inspection (pid null, not launched); no GitHub run covers this dirty tree, so no macOS evidence yet. Focused tests re-verified green on current tree (3 note_catalog lib tests, note_goto shape test) and just check exit 0 from this tree stands. Leaving bead open per phase close criterion (3 nodes must pass on macos-latest); submitting intermediate declaration with keep.

[2026-11-18T14:00:01Z · bob-cli-n7.2--1] PROPOSED FOLLOW-UP: macos-latest test job hits 45m timeout on post-fix tree, blocking full macOS verification — snapshot run 44308634344 (f4878bcb) and clean master run 44308576558 (1f6cc7be, same SHA) both cancelled at 45m during bob-obsidian compile (Run tests step, no test output); pre-fix run 44273496460 (509d8572) completed in 42m and showed the exact 3 product failures this bead fixes. Timeout reproduces identically on clean base, systemic per bob-cli-mj note (every run since before epic). Follow-up: land agent to confirm with fresh macos-ci-check or green master test job per plan Verification and closeout; consider warm-cache retry or timeout bump. -r macos-ci timeout blocks full verification but reproduces on clean base

[2026-11-18T14:00:10Z · bob-cli-n7.2--1] Linux verified on 1f6cc7be: note_catalog lib 8 passed (golden_listed_set_and_canonical_order, shared_path_tiers_agree_with_the_living_walk, symlinked_vault_root_keeps_library_tiers_hidden new regression) + capture_complete_note_goto_reports_shape_without_query ok + just check exit 0. macOS: pre-fix run 44273496460 (509d8572) shows the exact 3 failures (xlib/q.md extra, Living vs Hidden, /private/var vs /var); post-fix snapshot 44308634344 and clean master 44308576558 (same SHA 1f6cc7be) both cancelled at 45m timeout during bob-obsidian compile (no test verdict, infra, reproduces identically on clean base per mj systemic note). Fix canonicalizes library/ref paths before relativizing (tiers.rs, mod.rs) + canonical vault_root assertion (note_goto.rs) + Linux symlink-alias regression reproduces /var condition. epic-symbols clean. Timeout recorded as PROPOSED FOLLOW-UP for lander fresh macos-ci-check.

## Dependencies

- **Depends on:** [bob-cli-n7.1](bob-cli-n7.1.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-n7.3](bob-cli-n7.3.md) ✓ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n7.2.md) | [bob-cli-n7.2](bob-cli-n7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1f6cc7b`](https://github.com/bobs-org/bob-cli/commit/1f6cc7bedbeb6786202d9e003dad3b1cbccd4911) | fix(note-catalog): canonicalize library roots for symlinked vaults | [bob-cli-n7.2](bob-cli-n7.2.md) | 2026-11-18 07:55:27 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-n7.land--a][1] | Read all T4 phase notes and dispositions before closing the parent epic | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n7.land.md

<!-- sase:referenced-by:end -->
