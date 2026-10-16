# Bead: bob-cli-87.5 — bob ref create integration, provenance, help, and docs

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.5` · **Size:** large
**Created:** 2026-10-16 07:13:18 EDT · **Closed:** 2026-10-16 15:39:25 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

create-wiring: wire everything into create. Covers vault-note and route TARGETs, -P default, dated stem and title, the notes ref type, -C and -M, dry-run and success output, the source_note marker field, listen input, the help 'Vault notes' block, docs, and CLI tests.

## Notes

[2026-10-16T19:39:25Z · bob-cli-87.5--2] Implemented the approved note snapshot create wiring across create routing/defaults, metadata and markers, listen input, help/docs, and CLI coverage. Verification: just check passed on rerun (exit 0; 2026-10-16). sase bead epic-symbols reported no --epic-symbol entries for this phase, so no stale symbols required re-keying.

## Dependencies

- **Blocks:** [bob-cli-87.10](bob-cli-87.10.md) ◐ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.3](bob-cli-87.3.md) ✓ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.4](bob-cli-87.4.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-87.6](bob-cli-87.6.md) ◐ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-87.7](bob-cli-87.7.md) ◐ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-87.8](bob-cli-87.8.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.5.md) | [bob-cli-87.5](bob-cli-87.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`07fef5f`](https://github.com/bobs-org/bob-cli/commit/07fef5f02c9a572b02ea1a9d7bb1a4f265a2b6eb) | feat(ref): wire note snapshot creation | [bob-cli-87.5](bob-cli-87.5.md) | 2026-10-16 15:40:04 EDT |
