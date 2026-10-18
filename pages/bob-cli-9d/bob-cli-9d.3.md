# Bead: bob-cli-9d.3 — Panel: ⌘0 toggle, Newest token, headers, footer, README

[Bead Pages](../README.md) / [bob-cli-9d](README.md) / bob-cli-9d.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11j](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11j.md) · **Assignee:** `bob-cli-9d.3` · **Size:** medium
**Created:** 2026-10-18 15:40:20 EDT · **Closed:** 2026-10-18 16:36:33 EDT
**Plan:** [202610/refs\_newest\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_newest_mode.md)

## Description

refs-panel-newest: route ⌘0, hold the mode in the panel model (exclusive with Tabs, Esc and Backspace ladders), draw the token, date headers, footer hints, and inspector time, wire the git-lane merge, and document the mode.

## Notes

[2026-10-18T20:36:33Z · bob-cli-9d.3] Implemented refs-panel-newest in bob-mac-capture: ⌘0 toggles Newest (Caps Lock ignored, IME/Shift/keypad unbound), exclusive with Tabs, persistence=reset on every show, Esc/Backspace peel Tabs then Newest then scope. Search-bar Newest token, date-group headers with trailing detail, footer ⌘0 Newest/Library ladders, inspector Added time, RefsLibrary carries gitAddedAt and merges via mergingGitDates. README keyboard/prose updated. Verified: just portable-check green (1368 tests). Mac SSH timed out (kellys-macbook-pro offline); BobMacCapture bundle/typecheck-tests unverified.

## Dependencies

- **Depends on:** [bob-cli-9d.2](bob-cli-9d.2.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9d.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9d.3/README.md) | [bob-cli-9d.3](bob-cli-9d.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7d6063a`](https://github.com/bobs-org/bob-mac-capture/commit/7d6063a66a38e289644ef3a69a3abcad173af9a4) | feat(refs): add ⌘0 Newest mode to the Bob Refs panel | [bob-cli-9d.3](bob-cli-9d.3.md) | 2026-10-18 16:38:35 EDT |
