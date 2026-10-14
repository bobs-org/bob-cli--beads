# Bead: bob-cli-7k.4 — Wire ⌃Y, the card lifecycle, hide-on-copy, ⌘K, footer, and README

[Bead Pages](../README.md) / [bob-cli-7k](README.md) / bob-cli-7k.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.19.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.19.linker.w0.md) · **Assignee:** `bob-cli-7k.4` · **Size:** medium
**Created:** 2026-10-14 09:32:31 EDT · **Closed:** 2026-10-14 11:01:27 EDT
**Plan:** [202610/refs\_ctrl\_y\_copy\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_ctrl_y_copy_card.md)

## Description

refs-copy-integration: route ⌃Y and every card key, own the card lifecycle in RefsPanelModel, copy then hide Refs (or return to Capture) and show the HUD, fold ⌘K's copy items into Copy…, update the footer, the Esc ladder, and the README, and add tests.

## Notes

[2026-10-14T15:01:07Z · bob-cli-7k.4--6] PROPOSED FOLLOW-UP: Resolve the clean-base macOS typecheck failure `unable to load standard library for target arm64-apple-macosx26.0`; it reproduces on pristine HEAD while portable-check passes.

[2026-10-14T15:01:27Z · bob-cli-7k.4--6] Verified Scripts/bundle.sh completes on macOS; typecheck-tests reaches test compilation but fails with unable to load standard library for arm64-apple-macosx26.0, reproduced identically on pristine HEAD. Athena portable-check passed with 1,139 tests and zero failures. Recorded the clean-base toolchain issue as a PROPOSED FOLLOW-UP; no epic symbols remain; macOS and athena scratch copies cleaned.

## Dependencies

- **Depends on:** [bob-cli-7k.1](bob-cli-7k.1.md) ✓ · ⧖ 2026-10-14
- **Depends on:** [bob-cli-7k.3](bob-cli-7k.3.md) ✓ · ⧖ 2026-10-14
- **Blocks:** [bob-cli-7k.5](bob-cli-7k.5.md) ◐ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7k.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7k.4.md) | [bob-cli-7k.4](bob-cli-7k.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c4b1a25`](https://github.com/bobs-org/bob-mac-capture/commit/c4b1a257db3bdde636697d7f22aee6aab7285417) | feat(refs): wire copy card interactions and footer | [bob-cli-7k.4](bob-cli-7k.4.md) | 2026-10-14 11:02:14 EDT |
