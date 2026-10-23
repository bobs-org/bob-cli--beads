# Bead: bob-cli-at.4 — Scan JSON fields, scan receipt, and the Darwin notification

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.4` · **Size:** medium
**Created:** 2026-10-23 11:44:15 EDT · **Closed:** 2026-10-23 14:31:08 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

report: add the additive scan JSON fields (schema stays 1): `summary.held`, `notes[].marker_write {mode, editor_saved_first, status{from,to}?}`, and a top-level `held[] {pdf, note, title, reason, message}` appended after `queued`. Extract one envelope builder shared by JSON and human modes. Every writing `ref scan` that acquired the scan writer lock atomically writes that exact envelope to `<state>/bob-cli/ref/last-scan.json` (0600). That includes human and JSON modes, intake-only drains, and hard failures after the lock. Then, on macOS, it calls `notify_post("org.bobs.bob.ref.scan-finished")`. A receipt failure only warns on stderr. Document the fields, receipt, and notification in highlights-ref-sync.md and the JSON reference.

## Notes

[2026-10-23T18:31:08Z · bob-cli-at.4] Implemented scan JSON held fields (summary.held, notes[].marker_write, top-level held[]), shared envelope builder, scan receipt writer (0600/0700, temp+rename) with macOS notify_post, wired into human/JSON full scans and intake-only drains incl. hard failures after the lock. Verified: cargo fmt, clippy gates, full cargo test suite green (3205+1961 passed), docs-check 447 passed.

## Dependencies

- **Depends on:** [bob-cli-at.3](bob-cli-at.3.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-at.5](bob-cli-at.5.md) ◐ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-at.7](bob-cli-at.7.md) ◐ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.4/README.md) | [bob-cli-at.4](bob-cli-at.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`faa9a75`](https://github.com/bobs-org/bob-cli/commit/faa9a7579d681a4ccbfe47c39155b183df1ec13a) | feat(highlights-ref): add scan JSON held fields, scan receipt, and Darwin notification | [bob-cli-at.4](bob-cli-at.4.md) | 2026-10-23 14:32:05 EDT |
