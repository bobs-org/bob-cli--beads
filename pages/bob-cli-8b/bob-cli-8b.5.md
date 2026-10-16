# Bead: bob-cli-8b.5 — Template checkout lifecycle, Command-S save, Settings, and docs

[Bead Pages](../README.md) / [bob-cli-8b](README.md) / bob-cli-8b.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1n.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1n.linker.w0.md) · **Assignee:** `bob-cli-8b.5` · **Size:** medium
**Created:** 2026-10-16 08:18:36 EDT · **Closed:** 2026-10-16 11:24:32 EDT
**Plan:** [202610/saved\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/saved_capture_templates.md)

## Description

mac-checkout: track the checked-out origin, release it on every abandon path, pass --template-origin on submit, announce save outcomes, add Command-S Save template, the Settings section, README docs, and the memory decisions.

## Notes

[2026-10-16T15:16:58Z · bob-cli-8b.5] PROPOSED FOLLOW-UP: Add the saved-templates-are-checked-out decision record describing bob-owned shelf storage and replace-by-origin settlement.

[2026-10-16T15:17:07Z · bob-cli-8b.5] PROPOSED FOLLOW-UP: Add the saved-template glossary strand (alias template shelf) and link it to bulk-capture.

[2026-10-16T15:24:32Z · bob-cli-8b.5] Implemented the saved-template checkout, save/replace behavior, shelf settings and clear action, capture status feedback, and lifecycle tests/docs. Verified git diff --check, Swift syntax parsing on Athena, and just portable-check (1254 tests passed); macOS app/test targets remain unverified because the Mac host was offline. Confirmed no epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-8b.4](bob-cli-8b.4.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8b.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8b.5/README.md) | [bob-cli-8b.5](bob-cli-8b.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@6a7046e`](https://github.com/bobs-org/bob-mac-capture/commit/6a7046e226d3a995ffd06b2f6e873678e36a6cde) | feat(saved-templates): implement Mac Capture template checkout | [bob-cli-8b.5](bob-cli-8b.5.md) | 2026-10-16 11:25:25 EDT |
