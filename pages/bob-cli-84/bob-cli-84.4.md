# Bead: bob-cli-84.4 — Panel model Tabs filter, switching, and states

[Bead Pages](../README.md) / [bob-cli-84](README.md) / bob-cli-84.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7w.md) · **Assignee:** `bob-cli-84.4` · **Size:** medium
**Created:** 2026-10-15 17:50:48 EDT
**Plan:** [202610/highlights\_tabs\_switcher.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tabs_switcher.md)

## Description

tabs-model: RefsPanelModel gains the presentation source, the `tabsFilter` flag, the tabs state, and the tab-row map. It handles ⌘T and ⌘R re-snapshots, the Esc/⌫ ladder, and a ↵ held until the first snapshot lands. Matched rows switch through `openInHighlights` without `recordOpen`; collision and unmatched rows switch through the session's select, with a stale-tab banner. Synthetic rows survive library publications. Preview hooks and model tests use a fake reader.

## Dependencies

- **Depends on:** [bob-cli-84.2](bob-cli-84.2.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-84.5](bob-cli-84.5.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-84.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.4/README.md) | [bob-cli-84.4](bob-cli-84.4.md) | 0 |
