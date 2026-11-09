# Bead: bob-cli-ir.5.1.2 — Resolve record metadata and expose discovery rows

[Bead Pages](../README.md) / [bob-cli-ir.5.1](bob-cli-ir.5.1.md) / bob-cli-ir.5.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.5.md) · **Assignee:** `bob-cli-ir.5.1.2` · **Size:** medium
**Created:** 2026-11-08 18:25:56 EST · **Closed:** 2026-11-08 20:51:18 EST
**Plan:** [202611/capture\_record\_creation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_record_creation.md)

## Description

record-parse: adapt the existing records planner for capture-parse, implement record diagnostics and the collection-route fix, and add capture-targets record rows without polluting task-only consumers.

## Notes

[2026-11-09T01:51:09Z · bob-cli-ir.5.1.2] Record parse contract for the next phase: claimed items expose additive top-level/per-item `record` metadata; `type` is the configured ID and `path` is vault-relative. A single typed source uses `range`; repeated values use `range: null` plus individual `value_ranges[]`, keeping intervening note spans separate. Missing titles retain the schema and need `record_title`; missing required values need `record_value`. Configured record targets append after note routes, while task-only scans filter them out.

[2026-11-09T01:51:18Z · bob-cli-ir.5.1.2] Implemented record planner-backed capture-parse metadata and diagnostics, record-folder discovery/completion, and task-only scanner exclusions. Verified 156 record-filtered Rust tests passed (1 ignored), cargo check, cargo fmt --check, docs-gen, full docs-check, git diff --check, and no outstanding epic symbols.

## Dependencies

- **Depends on:** [bob-cli-ir.5.1.1](bob-cli-ir.5.1.1.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.5.1.3](bob-cli-ir.5.1.3.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.5.1.2/README.md) | [bob-cli-ir.5.1.2](bob-cli-ir.5.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4c97ed4`](https://github.com/bobs-org/bob-cli/commit/4c97ed416f3cc8fa066353a34d52d7757b845009) | feat(capture): resolve record metadata and expose targets | [bob-cli-ir.5.1.2](bob-cli-ir.5.1.2.md) | 2026-11-08 20:52:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.5.1.2][1] | Need the phase scope, design file, and prior notes before continuing assigned work | 2 |
| read-by | [agent:bob-cli-ir.5.1.3][2] | Need resolver/adapter contract recorded by record-parse | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.5.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.5.1.3/README.md

<!-- sase:referenced-by:end -->
