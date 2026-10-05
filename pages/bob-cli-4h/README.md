# Bead: bob-cli-4h — Mac menu bar internet ping indicator sharing one ping stream with tmux\_ping

[Bead Pages](../README.md) / bob-cli-4h

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.57](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.57.md) · **Assignee:** `bob-cli-4h.land`
**Created:** 2026-10-05 11:59:42 EDT
**Plan:** [202610/mac\_menu\_bar\_ping\_indicator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_menu_bar_ping_indicator.md)

## Description

The MacBook menu bar shows the same last-20 ping count as the tmux status bar, styled as a sibling of the Pomodoro item, while a single shared ping stream feeds both displays: never more than one ping to 8.8.8.8 every 2 s, and none while the Mac is locked.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-4h.1](bob-cli-4h.1.md) | tmux\_ping becomes a shared-state reader with a fallback pinger | ✓ closed | medium | 2026-10-05 | 1 | 1 |
| [bob-cli-4h.2](bob-cli-4h.2.md) | Pure Lua ping window model and presentation | ✓ closed | medium | 2026-10-05 | 1 | 1 |
| [bob-cli-4h.3](bob-cli-4h.3.md) | Hammerspoon ping menu bar runtime, init wiring, and README | ✓ closed | medium | 2026-10-05 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-4h: Mac menu bar internet ping indicator sharing one ping stream with tmux_ping [in_progress]"]
    n1["bob-cli-4h.1: tmux_ping becomes a shared-state reader with a fallback pinger [closed]"]
    n2["bob-cli-4h.2: Pure Lua ping window model and presentation [closed]"]
    n3["bob-cli-4h.3: Hammerspoon ping menu bar runtime, init wiring, and README [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n3
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4h.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4h.1/README.md) | [bob-cli-4h.1](bob-cli-4h.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-4h.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4h.2/README.md) | [bob-cli-4h.2](bob-cli-4h.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-4h.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4h.3/README.md) | [bob-cli-4h.3](bob-cli-4h.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-4h.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4h.land/README.md) | [bob-cli-4h](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@69fe995`](https://github.com/bbugyi200/dotfiles/commit/69fe995d423f9d1c21ccc525ad64016ace5d86b0) | feat(hammerspoon): add ping\_window model for ping menubar phase | [bob-cli-4h.2](bob-cli-4h.2.md) | 2026-10-05 12:05:56 EDT |
| chezmoi | [`chezmoi@331f072`](https://github.com/bbugyi200/dotfiles/commit/331f0729f6701e9a341bf5023a1951d0ecbb2522) | feat(tmux): tmux\_ping reads shared ping state with fallback pinger | [bob-cli-4h.1](bob-cli-4h.1.md) | 2026-10-05 12:11:53 EDT |
| chezmoi | [`chezmoi@e48f04f`](https://github.com/bbugyi200/dotfiles/commit/e48f04f6f588f96741232e5a556efedf057d37ee) | feat(ping): Hammerspoon ping menu bar runtime, init wiring, and README | [bob-cli-4h.3](bob-cli-4h.3.md) | 2026-10-05 12:23:00 EDT |
