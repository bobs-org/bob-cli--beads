# Bead: bob-cli-q5.9.1.4 — Add an acceptance-only in-app probe and evidence-grade signposts

[Bead Pages](../README.md) / [bob-cli-q5.9.1](bob-cli-q5.9.1.md) / bob-cli-q5.9.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hl.md) · **Assignee:** `bob-cli-q5.9.1.4` · **Size:** medium
**Created:** 2026-11-27 20:55:08 EST · **Closed:** 2026-11-27 22:18:55 EST
**Plan:** [202611/finish\_snoozed\_tasks\_unattended.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_snoozed_tasks_unattended.md)

## Description

mac-probe: build a probe that only the acceptance bundle can enable and that reads and drives the live wake HUD, beacon, and records. Add wake-ID and reason metadata to snooze signposts, the missing HUD tests, and harness subcommands, including the passive lock watcher.

## Notes

[2026-11-28T02:49:47Z · bob-cli-q5.9.1.4] Mac scratch bundle.sh --identity - and just typecheck-tests passed on mac after HUD AX walk compile fix (NSView/NSWindow/NSAccessibilityElement) and XCTest stub accuracy/throws typecheck fixes. Staging Scripts/macos-ci-check next.

[2026-11-28T03:18:55Z · bob-cli-q5.9.1.4--1] Acceptance-only snooze wake probe landed in bob-mac-capture. Verified: Mac scratch bundle.sh --identity - and just typecheck-tests on mac after HUD AX walk compile fix; just portable-check, just check-scripts, and just docs-check; exact-SHA macos-ci-check exit 0 for snapshot e446a97f01b96760c43c2c63399f79fd6408598f (GitHub Actions run 46100086357, macOS 26 SwiftPM: scripts, format, build, test, bundle, plist/signature, launch smoke, install/reinstall). Probe enables only for org.bobs.bob-mac-capture.accept* with snoozeAcceptanceProbe=true. Production Mac Capture, production defaults, ~/bob, and Bryan checkouts untouched.

## Dependencies

- **Blocks:** [bob-cli-q5.9.1.5](bob-cli-q5.9.1.5.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.9.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.9.1.4.md) | [bob-cli-q5.9.1.4](bob-cli-q5.9.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@8450659`](https://github.com/bobs-org/bob-mac-capture/commit/84506599514cff20f0351ae5d31b6f8938bea04b) | feat(mac-capture): add acceptance-only snooze wake probe | [bob-cli-q5.9.1.4](bob-cli-q5.9.1.4.md) | 2026-11-27 22:20:17 EST |
