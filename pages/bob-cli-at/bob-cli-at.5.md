# Bead: bob-cli-at.5 — Bob Mac Capture core decoding and open-PDF presentation

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.5` · **Size:** medium
**Created:** 2026-10-23 11:44:16 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

mac-core: in the linked bob-mac-capture repo, RefsCore decodes the new scan fields tolerantly. Those are `generated_at`, `summary.held`, `held[]` (lossy rows), and `notes[].marker_write`. Add a bounded receipt reader that resolves the path like bob: `XDG_STATE_HOME`, else `~/.local/state`. Add a pure `RefsPDFUpdates` classifier that takes a response plus optional open-tab file names. It splits entries into refreshed-open, refreshed-quiet, reading holds, busy holds, and changed holds, and supplies dedupe keys. Add the exact copy deck for notifications, footer clauses, and the busy banner, using the Refs state vocabulary. Unit-test it all and run `just portable-check`.

## Dependencies

- **Depends on:** [bob-cli-at.4](bob-cli-at.4.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-at.6](bob-cli-at.6.md) ◐ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.5/README.md) | [bob-cli-at.5](bob-cli-at.5.md) | 0 |
