# Bead: bob-cli-j8.3 — Capture writes notes into notebooks (the destination decides)

[Bead Pages](../README.md) / [bob-cli-j8](README.md) / bob-cli-j8.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3x.linker.w0.md) · **Assignee:** `bob-cli-j8.3` · **Size:** large
**Created:** 2026-11-09 12:11:27 EST
**Plan:** [202611/bob\_notebooks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_notebooks.md)

## Description

capture-notebook-notes: add the memoized notebook route policy and teach capture that a notebook route writes notes: `@nb`, `@nb#section` (exact, created on demand, near misses refused), `@nb^id`, `@nb#section^id` (new on every route), `@nb+id` sub-notes, lists, draft-wide `@@nb`, URLs, `--route`, teaching refusals, parse modes, previews, notebook capture-targets rows, and the grammar bump.

## Notes

[2026-11-09T18:49:17Z · bob-cli-j8.3] Planning evidence: prerequisite notebook recognition/list/check landed in 0a74731b; no prior-work notes or notebook capture policy/writer were present. Authored and validated a four-phase child epic covering shared route parsing, draft composition, guarded writes, then targets/docs/integration. The child land agent is tasked with verifying and closing this phase; no implementation changes made in this planning turn. Audited read of research:202611/bob_notebooks/bob_notebooks.md returned missing, so the binding parent plan supplies the contract. No epic-symbol entries currently belong to bob-cli-j8.3.

## Dependencies

- **Depends on:** [bob-cli-j8.1](bob-cli-j8.1.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j8.4](bob-cli-j8.4.md) ◐ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j8.9](bob-cli-j8.9.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.3.md) | [bob-cli-j8.3](bob-cli-j8.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j8.3.1.3][1] | Check parent phase scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.3.1.3/README.md

<!-- sase:referenced-by:end -->
