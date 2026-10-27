# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2 — Stop bob ref create from writing a saved source without its source\_markdown pointer

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2` · **Size:** large
**Created:** 2026-10-27 03:08:26 EDT · **Closed:** 2026-10-27 05:15:32 EDT
**Plan:** [202610/backlog\_batch16\_mac\_build\_orphan\_refs\_archive\_moves\_plugin\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch16_mac_build_orphan_refs_archive_moves_plugin_guards.md)

## Description

ref-pointer-orphans: resolve bob-cli-cy by finding the create path that wrote the muse_commentary store but no pointer, making store and pointer land together, and routing the one live orphan's repair through a gate.

## Notes

[2026-10-27T07:19:50Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2] PLANNING EVIDENCE: On bob-cli 2f004d77, both sync execution branches rebuild pipeline_metadata and drop stable_metadata.source_markdown; the omission exists in 009060f9. The isolated bobs-org/bob checkout confirms 6beb2dad7 saved the source and d679d5151 created the only note revision without its pointer; source and PDF hashes still match the catalog exactly. A named attach-source dry run using the existing saved source verified 1 reference, skipped 0, writes none. No implementation or live-vault changes were made. A validated medium tale, sase_plan_ref_source_birth_pointer.md, covers pointer transfer, an intake invariant, regressions, doctor guidance, and the epic-required human repair gate; it is being submitted through sase plan propose.

[2026-10-27T09:15:16Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2--3] BASELINE: At 2f004d77, both v1/v2 sync executors rebuilt pipeline_metadata and dropped planned stable_metadata.source_markdown; the only new reference therefore lacked the pointer despite a verified saved source. CAUSE: execution metadata retained birth_lineage in v2 but omitted the parallel planned source pointer, and create intake did not enforce that a successfully saved Markdown source remained attached to the persisted note. FIX: preserve the planned pointer through both marker-write paths; propagate the verified saved-source expectation through create intake and reject/queue if the parsed persisted pointer is missing or differs; add doctor diagnostics and regressions. VERIFICATION: focused pointer/v1/v2 tests, store_ CLI tests, queued-create test, doctor diagnostics test, just check, and just docs-check all passed on the completed rerun (monitor 7v69tmjbxvfv, exit 0). An earlier run of store_ had two transient missing-note failures; the same full chain passed on rerun. REPAIR: custom gate custom-7255eeae-f6c8-4b06-83bf-38a0f7020088 approved one attach-source for muse_commentary_missing_from_exec_stream; preview/apply confirmed source SHA-256 ed2f4a29e3e3273f654f7c138daf7a8fe63c27cd68147419319245ca2f3777f8, PDF SHA-256 6b7e7234369e8afa77ec12c7994199d8a185ae8692f35196e7ff491e91c2e203, catalog SHA-256 391ce0e3b6dcf5eb1dd93658a4397ecc10426b534208aa62bf78c701a7619e5e; attached and committed b1d897724ac9ab55bb49f6c4a3830c895ae538df. POST-REPAIR: bob ref show -f json reports the exact source_markdown pointer and attached route; bob ref code reports available, 25,042-byte source with matching SHA and two blocks (Mermaid/JSON); bob ref links reports no_links; bob ref code -f markdown emits both blocks, --source SHA matches, and bob ref marker reads the PDF marker without writes. No unrepaired orphan or repair limitation remains.

[2026-10-27T09:15:32Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2--3] Verified source-pointer implementation and all focused/full/docs checks; approved gate attached the byte-identical saved source to the exact orphan; Bob reads confirm pointer, source, code catalog, links, and Markdown access. No epic symbols remain. Closed this phase only; target task and ancestors remain open.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2--3][1] | Need the assigned phase scope, current notes, and closure state | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.2.md

<!-- sase:referenced-by:end -->
