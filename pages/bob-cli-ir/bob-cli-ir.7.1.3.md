# Bead: bob-cli-ir.7.1.3 — Transactional capture updates and exact previews

[Bead Pages](../README.md) / [bob-cli-ir.7.1](bob-cli-ir.7.1.md) / bob-cli-ir.7.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.7.md) · **Assignee:** `bob-cli-ir.7.1.3` · **Size:** medium
**Created:** 2026-11-09 02:47:02 EST · **Closed:** 2026-11-09 05:01:59 EST
**Plan:** [202611/record\_append.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_append.md)

## Description

update-writes: stage record updates from the capture batch overlay through the existing guarded writer, expose update note_files and block diffs, and test repeated updates, one-line notes, rollback, dry-run parity, and concurrent edits.

## Notes

[2026-11-09T10:01:59Z · bob-cli-ir.7.1.3] Capture execution now stages record updates through the batch overlay and existing preimage-checked writer. CLI tests cover one-line append, field-only, undated podcasts, missing Notes, messy-byte preservation, list replacement, ordered same-target edits, create-then-update parse/dry-run/commit alignment, mixed drafts, dry-run vs commit bytes, no-op mtime, later-invalid rollback, and historical warnings. Unit tests cover concurrent NoteChanged plus plant-after-update rollback. just docs-gen, just docs-check, and just check passed; generated CLI help no longer claims record_update_reserved.

## Dependencies

- **Depends on:** [bob-cli-ir.7.1.2](bob-cli-ir.7.1.2.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-ir.7.1.4](bob-cli-ir.7.1.4.md) ◐ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-ir.7.1.5](bob-cli-ir.7.1.5.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.3/README.md) | [bob-cli-ir.7.1.3](bob-cli-ir.7.1.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.7.1.3][1] | Need remaining bead fields: notes, design, decisions, and prior work | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.3/README.md

<!-- sase:referenced-by:end -->
