# Bead: bob-cli-9v.3 — Inline images and standalone notes in the preview feed

[Bead Pages](../README.md) / [bob-cli-9v](README.md) / bob-cli-9v.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11v.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11v.w0.md) · **Assignee:** `bob-cli-9v.3` · **Size:** medium
**Created:** 2026-10-19 12:32:44 EDT · **Closed:** 2026-10-19 14:41:17 EDT
**Plan:** [202610/refs\_reading\_room.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_reading_room.md)

## Description

inspector-images: add an ImageIO-backed image loader with metadata prefetch so every image reserves its exact size before layout, render image highlights, attached images, unavailable-image rows, and standalone notes in the feed, and cover them with loader, hosted reveal, and render-fixture tests plus README updates.

## Notes

[2026-10-19T18:41:17Z · bob-cli-9v.3] Inspector images and standalone notes: ImageIO loader with metrics-before-publish prefetch, reserved-size views, unavailable rows, and standalone notes in the feed (standalone_notes=include). just portable-check green (1431 tests). Mac scratch Scripts/bundle.sh + just typecheck-tests PASS (typecheck-tests stubs XCTest; CI still runs tests). CI is not on origin yet. Restored surgical Loader/PanelView diffs after an accidental swift-format rewrite.

## Dependencies

- **Depends on:** [bob-cli-9v.1](bob-cli-9v.1.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-9v.2](bob-cli-9v.2.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9v.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9v.3/README.md) | [bob-cli-9v.3](bob-cli-9v.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@73d1106`](https://github.com/bobs-org/bob-mac-capture/commit/73d110625d60f5d2a5460a834098e5c7acdfa03d) | feat(refs): inline inspector images and standalone notes | [bob-cli-9v.3](bob-cli-9v.3.md) | 2026-10-19 14:42:40 EDT |
