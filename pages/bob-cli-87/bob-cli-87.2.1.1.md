# Bead: bob-cli-87.2.1.1 — Snapshot model and projected Markdown contract

[Bead Pages](../README.md) / [bob-cli-87.2.1](bob-cli-87.2.1.md) / bob-cli-87.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.md) · **Assignee:** `bob-cli-87.2.1.1` · **Size:** medium
**Created:** 2026-10-16 07:26:12 EDT · **Closed:** 2026-10-16 08:20:12 EDT
**Plan:** [202610/snapshot\_view\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_view_core.md)

## Description

model-contract: define the engine-neutral snapshot model, lossless source metadata, serializer, and synthetic contract fixture. Establish the crate-visible seams that the remaining child phases and the outer Bob-layer and print-profile phases use.

## Notes

[2026-10-16T12:20:12Z · bob-cli-87.2.1.1--4] Verified the engine-neutral model and serializer against the hand-authored contract fixture; model-generated golden remains separately harness-managed. Focused note_snapshot tests and just check completed successfully, and epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-87.2.1.2](bob-cli-87.2.1.2.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.1.md) | [bob-cli-87.2.1.1](bob-cli-87.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`426b07c`](https://github.com/bobs-org/bob-cli/commit/426b07ca0286312d794d260475deba4a42422864) | feat(highlights): add snapshot model and markdown contract | [bob-cli-87.2.1.1](bob-cli-87.2.1.1.md) | 2026-10-16 08:28:56 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.2.1.1--4][1] | Need structured phase fields and attached design references | 2 |
| read-by | [agent:bob-cli-87.2.1.land--1][2] | Review the first completed child scope and notes for landing completeness | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.land.md

<!-- sase:referenced-by:end -->
