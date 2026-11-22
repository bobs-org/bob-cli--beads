# Bead: bob-cli-on.8.1.3 — Atomic carry and drop planning

[Bead Pages](../README.md) / [bob-cli-on.8.1](bob-cli-on.8.1.md) / bob-cli-on.8.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.md) · **Assignee:** `bob-cli-on.8.1.3` · **Size:** medium
**Created:** 2026-11-22 07:22:30 EST · **Closed:** 2026-11-22 09:34:00 EST
**Plan:** [202611/requirement\_close\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/requirement_close_engine.md)

## Description

writes: adapt carry_req and drop_req to guarded staged capture snapshots, compose line movement across disjoint branches, and return exact outcome receipts without adding another commit path.

## Notes

[2026-11-22T14:34:00Z · bob-cli-on.8.1.3] Implemented atomic carry/drop planning: src/native/task_complete/req_writes.rs (plan_req_writes reusing carry_req/ReqRef and drop_req with expected-line guard, disjoint carries bottom-to-top then drops, coordinate composition via current-forest relookup, final block-ID relocation for created tasks/moves, Met aggregation excluding folded descendants, exact receipts, no new commit path) plus src/native/capture/req_close.rs adapter (load_staged_snapshot guards, full vault only for structural verdicts, stage_snapshot_postimage, Met-only no-scan). RV20-RV28 pinned in tests/fixtures/req_close/vectors.json with README writes family. Verified: cargo test native::task_complete::tests (239 passed), native::task_split (8 passed), native::task_block_layout (14 passed), native::capture::req_close adapter test (1 passed); cargo fmt --check clean, git diff --check clean, cargo clippy workspace all-targets with canonical gates shows no errors, sase bead epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-on.8.1.2](bob-cli-on.8.1.2.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.8.1.4](bob-cli-on.8.1.4.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.3/README.md) | [bob-cli-on.8.1.3](bob-cli-on.8.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d5e31ab`](https://github.com/bobs-org/bob-cli/commit/d5e31abcbbb19c2ca3fc14947ee03e3b9a0369fe) | feat(task-complete): add atomic carry/drop req write planning | [bob-cli-on.8.1.3](bob-cli-on.8.1.3.md) | 2026-11-22 09:35:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.8.1.3][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-on.8.1.4][2] | Need prior phase handoff notes for placement phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.4/README.md

<!-- sase:referenced-by:end -->
