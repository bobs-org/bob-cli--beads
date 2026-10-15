# Bead: bob-cli-84.3 — Highlights-only Accessibility reader

[Bead Pages](../README.md) / [bob-cli-84](README.md) / bob-cli-84.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7w.md) · **Assignee:** `bob-cli-84.3` · **Size:** medium
**Created:** 2026-10-15 17:50:48 EDT
**Plan:** [202610/highlights\_tabs\_switcher.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tabs_switcher.md)

## Description

ax-reader: `AXHighlightsTabsReader` in BobMacCapture implements the RefsCore reader protocol, using only public AX API against Highlights' process. It never launches Highlights, never prompts, and works off the main actor with messaging timeouts and a time budget. It reads window AXDocument and the native tab bar, and presses one verified tab button for select. Tab names stay in memory only. An optional read-only probe runs on the Mac.

## Dependencies

- **Depends on:** [bob-cli-84.1](bob-cli-84.1.md) ✓ · ⧖ 2026-10-15
- **Depends on:** [bob-cli-84.2](bob-cli-84.2.md) ◐ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-84.6](bob-cli-84.6.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-84.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.3/README.md) | [bob-cli-84.3](bob-cli-84.3.md) | 0 |
