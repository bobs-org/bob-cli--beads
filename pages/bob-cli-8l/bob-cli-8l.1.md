# Bead: bob-cli-8l.1 — RefsCore close contracts, session close, and copy

[Bead Pages](../README.md) / [bob-cli-8l](README.md) / bob-cli-8l.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.85](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.85.md) · **Assignee:** `bob-cli-8l.1` · **Size:** medium
**Created:** 2026-10-16 14:11:30 EDT · **Closed:** 2026-10-16 14:20:00 EDT
**Plan:** [202610/highlights\_tab\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tab_close.md)

## Description

close-core: pure Foundation additions to RefsCore. They add the close result and outcome types, two new reader requirements with safe protocol-extension defaults (so every existing conformer keeps compiling), and `HighlightsTabsSession.close`, which decides the last-tab quit. They also add the closed-tab stack (reopen decision), the after-removal selection rule, and all close copy (toasts, announcement, failure banner). Golden tests run on Linux with `just portable-check`.

## Notes

[2026-10-16T18:20:00Z · bob-cli-8l.1] close-core done in bob-mac-capture 1f63983: RefsCore close contracts (documentCount, CloseResult/Outcome, close+quitIfNoDocuments with defaults, session.close with last-tab quit, RefsClosedTabs stack, afterRemoving, close copy). just portable-check on athena: lint+build+1288 tests all pass, incl 13 new RefsTabCloseTests. No BobMacCapture* targets touched, so no Mac scratch compile needed.

## Dependencies

- **Blocks:** [bob-cli-8l.2](bob-cli-8l.2.md) ◐ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8l.3](bob-cli-8l.3.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8l.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8l.1/README.md) | [bob-cli-8l.1](bob-cli-8l.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7fd75c8`](https://github.com/bobs-org/bob-mac-capture/commit/7fd75c8835289f92465aaf01c505e932cb4201ab) | feat(refs): add tab-close contracts, session close, and copy | [bob-cli-8l.1](bob-cli-8l.1.md) | 2026-10-16 14:20:54 EDT |
