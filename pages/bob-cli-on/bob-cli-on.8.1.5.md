# Bead: bob-cli-on.8.1.5 — CLI, capability gate, JSON, and human output

[Bead Pages](../README.md) / [bob-cli-on.8.1](bob-cli-on.8.1.md) / bob-cli-on.8.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.md) · **Assignee:** `bob-cli-on.8.1.5` · **Size:** medium
**Created:** 2026-11-22 07:22:30 EST · **Closed:** 2026-11-22 13:37:22 EST
**Plan:** [202611/requirement\_close\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/requirement_close_engine.md)

## Description

capture: connect the requirement pipeline to every managed capture Done entry, add carry and req-choice arguments, publish groups and receipts, preserve old-client defaults, and cover the public CLI flow end to end.

## Notes

[2026-11-22T17:37:42Z · bob-cli-on.8.1.5] Contract locations for parent land: docs/task-dependencies.md §12.5 (requirement rows, handshake, numbering, receipts), docs/reference/json-outputs.md (always-present pull_in.reqs plus optional groups/rows/copy extras and CaptureResult.req_outcomes), CLI -k/--carry after cancel-offer and hidden --req-choice. Fixture revision: tests/fixtures/note_pull JSON gained pull_in.reqs {supported,pending}. Phase 6 owns §§12.25/12.26.

[2026-11-22T18:37:22Z · bob-cli-on.8.1.5--2] Closed by explicit `sase stitch create -B close` after create_commit landed 7073b7c8 ("feat(capture)!: publish requirement close on the successor card"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-on.8.1.5` if more work remains.

## Dependencies

- **Depends on:** [bob-cli-on.8.1.4](bob-cli-on.8.1.4.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.8.1.6](bob-cli-on.8.1.6.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.8.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.1.5.md) | [bob-cli-on.8.1.5](bob-cli-on.8.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7073b7c`](https://github.com/bobs-org/bob-cli/commit/7073b7c879b8cc853ee3b9a1072326dd185cba85) | feat(capture)!: publish requirement close on the successor card | [bob-cli-on.8.1.5](bob-cli-on.8.1.5.md) | 2026-11-22 13:36:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.8.1.5--2][1] | Confirm phase 5 close eligibility | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.1.5.md

<!-- sase:referenced-by:end -->
