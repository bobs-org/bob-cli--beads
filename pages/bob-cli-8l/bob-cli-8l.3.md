# Bead: bob-cli-8l.3 — Panel close commands, queue, outcomes, keys, and toasts

[Bead Pages](../README.md) / [bob-cli-8l](README.md) / bob-cli-8l.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.85](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.85.md) · **Assignee:** `bob-cli-8l.3` · **Size:** medium
**Created:** 2026-10-16 14:11:30 EDT · **Closed:** 2026-10-16 15:16:36 EDT
**Plan:** [202610/highlights\_tab\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tab_close.md)

## Description

close-model: RefsPanelModel gains ⌃D close commands. A close removes the row optimistically and moves the selection to its neighbour; closes run one at a time in press order; each outcome maps to a toast, banner, state card, or hide. The router sends ⌃D to close only while a tab row is selected (scroll otherwise) and maps ⇧⌘T to reopen. The controller shows the glass toasts. ⌘K gains Close Tab. Model, router, and actions-menu tests run against a fake reader.

## Notes

[2026-10-16T19:16:36Z · bob-cli-8l.3--4] Verified close-model: just portable-check on athena scratch copy and just bundle && just typecheck-tests on macOS scratch copy both passed (monitor ywv03nat9bqg, tool run 9fdfec2f61468b5ec3dad8475e5dc9e8, exit 0). Epic-symbols were empty. ⌃D close queue, neighbour selection, ⇧⌘T reopen, ⌘K Close Tab, glass toasts, and model/router/actions-menu tests are in bob-mac-capture.

## Dependencies

- **Depends on:** [bob-cli-8l.1](bob-cli-8l.1.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8l.4](bob-cli-8l.4.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8l.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8l.3.md) | [bob-cli-8l.3](bob-cli-8l.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7954c28`](https://github.com/bobs-org/bob-mac-capture/commit/7954c28aec7d25e5a5ba42633a1b2436a3b2f74e) | feat(refs): close Highlights tabs with ⌃D from the panel | [bob-cli-8l.3](bob-cli-8l.3.md) | 2026-10-16 15:18:42 EDT |
