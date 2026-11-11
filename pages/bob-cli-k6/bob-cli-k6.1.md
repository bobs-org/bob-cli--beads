# Bead: bob-cli-k6.1 — Always-on SVG image guard

[Bead Pages](../README.md) / [bob-cli-k6](README.md) / bob-cli-k6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.d9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.d9.md) · **Assignee:** `bob-cli-k6.1` · **Size:** medium
**Created:** 2026-11-11 07:53:18 EST · **Closed:** 2026-11-11 08:37:56 EST
**Plan:** [202611/ref\_create\_svg\_images.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_create_svg_images.md)

## Description

svg-image-guard: add an always-on Lua image filter that swaps SVG embeds for a same-stem sibling raster or an Image-not-printable placeholder, reports them as images:/warning: lines, fixes the misleading svg.sty hint, and documents the behavior.

## Notes

[2026-11-11T13:37:50Z · bob-cli-k6.1] PROPOSED FOLLOW-UP: Clean-base just docs-check still fails on five over-budget mounted pages: capture-panel, capture-previews, keyboard, and bob-navigation-hotkeys are tracked by bob-cli-jz; protocol.md is tracked by bob-cli-h9. Clean HEAD and this checkout reproduce identical counts (6036, 6177, 6060, 6186, and 6149 words; cap 6000).

[2026-11-11T13:37:56Z · bob-cli-k6.1] Implemented and verified the SVG image guard, warnings, report, renderer hint, and docs. Focused tests passed; just check passed. PDF-render integration cases skipped because the required XeLaTeX/Poppler toolchain is unavailable. just docs-check reproduces the same known clean-base word-budget failures tracked by bob-cli-jz and bob-cli-h9.

## Dependencies

- **Blocks:** [bob-cli-k6.2](bob-cli-k6.2.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-k6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-k6.1/README.md) | [bob-cli-k6.1](bob-cli-k6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`52f0d61`](https://github.com/bobs-org/bob-cli/commit/52f0d615b779fd66018888923ed8f8108761ef72) | feat(highlights): guard SVG images in PDF renders | [bob-cli-k6.1](bob-cli-k6.1.md) | 2026-11-11 08:39:05 EST |
