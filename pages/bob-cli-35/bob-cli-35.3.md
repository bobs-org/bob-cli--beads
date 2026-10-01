# Bead: bob-cli-35.3 — Reader print template and renderer

[Bead Pages](../README.md) / [bob-cli-35](README.md) / bob-cli-35.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3s.md) · **Assignee:** `bob-cli-35.3` · **Size:** medium
**Created:** 2026-10-01 02:07:06 EDT · **Closed:** 2026-10-01 03:17:33 EDT
**Plan:** [202610/web\_url\_highlights\_clip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/web_url_highlights_clip.md)

## Description

reader-template: Bob-owned Chromium print template with bundled OFL fonts, masthead, Highlights-safe typography, Pillow image normalization, offline headless print with outline and n / N footers.

## Notes

[2026-10-01T07:17:19Z · bob-cli-35.3] PROPOSED FOLLOW-UP: pre-existing clippy deny (overly_complex_bool_expr) in tests/cli/capture/pomodoro_name.rs fails `just lint` identically on clean base HEAD; blocks `just all` for all beads

[2026-10-01T07:17:33Z · bob-cli-35.3] reader-template done: 9 OFL woff2 (506KB) + reader.css + real web_clip_render.py (Pillow normalize, masthead assembly, offline headless print with outline/n/N footers) registered in SUPPORT_ASSETS. Verified: just check-web-clip-adapter passes locally and on athena (browser-backed render + mutool text checks: title p1, no soft-hyphens/joiners/ligatures/hyphenation); cargo test all green; cargo fmt clean; cargo package lists new files. Live on athena: OpenAI Symphony URL ok headed-xvfb, 38pp, fidelity ok, 2/2 light-variant SVG diagrams visible, code wraps, viewed p1-5+p7; lilianweng agent post ok headless, 28pp, 13/13 img, 6/6 code, viewed p1+p3. Fixed Chromium @page cross-sheet quirk (:first suppression now emitted inline with title rule; p1 footer drops title). just lint red is pre-existing on base HEAD (recorded follow-up). Scratch PDFs: /tmp/bob-clip-reader-verify/ on athena.

## Dependencies

- **Depends on:** [bob-cli-35.2](bob-cli-35.2.md) ✓ · ⧖ 2026-10-01
- **Blocks:** [bob-cli-35.5](bob-cli-35.5.md) ◐ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-35.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-35.3/README.md) | [bob-cli-35.3](bob-cli-35.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5c6e2ad`](https://github.com/bobs-org/bob-cli/commit/5c6e2ad64a8c6535eb67930adbad9b3bf378d1c5) | feat(web-clip): add Bob-owned reader print template and renderer | [bob-cli-35.3](bob-cli-35.3.md) | 2026-10-01 03:21:17 EDT |
