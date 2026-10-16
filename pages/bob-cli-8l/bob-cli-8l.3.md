# Bead: bob-cli-8l.3 — Panel close commands, queue, outcomes, keys, and toasts

[Bead Pages](../README.md) / [bob-cli-8l](README.md) / bob-cli-8l.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.85](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.85.md) · **Assignee:** `bob-cli-8l.3` · **Size:** medium
**Created:** 2026-10-16 14:11:30 EDT
**Plan:** [202610/highlights\_tab\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tab_close.md)

## Description

close-model: RefsPanelModel gains ⌃D close commands. A close removes the row optimistically and moves the selection to its neighbour; closes run one at a time in press order; each outcome maps to a toast, banner, state card, or hide. The router sends ⌃D to close only while a tab row is selected (scroll otherwise) and maps ⇧⌘T to reopen. The controller shows the glass toasts. ⌘K gains Close Tab. Model, router, and actions-menu tests run against a fake reader.

## Dependencies

- **Depends on:** [bob-cli-8l.1](bob-cli-8l.1.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8l.4](bob-cli-8l.4.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8l.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8l.3.md) | [bob-cli-8l.3](bob-cli-8l.3.md) | 0 |
