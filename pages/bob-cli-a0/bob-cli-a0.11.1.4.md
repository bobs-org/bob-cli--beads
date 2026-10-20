# Bead: bob-cli-a0.11.1.4 — Migrate troubleshooting, finish the README front door, and verify coverage

[Bead Pages](../README.md) / [bob-cli-a0.11.1](bob-cli-a0.11.1.md) / bob-cli-a0.11.1.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.11.md) · **Assignee:** `bob-cli-a0.11.1.4` · **Size:** medium
**Created:** 2026-10-20 03:05:22 EDT
**Plan:** [202610/mac\_capture\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_reference.md)

## Description

guides-front-door: Move both troubleshooting sections into goal-titled bob-cli Fix problems guides, finish all cross-links and search cases, audit every original README section, then replace the README with a useful front door retaining an exact Signing heading. Validate both builders and the combined docs gate. Close only the assigned child phase; leave bob-cli-a0.11 for this child epic's land agent.

## Notes

[2026-10-20T11:28:29Z · bob-cli-a0.11.1.4] README-section-to-destination mapping (guides-front-door, audited against README at 065908f / HEAD bd9b1e2; README unchanged since baseline before this rewrite): Introduction -> README front door plus reference/mac-capture and develop/mac-capture hubs. Requirements platform/toolchain/bob paths -> install.md; capabilities/fallbacks -> protocol.md. Development recipes -> develop/build.md. Signing (stable Bob Mac Capture Local identity, Keychain Access steps, codesign verify) stays on README ## Signing; full keychain unlock/mismatch/errSecInternalComponent -> install.md#signing. Menu-Bar Icon -> diagnostics.md; glyph fixtures -> develop/build.md and develop/render-fixtures.md. Runtime Contract including pickers -> capture-panel.md, pickers.md, task-pickers.md, relationship-pickers.md, capture-previews.md, protocol.md, develop/architecture.md. Completing with ! and Saving links -> capture-previews.md / capture-panel.md. Bob Refs Data/Updates/Sorting/NEW/Tuning/panel/Copy/Rename/Link to Today/Opening/Tabs -> refs.md plus keyboard.md. Inspector -> refs-inspector.md. Bob Refs Privacy -> permissions.md. Idle agenda -> idle-agenda.md. Keyboard including shelf and Control-\ -> keyboard.md. Saved templates -> saved-templates.md and settings.md. Wikilink Completion -> wikilink-completion.md. Live Preview and Clipboard Semantics -> capture-panel.md. Notifications copy -> settings.md; authorization/signed-bundle -> permissions.md. Hotkey Registry, Conflicts, Launch at Login -> keyboard.md, settings.md, permissions.md. Updating/Reinstalling/Rollback and Uninstalling -> install.md. Privacy -> permissions.md. Diagnostics and Signposts -> diagnostics.md. CI -> develop/ci.md and develop/render-fixtures.md. Troubleshooting: swift test XCTest -> develop/build.md; Bob is not resolved, timeouts, Target cache stale, wikilink empty/warning -> guides/fix-mac-capture-bob-resolution.md; Hotkey conflict / Refs hotkey conflict -> guides/resolve-mac-capture-hotkey-conflict.md; notifications, install-complete banner, Accessibility/tccutil, launch-at-login -> guides/restore-mac-capture-permissions.md; Bob Refs load/Highlights/scan/tab-close/Reset Open History -> guides/recover-bob-refs.md (dirty vault reuses resolve-vault-conflict-copy; stuck clip jobs reuse recover-reference-job); retained drafts, block-ID errors/focus, slow paste, Restart failed, missing menu-bar icon -> guides/recover-mac-capture.md.

## Dependencies

- **Depends on:** [bob-cli-a0.11.1.3](bob-cli-a0.11.1.3.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.11.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.11.1.4/README.md) | [bob-cli-a0.11.1.4](bob-cli-a0.11.1.4.md) | 0 |
