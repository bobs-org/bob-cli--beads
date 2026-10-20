# Bead: bob-cli-a0.11.1.2 — Extract installation, settings, permissions, and Bob Refs reference

[Bead Pages](../README.md) / [bob-cli-a0.11.1](bob-cli-a0.11.1.md) / bob-cli-a0.11.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.11.md) · **Assignee:** `bob-cli-a0.11.1.2` · **Size:** medium
**Created:** 2026-10-20 03:05:22 EDT · **Closed:** 2026-10-20 03:47:00 EDT
**Plan:** [202610/mac\_capture\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_reference.md)

## Description

application-reference: Extract the remaining application reference into install, settings, permissions, diagnostics, refs, refs-inspector, and developer build/CI pages. Extend nav and the protocol compatibility table. Keep troubleshooting and the original README available until the final migration phase. Follow application-reference below.

## Notes

[2026-10-20T07:46:44Z · bob-cli-a0.11.1.2] README-section-to-destination mapping (application-reference): Requirements platform/toolchain/bob paths + login-shell para -> install.md; capability list stays protocol.md. Development recipes + toolchain -> develop/build.md; install-relevant bundle/install identity split also in install.md. Signing (stable Bob Mac Capture Local identity, keychain unlock/mismatch, errSecInternalComponent, codesign verify) -> install.md. Menu-Bar Icon states -> diagnostics.md; glyph render filter and StatusItemGlyph path -> develop/build.md. Bob Refs Data/Updates/Sorting/NEW/Tuning/panel/Copy/Rename/Link to Today/Opening/Tabs -> refs.md. Inspector -> refs-inspector.md. Bob Refs Privacy + capture Privacy -> permissions.md (source-verified: References persist refsHotkeyEnabled as Control-Shift-Command-O, not the README's ⌃⇧⌘R capture-toggle key). Bob Refs Troubleshooting and ## Troubleshooting stay README anchors until guides-front-door. Notifications copy + Settings controls -> settings.md; authorization/signed-bundle requirement -> permissions.md. Hotkey Registry/conflicts -> settings.md Hotkey + diagnostics.md; Launch at Login -> settings.md Launch + permissions.md. Updating/Reinstalling/Rollback + Uninstalling -> install.md. Diagnostics and Signposts + timeouts + Copy Diagnostic + refs-rank invocation -> diagnostics.md. CI workflow + render-fixtures artifact mention -> develop/ci.md. SettingsView order Bob/Hotkey/References/Agenda/Canceled Draft Stash/Saved Templates/Launch/Notifications/Diagnostics verified against AppSettings defaults (production hotkey on, refs hotkey on, agenda on, stash capacity 10, inspector page size 5, Highlights open Command-O, Tabs Shift-Command-O). Protocol compatibility table extended with ref list/plan/scan/show/rename, vault-sync -q, blocked/task/added_at/marker_id. Hubs and nav updated; search smoke added for "Bob Mac Capture Local" and refs-rank. README left intact.

[2026-10-20T07:47:00Z · bob-cli-a0.11.1.2] application-reference done: 8 Mac pages (install, settings, permissions, refs, refs-inspector, diagnostics, develop/build, develop/ci) extracted from README and SettingsView/AppSettings; protocol compatibility table extended with Refs commands/fields; nav and hubs updated. just docs-check exit 0 with BOB_DOCS_BOB_MAC_CAPTURE_DIR at the SASE-opened Mac checkout: strict Zensical, 140 published pages, lychee 0 errors, search smoke 97 cases including Bob Mac Capture Local and refs-rank, 418 pytest. Settings defaults verified against AppSettings (production hotkey on, refs hotkey on, agenda on, stash 10, inspector page 5). README intact, no Swift changes. epic-symbols: none leftover. Troubleshooting remains on README until guides-front-door.

## Dependencies

- **Depends on:** [bob-cli-a0.11.1.1](bob-cli-a0.11.1.1.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a0.11.1.3](bob-cli-a0.11.1.3.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.11.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.11.1.2/README.md) | [bob-cli-a0.11.1.2](bob-cli-a0.11.1.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8ba2995`](https://github.com/bobs-org/bob-cli/commit/8ba29959d4aab047bff060c2bc082bbb92213803) | docs(mac-capture): wire application-reference hubs and search smoke | [bob-cli-a0.11.1.2](bob-cli-a0.11.1.2.md) | 2026-10-20 03:48:27 EDT |
| bob-mac-capture | [`bob-mac-capture@3b944d8`](https://github.com/bobs-org/bob-mac-capture/commit/3b944d877a7a0890b29c2d8d5d93d2c677d4b9d5) | docs: extract install, settings, permissions, and Bob Refs reference | [bob-cli-a0.11.1.2](bob-cli-a0.11.1.2.md) | 2026-10-20 03:49:51 EDT |
