# Bead: bob-cli-c9.1 — Reading families in the library read model

[Bead Pages](../README.md) / [bob-cli-c9](README.md) / bob-cli-c9.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14a](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14a.md) · **Assignee:** `bob-cli-c9.1` · **Size:** medium
**Created:** 2026-10-25 14:15:31 EDT · **Closed:** 2026-10-25 15:04:35 EDT
**Plan:** [202610/ref\_create\_force\_recapture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_force_recapture.md)

## Description

family: teach ref_library the note-local earlier: list, reading numbers, and families. Doctor stops flagging families as duplicate_identity, find/show/resolve rank the newest reading first, list/show render vN chips and earlier/later rows, and JSON grows additively; uses hand-written fixtures only.

## Notes

[2026-10-25T19:04:35Z · bob-cli-c9.1] Family read model landed: lineage module parses note-local earlier: (Reading/Replaced) with reading numbers; build_index resolves families; duplicate_identity exempt within one family (cross-family pairs still warn) and superseded_by winner is newest reading; doctor identity row shares the exemption plus earlier_dangling warning; newest-first primary ranking; show collapses all-one-family hits to newest with reason-aware also lines, earlier:/later: rows, vN/v1 chips, later in JSON; sync round trip keeps block earlier: byte-for-byte (fixed orphaned-continuation absorption in render_with_projection, proven by failing-then-passing tests); hand-written fixture tests for find/show/list/doctor/rename incl. dangling-middle and protocol__v2 cases; rename of a family member verified (failed pre-fix with duplicate_identity, passes now, earlier: link rewritten). Verified: cargo fmt, clippy gate (-D unused), full cargo test --no-fail-fast green, just docs-check 447 passed. docs/ref.md + docs/highlights-ref-sync.md updated. Changes left uncommitted for the land agent.

## Dependencies

- **Blocks:** [bob-cli-c9.3](bob-cli-c9.3.md) ◐ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.1/README.md) | [bob-cli-c9.1](bob-cli-c9.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`16f86b7`](https://github.com/bobs-org/bob-cli/commit/16f86b7df6d9e8ee69822404ada9092ba8220339) | feat(ref): reading families in the library read model | [bob-cli-c9.1](bob-cli-c9.1.md) | 2026-10-25 15:05:38 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.1/README.md

<!-- sase:referenced-by:end -->
