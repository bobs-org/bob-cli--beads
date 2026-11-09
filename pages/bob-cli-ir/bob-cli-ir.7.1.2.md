# Bead: bob-cli-ir.7.1.2 — Record update grammar and editor parse

[Bead Pages](../README.md) / [bob-cli-ir.7.1](bob-cli-ir.7.1.md) / bob-cli-ir.7.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.7.md) · **Assignee:** `bob-cli-ir.7.1.2` · **Size:** medium
**Created:** 2026-11-09 02:47:02 EST · **Closed:** 2026-11-09 03:55:09 EST
**Plan:** [202611/record\_append.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_append.md)

## Description

update-language: recognize @dir/stem as RecordUpdate in strict and editor parsing, resolve update metadata through the shared planner, expose current field values, and preserve record claiming, opaque values, and precise byte ranges.

## Notes

[2026-11-09T08:55:09Z · bob-cli-ir.7.1.2] Implemented update parsing, planner-backed current-field metadata, exact nested stem ranges, docs, and grammar revision 21; capture execution remains fail-closed with no file mutation. Verified cargo check --lib, focused update parser unit tests, both update CLI integration tests, cargo fmt --check, git diff --check, and no remaining epic symbols.

## Dependencies

- **Depends on:** [bob-cli-ir.7.1.1](bob-cli-ir.7.1.1.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-ir.7.1.3](bob-cli-ir.7.1.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.2/README.md) | [bob-cli-ir.7.1.2](bob-cli-ir.7.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1264176`](https://github.com/bobs-org/bob-cli/commit/126417682efc6774a8257e6abef6c638d6e24fb7) | feat(capture): parse existing record updates | [bob-cli-ir.7.1.2](bob-cli-ir.7.1.2.md) | 2026-11-09 04:19:04 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.7.1.2][1] | Need the assigned phase scope, earlier notes, epic decisions, and linked design file before continuing work | 2 |
| read-by | [agent:bob-cli-ir.7.1.3][2] | Need prior phase notes and what landed for update-language | 1 |
| read-by | [agent:bob-cli-ir.7.1.5][3] | Need sibling phase status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.5/README.md

<!-- sase:referenced-by:end -->
