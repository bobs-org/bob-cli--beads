# Bead: bob-cli-87.3.1.2 — Managed logs, closed appendix, and self-snapshot filtering

[Bead Pages](../README.md) / [bob-cli-87.3.1](bob-cli-87.3.1.md) / bob-cli-87.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.3.md) · **Assignee:** `bob-cli-87.3.1.2` · **Size:** medium
**Created:** 2026-10-16 11:43:19 EDT · **Closed:** 2026-10-16 12:47:01 EDT
**Plan:** [202610/snapshot\_bob\_layer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_bob_layer.md)

## Description

logs-visibility: condense managed logs, support full logs and a compact closed-task appendix through include_closed, filter self-snapshot reference tasks, and finalize omission accounting and visible anchors with read-only regression tests.

## Notes

[2026-10-16T16:47:01Z · bob-cli-87.3.1.2] Bob logs-visibility: reading mode condenses SCHEDULE LOG to moved N× (entries only), WORK LOG to newest WORKED LogRow plus +N older, and hides CANCEL LOG; include_closed prints full logs on open and restored closed tasks. Done/canceled subtrees are omitted with one count each (descendants cannot escape) or restored in a compact Closed tasks appendix with completion/cancelled date chips. Self-snapshot #ref tasks whose linked note source_note resolves to the root are omitted in both modes and counted separately. Anchors rebuild from surviving body plus appendix. Verified cargo test --lib note_snapshot (123 passed), including six statuses, nested closed, omitted/restored links, log punctuation, full logs, both self-ref modes, CountingLoader one-read-per-source, and unchanged source bytes/hashes. sase bead epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-87.3.1.1](bob-cli-87.3.1.1.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-87.3.1.3](bob-cli-87.3.1.3.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.3.1.2/README.md) | [bob-cli-87.3.1.2](bob-cli-87.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`87bc784`](https://github.com/bobs-org/bob-cli/commit/87bc78442fe71c511797751289c84f03ed67b8de) | feat(note-snapshot): condense logs, omit closed tasks, filter self-snapshots | [bob-cli-87.3.1.2](bob-cli-87.3.1.2.md) | 2026-10-16 12:48:25 EDT |
