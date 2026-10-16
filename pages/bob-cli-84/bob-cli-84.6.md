# Bead: bob-cli-84.6 — ⇧⌘O entry point, live wiring, settings, and docs

[Bead Pages](../README.md) / [bob-cli-84](README.md) / bob-cli-84.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7w.md) · **Assignee:** `bob-cli-84.6` · **Size:** medium
**Created:** 2026-10-15 17:50:48 EDT
**Plan:** [202610/highlights\_tabs\_switcher.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tabs_switcher.md)

## Description

tabs-entry: adds `HotKeyAction.refsHighlightsTabs = 4` with a configurable ⇧⌘O/⌘E/Off key that registers only while Highlights is frontmost, and splits the hotkey dispatch so ⌘O and ⌃⇧⌘O are unchanged. Adds coordinator toggle-to-Tabs semantics, wires the live AX reader, session, and ad-hoc flag, and samples recency when Highlights deactivates. Adds the Settings key picker and the README Tabs, keyboard, privacy, and troubleshooting docs, plus the optional decision record.

## Notes

[2026-10-16T12:13:22Z · bob-cli-84.6--2] PROPOSED FOLLOW-UP: Add a decisions record for the Highlights-only Accessibility tab reader — the epic plan explicitly selected decision_record=no, so document the approved scope in a future authorized memory change.

## Dependencies

- **Depends on:** [bob-cli-84.1](bob-cli-84.1.md) ✓ · ⧖ 2026-10-15
- **Depends on:** [bob-cli-84.3](bob-cli-84.3.md) ✓ · ⧖ 2026-10-15
- **Depends on:** [bob-cli-84.5](bob-cli-84.5.md) ✓ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-84.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-84.6.md) | [bob-cli-84.6](bob-cli-84.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1e2a9bd`](https://github.com/bobs-org/bob-mac-capture/commit/1e2a9bd1c3766368b651bc8bf9032e7c8ece13f9) | feat(refs): wire Highlights Tabs entry point and settings | [bob-cli-84.6](bob-cli-84.6.md) | 2026-10-16 08:13:33 EDT |
