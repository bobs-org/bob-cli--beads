# Bead: bob-cli-ir.1 — Capture installs new files without ever replacing one

[Bead Pages](../README.md) / [bob-cli-ir](README.md) / bob-cli-ir.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1a0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1a0.md) · **Assignee:** `bob-cli-ir.1` · **Size:** small
**Created:** 2026-11-08 11:06:11 EST · **Closed:** 2026-11-08 11:28:16 EST
**Plan:** [202611/record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_notes.md)

## Description

no-replace-install: install every newly created capture file with a hard-link no-replace step, so a file that appears mid-commit is refused, never overwritten.

## Notes

[2026-11-08T16:28:16Z · bob-cli-ir.1] New capture files install via hard_link (create_new fallback when Unsupported/EPERM/EXDEV). Intervening creates refuse as NoteChanged ('note was created on disk after planning') without overwriting foreign bytes; earlier writes roll back. Existing edits still rename. just check and just docs-check passed; no leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-ir.3](bob-cli-ir.3.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.5](bob-cli-ir.5.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.1/README.md) | [bob-cli-ir.1](bob-cli-ir.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`971214d`](https://github.com/bobs-org/bob-cli/commit/971214d88b0eb9c7fe2a0199be7f6670645c668c) | feat(capture): install new notes without replacing existing files | [bob-cli-ir.1](bob-cli-ir.1.md) | 2026-11-08 11:29:27 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.1][1] | Need the phase scope, design file, DECISIONS, and notes before implementing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.1/README.md

<!-- sase:referenced-by:end -->
