# Bead: bob-cli-at.4 — Scan JSON fields, scan receipt, and the Darwin notification

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.4` · **Size:** medium
**Created:** 2026-10-23 11:44:15 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

report: add the additive scan JSON fields (schema stays 1): `summary.held`, `notes[].marker_write {mode, editor_saved_first, status{from,to}?}`, and a top-level `held[] {pdf, note, title, reason, message}` appended after `queued`. Extract one envelope builder shared by JSON and human modes. Every writing `ref scan` that acquired the scan writer lock atomically writes that exact envelope to `<state>/bob-cli/ref/last-scan.json` (0600). That includes human and JSON modes, intake-only drains, and hard failures after the lock. Then, on macOS, it calls `notify_post("org.bobs.bob.ref.scan-finished")`. A receipt failure only warns on stderr. Document the fields, receipt, and notification in highlights-ref-sync.md and the JSON reference.

## Dependencies

- **Depends on:** [bob-cli-at.3](bob-cli-at.3.md) ◐ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-at.5](bob-cli-at.5.md) ◐ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-at.7](bob-cli-at.7.md) ◐ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.4/README.md) | [bob-cli-at.4](bob-cli-at.4.md) | 0 |
