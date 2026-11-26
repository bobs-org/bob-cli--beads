# Bead: bob-cli-q8.1 — Contract, shared vectors, and the Rust tie helpers

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6f.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6f.linker.w0.md) · **Assignee:** `bob-cli-q8.1` · **Size:** medium
**Created:** 2026-11-25 18:16:42 EST · **Closed:** 2026-11-25 19:49:47 EST
**Plan:** [202611/plain\_link\_dependency\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/plain_link_dependency_ties.md)

## Description

tie-contract: write the plain-link/dependency contract and PT vectors in bob-cli docs, add the shared vector fixture, and add the pure Rust helpers that classify a pair's tie and drop plain entries byte-exactly.

## Notes

[2026-11-26T00:49:28Z · bob-cli-q8.1] PROPOSED FOLLOW-UP: lib failures three_component_marker_keeps_route_and_task_contexts and task_drawers_and_project_h2_drawers_resolve_for_merge reproduce identically on clean master (already tracked in bob-cli-q7.2 notes); docs-check lint budget overruns reproduce on clean master (already tracked in bob-cli-q4.9.1.3 notes)

[2026-11-26T00:49:47Z · bob-cli-q8.1] tie-contract done: docs/task-relations.md §22 plus §1/§2/§7/§12/§13/M7 edits, docs/task-dependencies.md §5 paragraph, tests/fixtures/plain_link_ties/vectors.json (PT1-PT21), src/native/task_relations/ties.rs with drop_plain_link_entries + PairTies pinned by vector-driven tests. Verified: fmt clean, clippy clean, ties/task_relations/task_dependencies/task_status_hooks lib tests green, cli relations integration 38 green, docs_reference green, full lib 8201 pass with only 2 failures that reproduce identically on clean master (tracked in bob-cli-q7.2), docs-check lint 3 budget errors likewise pre-existing (tracked in bob-cli-q4.9.1.3). No behavior change; no memory edits (those belong to nav-tie-keys).

## Dependencies

- **Blocks:** [bob-cli-q8.2](bob-cli-q8.2.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q8.3](bob-cli-q8.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q8.4](bob-cli-q8.4.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q8.5](bob-cli-q8.5.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.1/README.md) | [bob-cli-q8.1](bob-cli-q8.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a1caeef`](https://github.com/bobs-org/bob-cli/commit/a1caeefabef111947a17247c0af512868ba2a08c) | feat(relations): plain-link/dependency tie contract, PT vectors, and Rust tie helpers | [bob-cli-q8.1](bob-cli-q8.1.md) | 2026-11-25 19:51:06 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q8.1][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-q8.5][2] | check contract phase done | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.5/README.md

<!-- sase:referenced-by:end -->
