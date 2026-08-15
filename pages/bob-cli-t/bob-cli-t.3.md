# Bead: bob-cli-t.3 — Deliver complete, polished single and batch notifications

[Bead Pages](../README.md) / [bob-cli-t](README.md) / bob-cli-t.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.024.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.024.w1.md) · **Assignee:** `bob-cli-t.3` · **Size:** small
**Created:** 2026-08-15 09:47:54 EDT · **Closed:** 2026-08-15 11:14:09 EDT
**Plan:** [202608/multi\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/multi_capture.md)

## Description

mac_notification_polish: render richer ordered notification summaries and route singular or plural open actions to every unique captured destination.

## Notes

[2026-08-15T14:27:38Z · 02b] RELATED SWIFT 6 DIAGNOSTICS: The same install log ends with NotificationService warnings because @MainActor-isolated static identifiers/options are read by intentionally nonisolated content builders, routing helpers, and UNUserNotificationCenterDelegate methods. These warnings are not the current exit-1 cause, but become errors in Swift 6 mode and this phase owns NotificationService.swift. Keep notification constants explicitly nonisolated (all values are immutable Sendable types) while implementing singular/plural notification metadata, and verify the actor-isolation diagnostics disappear.

[2026-08-15T14:40:27Z · 02b] NOTIFICATION ISOLATION CONTRACT APPLIED (uncommitted in bob-mac-capture working tree at tip 77da370): the four static metadata values on @MainActor NotificationService -- openNoteActionIdentifier, captureCategoryIdentifier, targetPathKey, foregroundPresentationOptions -- are now explicitly nonisolated so the nonisolated content/category/routing builders and UNUserNotificationCenterDelegate callbacks can read them without a main-actor hop (previously implicit-MainActor warnings that become Swift 6 errors). No singular/plural categories, action identifiers, or array user-info key existed yet in this tree to extend -- apply the same nonisolated-immutable-Sendable rule to any new equivalent metadata this phase adds. Also removed the now-unneeded @MainActor annotations from 8 NotificationServiceTests methods (successContent/failureContent/restartFailureContent/testContent/foregroundPresentationOptions/captureCategory/targetURL x2) so they exercise these members from genuinely nonisolated test contexts, pinning the contract. Implemented from a Linux sandbox (no AppKit/UserNotifications available: swift build --target BobMacCapture fails with 'no such module AppKit'), so just build/test have NOT been run yet -- needs macOS 26 + Xcode 26 validation before this is considered done.

[2026-08-15T15:14:09Z · bob-cli-t.3] Implemented normalized multi-capture success decoding plus richer single/batch notification presentation, singular/plural categories, ordered de-duplicated target routing, Command-Return multi-target opening, README contract, and focused tests. Verified swift build --target CaptureCore passes. Attempted just format-lint, just build, just test, just bundle, and direct swift test; mac app validation is blocked on this host because no Xcode/CommandLineTools/xcode-select are installed and Linux Swift cannot import AppKit/UserNotifications.

[2026-08-15T15:14:57Z · bob-cli-t.3] Verified swift build --target CaptureCore passes; macOS app validation commands were attempted but blocked on this host by missing Xcode/CommandLineTools/xcode-select and Linux Swift cannot import AppKit/UserNotifications.

## Dependencies

- **Depends on:** [bob-cli-t.2](bob-cli-t.2.md) ✓ · ⧖ 2026-08-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-t.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.3/README.md) | [bob-cli-t.3](bob-cli-t.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c95ba0e`](https://github.com/bobs-org/bob-mac-capture/commit/c95ba0e34b4a63b8c5223f02a2d9983b8253c0ae) | feat: polish batch capture notifications | [bob-cli-t.3](bob-cli-t.3.md) | 2026-08-15 11:18:13 EDT |
