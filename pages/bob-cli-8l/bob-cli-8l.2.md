# Bead: bob-cli-8l.2 — Accessibility close ladder and graceful quit

[Bead Pages](../README.md) / [bob-cli-8l](README.md) / bob-cli-8l.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.85](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.85.md) · **Assignee:** `bob-cli-8l.2` · **Size:** medium
**Created:** 2026-10-16 14:11:30 EDT
**Plan:** [202610/highlights\_tab\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tab_close.md)

## Description

close-reader: `AXHighlightsTabsReader` implements `close` and `quitIfNoDocuments`. A close first tries the tab's own close button, then the window's close button when the tab is visible, and only then selects the tab, closes it, and restores the previously visible tab. Every close is verified by bounded re-reads, and an unsaved-changes sheet is detected and handed to Bryan. When no documents remain, Highlights quits through `NSRunningApplication.terminate()`. The phase also runs a read-only Mac probe and adds a CI test.

## Dependencies

- **Depends on:** [bob-cli-8l.1](bob-cli-8l.1.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8l.2/README.md) | [bob-cli-8l.2](bob-cli-8l.2.md) | 0 |
