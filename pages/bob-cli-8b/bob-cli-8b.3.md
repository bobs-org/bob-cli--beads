# Bead: bob-cli-8b.3 — Bob Mac Capture saved-template models, client, and fixtures

[Bead Pages](../README.md) / [bob-cli-8b](README.md) / bob-cli-8b.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1n.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1n.linker.w0.md) · **Assignee:** `bob-cli-8b.3` · **Size:** medium
**Created:** 2026-10-16 08:18:36 EDT · **Closed:** 2026-10-16 10:20:13 EDT
**Plan:** [202610/saved\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/saved_capture_templates.md)

## Description

mac-core: decode the shelf protocol in CaptureCore, add BobProcessClient list/save/delete/clear plus an identity-gated --template-origin, shared picker helpers, the row presentation builder, the environment-key fix, recorded fixtures, and fake-bob routes.

## Notes

[2026-10-16T13:30:42Z · bob-cli-8b.3] PROPOSED FOLLOW-UP: Add decisions:saved-templates-are-checked-out — memory_saved_templates_decision was skipped by the epic decision.

[2026-10-16T13:30:48Z · bob-cli-8b.3] PROPOSED FOLLOW-UP: Add glossary:saved-template (alias template shelf) — memory_saved_template_glossary was skipped by the epic decision.

[2026-10-16T14:20:13Z · bob-cli-8b.3--7] Verified Athena just portable-check (monitor hntxzndn44ks, 1254 tests, 0 failures) and Mac scratch ./Scripts/bundle.sh && just typecheck-tests (PASS BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, RefsCoreTests). Removed Athena /tmp/bob-mac-capture-portable-bob-cli-8b3-1332 and Mac /tmp/bob-mac-capture-scratch-bob-cli-8b3-1332. typecheck-tests is stub-only; CI still runs XCTest. Linux CI cannot type-check Sources/BobMacCapture* or Tests/BobMacCapture*.

## Dependencies

- **Depends on:** [bob-cli-8b.2](bob-cli-8b.2.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8b.4](bob-cli-8b.4.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8b.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8b.3.md) | [bob-cli-8b.3](bob-cli-8b.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@cb4c01e`](https://github.com/bobs-org/bob-mac-capture/commit/cb4c01e0dd40165959a8bb39111d68248a44cfac) | feat(mac-capture): add saved-template protocol client and models | [bob-cli-8b.3](bob-cli-8b.3.md) | 2026-10-16 10:21:28 EDT |
