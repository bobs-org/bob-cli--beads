# Bead: bob-cli-35.5 — Live OpenAI capture verification and docs finish

[Bead Pages](../README.md) / [bob-cli-35](README.md) / bob-cli-35.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3s.md) · **Assignee:** `bob-cli-35.5` · **Size:** medium
**Created:** 2026-10-01 02:07:06 EDT · **Closed:** 2026-10-01 04:03:00 EDT
**Plan:** [202610/web\_url\_highlights\_clip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/web_url_highlights_clip.md)

## Description

live-verify: build bob, capture the OpenAI Symphony URL on athena into a scratch vault and then the real intake queue, inspect pages and text layer, prove scan writes the ref note, confirm apollo fails closed, fix issues, record follow-ups.

## Notes

[2026-10-01T07:57:03Z · bob-cli-35.5] PROPOSED FOLLOW-UP: Manual Mac Highlights acceptance — highlight ~10 passages across line breaks, links, inline code, captions, compare sidecar vs ref-note quotes; only if broken, swap render stage for Defuddle-Markdown plus pandoc path

[2026-10-01T07:57:10Z · bob-cli-35.5] PROPOSED FOLLOW-UP: Install updated bob on athena, apollo, and Mac after landing

[2026-10-01T07:57:17Z · bob-cli-35.5] PROPOSED FOLLOW-UP: Add --from-chrome Mac capture and Bob Mac Capture or Shortcuts entry point spawning bob highlights clip

[2026-10-01T07:57:25Z · bob-cli-35.5] PROPOSED FOLLOW-UP: Add --mode page, image rescue for dropped figures, and --keep-source DIR

[2026-10-01T07:57:32Z · bob-cli-35.5] PROPOSED FOLLOW-UP: Design recapture and versioning for already-captured URLs

[2026-10-01T07:59:59Z · bob-cli-35.5] PROPOSED FOLLOW-UP: just all lint is red on clean base — clippy::overly_complex_bool_expr deny in tests/cli/capture/pomodoro_name.rs:808 (unrelated capture test, predates this epic); see task bead bob-cli-v

[2026-10-01T08:03:00Z · bob-cli-35.5] Live gate done 2026-10-01: athena Chrome154/Xvfb captured OpenAI Symphony (38p, 2/2 img light SVG viewed, 1/1 code, 8912w, 483KB, text layer clean), scratch scan wrote ref note + 2nd scan no-op, real intake drained by Mac bob_xlib_pull with ref note synced to athena/apollo, Lilian Weng static check headless 28p 13/13 img; cargo test + check-web-clip-adapter pass, fmt pass; just lint red identically on clean base (pomodoro_name.rs:808, follow-up noted, tracks bob-cli-v); apollo has bundled Chromium151 and captured headed via forwarded DISPLAY (stray xlib PDF deleted), docs corrected + Verified section added; docs/highlights-clip.md only tree change

## Dependencies

- **Depends on:** [bob-cli-35.3](bob-cli-35.3.md) ✓ · ⧖ 2026-10-01
- **Depends on:** [bob-cli-35.4](bob-cli-35.4.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-35.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-35.5/README.md) | [bob-cli-35.5](bob-cli-35.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a35b255`](https://github.com/bobs-org/bob-cli/commit/a35b255e872f4fa2cbe8d831644a7a64f68d0611) | docs(web-clip): record live-verify gate for bob highlights clip | [bob-cli-35.5](bob-cli-35.5.md) | 2026-10-01 04:05:33 EDT |
