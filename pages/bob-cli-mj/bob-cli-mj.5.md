# Bead: bob-cli-mj.5 — bob-mac-capture: videos in the clip card

[Bead Pages](../README.md) / [bob-cli-mj](README.md) / bob-cli-mj.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.63.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.63.linker.w0.md) · **Assignee:** `bob-cli-mj.5` · **Size:** medium
**Created:** 2026-11-16 17:31:31 EST · **Closed:** 2026-11-16 19:57:20 EST
**Plan:** [202611/video\_attachments\_z\_player.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/video_attachments_z_player.md)

## Description

mac-video-card: count videos in the clip header, show size_bytes, and render a cancellable, cached AVFoundation poster with a play glyph and duration badge for video rows, staying a thin client of bob's kind; green exact-SHA macOS CI.

## Notes

[2026-11-17T00:25:29Z · bob-cli-mj.5] PROPOSED FOLLOW-UP: just docs-check failed on generated drift docs/reference/glossary.md in cached bob-cli master a57fdba (docs(memory): add bank closing glossary) — lint of capture-previews.md passed (5949 words); this glossary drift is in bob-cli, not this phase’s clip-card docs, and is independent of the mac-video-card tree

[2026-11-17T00:57:20Z · bob-cli-mj.5--1] Clip card counts videos, shows size_bytes, leftover attachment_large warnings, and AVFoundation poster/duration; portable-check 2551 tests green; macos-ci-check exact-SHA green; Mac scratch typecheck unverified (Mac offline); docs-check glossary drift on bob-cli master recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-mj.1](bob-cli-mj.1.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mj.5.md) | [bob-cli-mj.5](bob-cli-mj.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@2c40f68`](https://github.com/bobs-org/bob-mac-capture/commit/2c40f68df3a1ff3a6207f1687f43d80d7841c7f8) | feat(capture): show video posters and sizes in the clip card | [bob-cli-mj.5](bob-cli-mj.5.md) | 2026-11-16 19:59:17 EST |
