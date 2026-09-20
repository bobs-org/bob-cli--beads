# Bead: bob-cli-25.5 — Bob Mac Capture frontend support

[Bead Pages](../README.md) / [bob-cli-25](README.md) / bob-cli-25.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.1a](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.apollo.1a.md) · **Assignee:** `bob-cli-25.5` · **Size:** small
**Created:** 2026-09-20 18:07:13 EDT · **Closed:** 2026-09-20 19:04:35 EDT
**Plan:** [202609/capture\_project\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_project_notes.md)

## Description

mac: teach the macOS capture panel the new span kind and capture kind so the `+` sigil is highlighted and project-note results are labeled correctly.

## Notes

[2026-09-20T23:04:35Z · bob-cli-25.5] Mac frontend handles project-note captures: project_note_marker maps to .explicitToggle (CompletionRowContent.swift) and friendlyKindLabel returns Project for project_note/project-note (NotificationService.swift); coverage tests added in CaptureCoreTests and BobMacCaptureTests. Verified live against bob build: capture-parse reports mode project_note with project_note_marker span, and --dry-run JSON reports kind project_note with route_label cash_goog_exit.md. completionSpanKinds/routeSpanKinds already cover the unchanged route/block spans; Swift suite not runnable here (no macOS toolchain).

## Dependencies

- **Depends on:** [bob-cli-25.1](bob-cli-25.1.md) ✓ · ⧖ 2026-09-20
- **Depends on:** [bob-cli-25.3](bob-cli-25.3.md) ✓ · ⧖ 2026-09-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-25.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-25.5/README.md) | [bob-cli-25.5](bob-cli-25.5.md) | 0 |
