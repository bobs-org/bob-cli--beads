# Bead: bob-cli-mr.2 — Never promote closed or archived prerequisites

[Bead Pages](../README.md) / [bob-cli-mr](README.md) / bob-cli-mr.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1dh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1dh.md) · **Assignee:** `bob-cli-mr.2` · **Size:** medium
**Created:** 2026-11-17 11:16:43 EST · **Closed:** 2026-11-17 11:44:47 EST
**Plan:** [202611/backlog\_triage\_t1\_red\_gates\_closed\_prereqs\_scan\_lock.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t1_red_gates_closed_prereqs_scan_lock.md)

## Description

closed-prereqs: filter capture promotion seeds by graph.open, guard the rewrite loop, add closed/done/cancelled prerequisite tests, and close bob-cli-jh.

## Notes

[2026-11-17T16:44:47Z · bob-cli-mr.2] Filtered capture promotion seeds by graph.open on both non-^prj paths and guarded plan_promotions against closed/cancelled/archive rewrites. Closed bob-cli-jh. Verified capture_does_not_promote_closed_done_or_cancelled_prerequisites (Next and In Progress x live [x], done/ archive, cancelled [-]), capture_new_task_does_not_promote_a_closed_prerequisite, capture_promotion_walks_through_prj_without_raising_it, promotion_walks_through_a_blocked_seed_without_raising_it. Dry-run and live temp vault: archived [x] stayed byte-identical; Depends-On still written. docs/task-dependencies.md already states open-only promotion and "Closed lines are never edited". bob-plugins JS already filters addedOpen — no plugin change. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-mr.1](bob-cli-mr.1.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-mr.3](bob-cli-mr.3.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mr.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.2.md) | [bob-cli-mr.2](bob-cli-mr.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b0bddbb`](https://github.com/bobs-org/bob-cli/commit/b0bddbb98247331181bd0c9f6aa3ed07e6f6541e) | fix(capture): never promote closed or archived prerequisites | [bob-cli-mr.2](bob-cli-mr.2.md) | 2026-11-17 12:04:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mr.2--1][1] | Need current bead status and remaining work after host completion failed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.2.md

<!-- sase:referenced-by:end -->
