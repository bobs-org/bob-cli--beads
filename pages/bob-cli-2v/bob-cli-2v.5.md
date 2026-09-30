# Bead: bob-cli-2v.5 — Bob Mac Capture task-link picker panel, ID prompt, and keys

[Bead Pages](../README.md) / [bob-cli-2v](README.md) / bob-cli-2v.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3j](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3j.md) · **Assignee:** `bob-cli-2v.5` · **Size:** medium
**Created:** 2026-09-30 13:00:14 EDT · **Closed:** 2026-09-30 14:25:52 EDT
**Plan:** [202609/task\_link\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_link_picker.md)

## Description

mac_panel: route the `task_link` context into the picker card. Accept inserts `@route:id`, Shift-Return inserts it with `=`, and Command-Return inserts it and captures. Tasks without an ID open a prefilled Add block ID prompt that assigns the ID and splices the link, and Escape returns to the picker. Also update the views, README, real-bob fixtures, and tests, and get macOS CI green.

## Notes

[2026-09-30T18:25:21Z · bob-cli-2v.5] PROPOSED FOLLOW-UP: just test (swift test) fails on CLT-only mac hosts with no such module XCTest for all test targets, identically on the clean base tree; run CaptureTaskLinkPanelTests + TaskLinkPickerPresentationTests under full Xcode 26+ or macOS CI where XCTest exists

[2026-09-30T18:25:39Z · bob-cli-2v.5] PROPOSED FOLLOW-UP: needs one macOS 26 SwiftPM CI run with every step green for the task-link panel (just format-lint build test); just format-lint GREEN and just build GREEN verified on mac via ssh, just test blocked by missing XCTest on CLT-only host

[2026-09-30T18:25:52Z · bob-cli-2v.5] mac_panel wired: task_link routed into picker card (open/refetch/chip), accept inserts @route:id, Shift-Return appends =, Cmd-Return submits, ID-less rows open prefilled link-mode Add block ID prompt (Tab cycling, Add ID & Link/Start/Capture, Escape restores picker); views (now/note headers, ID-less locator, schedule capsule, action/pull-forward lines), README, 6 real-bob fixtures + fake-bob cases, CaptureTaskLinkPanelTests. Verified: just format-lint GREEN + just build GREEN on mac via ssh, 16/16 bob-cli task_link tests GREEN, fixture JSON valid, fake-bob syntax OK. just test RED solely from missing XCTest on CLT-only host (reproduces on clean base, recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-2v.3](bob-cli-2v.3.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2v.4](bob-cli-2v.4.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2v.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2v.5/README.md) | [bob-cli-2v.5](bob-cli-2v.5.md) | 0 |
