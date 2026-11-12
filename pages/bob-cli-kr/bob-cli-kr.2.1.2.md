# Bead: bob-cli-kr.2.1.2 — Preserve schema spans and compose a reversible index edit

[Bead Pages](../README.md) / [bob-cli-kr.2.1](bob-cli-kr.2.1.md) / bob-cli-kr.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-kr.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-kr.2.md) · **Assignee:** `bob-cli-kr.2.1.2` · **Size:** medium
**Created:** 2026-11-12 07:56:42 EST · **Closed:** 2026-11-12 10:25:25 EST
**Plan:** [202611/album\_schema\_writer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_schema_writer.md)

## Description

schema-spans: implement conservative nested YAML span edits, exact inverse restoration metadata, and the read-only album update planner combining schema and records-index changes with guarded dependencies.

## Notes

[2026-11-12T15:24:46Z · bob-cli-kr.2.1.2] HANDOFF: schema-command consumes the test-only src/native/albums/update modules. Wire shape: parse_envelope accepts schema_version/expect/ordered ops; inverse op metadata is restore: {spans: [{key_path, expected, prior}]} with schema paths under record and exact entry bytes or null (see update/mod.rs examples). Interfaces: ops::apply_ops(&[Op], &ApplyInputs) -> OpOutcome; spans::apply_schema_ops(markdown, ops, aligned restorations, outcome, inputs) -> SchemaSpanEdit; plan::plan_update(vault, config_path, snapshot, registry, requested_stem, envelope, today) -> UpdatePlan. The plan returns one optional combined FileEdit plus read dependencies; semantic no-op returns edit=None and original album bytes without index repair. Run 28 album update unit tests with cargo test --lib native::albums::update.

[2026-11-12T15:25:25Z · bob-cli-kr.2.1.2] Implemented reversible schema span edits and the snapshot-bound planner, including index composition, read dependencies, and no-op behavior. Verified: cargo test --lib native::albums::update (28 passed), cargo fmt --all -- --check, and git diff --check. Non-strict cargo clippy --lib --tests passes; strict -D warnings remains blocked by existing workspace lints.

## Dependencies

- **Depends on:** [bob-cli-kr.2.1.1](bob-cli-kr.2.1.1.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kr.2.1.3](bob-cli-kr.2.1.3.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-kr.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-kr.2.1.2/README.md) | [bob-cli-kr.2.1.2](bob-cli-kr.2.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kr.2.1.2][1] | Verify this phase's implementation, validation, and handoff note before closing it | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-kr.2.1.2/README.md

<!-- sase:referenced-by:end -->
