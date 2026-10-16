# Bead: bob-cli-8l.4 — Row close button, footer, inspector hint, motion, design tests, and README

[Bead Pages](../README.md) / [bob-cli-8l](README.md) / bob-cli-8l.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.85](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.85.md) · **Assignee:** `bob-cli-8l.4` · **Size:** medium
**Created:** 2026-10-16 14:11:30 EDT · **Closed:** 2026-10-16 15:38:08 EDT
**Plan:** [202610/highlights\_tab\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tab_close.md)

## Description

close-views: Tabs rows show a quiet close button on hover and selection in a reserved trailing column, and the row exposes a VoiceOver "Close Tab" action. Removals fold out with a short animation (fade only under Reduce Motion). The footer reads "↵ Switch  ⌃D Close Tab", and the inspector card hint and the closed-tab toast style are added, with design fixtures for each. The README covers ⌃D, the last-tab quit, reopen, Privacy, and Troubleshooting.

## Notes

[2026-10-16T19:38:08Z · bob-cli-8l.4] close-views: Tabs rows reserve an 18pt close column with xmark.circle.fill on hover/selection, VoiceOver Close Tab action, and fold-out removal (opacity-only under Reduce Motion). Footer leads with ⌃D Close Tab (Reveal drops first at 760pt); inspector hint is ↵ switches · ⌃D closes; closedTab toasts render with and without detail. README covers ⌃D, last-tab quit, ⇧⌘T reopen, Privacy, Troubleshooting, and ⌘K Close Tab. Verified just portable-check on athena (1290 tests) and Mac scratch bundle.sh + just typecheck-tests.

## Dependencies

- **Depends on:** [bob-cli-8l.3](bob-cli-8l.3.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8l.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8l.4/README.md) | [bob-cli-8l.4](bob-cli-8l.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7ee2499`](https://github.com/bobs-org/bob-mac-capture/commit/7ee2499aa77d358f05b5e4a00a91937c925e076c) | feat(refs): add Tabs close button, fold-out, and close copy | [bob-cli-8l.4](bob-cli-8l.4.md) | 2026-10-16 15:39:34 EDT |
