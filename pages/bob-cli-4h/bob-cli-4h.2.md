# Bead: bob-cli-4h.2 — Pure Lua ping window model and presentation

[Bead Pages](../README.md) / [bob-cli-4h](README.md) / bob-cli-4h.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.57](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.57.md) · **Assignee:** `bob-cli-4h.2` · **Size:** medium
**Created:** 2026-10-05 11:59:42 EDT · **Closed:** 2026-10-05 12:04:18 EDT
**Plan:** [202610/mac\_menu\_bar\_ping\_indicator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_menu_bar_ping_indicator.md)

## Description

ping-window-model: add the hs-free ping_window.lua module (state parse/serialize, window append and gap reset, tier classification, fixed-width count, RTT parsing, menu bar title and dropdown model) with a busted spec built on the shared contract fixtures.

## Notes

[2026-10-05T16:04:18Z · bob-cli-4h.2] Added home/dot_hammerspoon/ping_window.lua (hs-free model: parse/serialize, append with 40s gap reset and 20-trim, 5-tier classify, U+2007 5-cell counts, RTT parse/format, title segments and dropdown model) and tests/hammerspoon/ping_window_spec.lua on the shared contract fixtures. Verified: new spec 24/24 pass, full hammerspoon suite 88/88 pass, stylua clean on both files, no epic-symbol leftovers. Work left uncommitted in linked chezmoi checkout for the epic land agent.

## Dependencies

- **Blocks:** [bob-cli-4h.3](bob-cli-4h.3.md) ◐ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4h.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4h.2/README.md) | [bob-cli-4h.2](bob-cli-4h.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@69fe995`](https://github.com/bbugyi200/dotfiles/commit/69fe995d423f9d1c21ccc525ad64016ace5d86b0) | feat(hammerspoon): add ping\_window model for ping menubar phase | [bob-cli-4h.2](bob-cli-4h.2.md) | 2026-10-05 12:05:56 EDT |
