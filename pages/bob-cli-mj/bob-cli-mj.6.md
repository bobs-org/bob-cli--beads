# Bead: bob-cli-mj.6 — bob-plugins: scrubber, frame step, speed, mute, fullscreen

[Bead Pages](../README.md) / [bob-cli-mj](README.md) / bob-cli-mj.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.63.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.63.linker.w0.md) · **Assignee:** `bob-cli-mj.6` · **Size:** medium
**Created:** 2026-11-16 17:31:31 EST · **Closed:** 2026-11-16 20:43:16 EST
**Plan:** [202611/video\_attachments\_z\_player.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/video_attachments_z_player.md)

## Description

plugin-video-transport: add the hairline scrubber with hover time bubble and drag seek, frame stepping, playback speed, g/G, mute, fullscreen, and the play/pause flash to VideoZoomModal; extend the real-Obsidian e2e and docs; deploy.

## Notes

[2026-11-17T01:42:47Z · bob-cli-mj.6] PROPOSED FOLLOW-UP: docs:check glossary drift — docs/reference/glossary.md out of date on clean tree, fails npm run docs:check identically without this phase

[2026-11-17T01:42:54Z · bob-cli-mj.6] PROPOSED FOLLOW-UP: full npm test has 11 pre-existing failures (bank-setup, keep-moving-marks-surface, off-clock-link-chips, bracket-mode-indicator/repeat, highlights-hints, priority-notice, ref-pdf, period-links, block-marks e2e self-test) reproducing identically on clean tree

[2026-11-17T01:42:59Z · bob-cli-mj.6] PROPOSED FOLLOW-UP: two 25ms Live Preview perf-budget tests flake under full-suite load but pass in isolation; consider raising budget or isolating perf run

[2026-11-17T01:43:16Z · bob-cli-mj.6] Transport done and deployed: 207d-video-zoom-transport.js (scrubber with hover bubble + drag seek, frame step, 0.25-2 speed ladder, g/G, mute, fullscreen, play/pause flash) wired into VideoZoomModal; 90/90 unit tests pass; real-Obsidian e2e 13/13 pass (1 sanctioned BOB_BIN skip); docs/image-zoom.md key tables complete; bob plugins sync deployed to vault. Pre-existing docs:check glossary drift and 11 clean-tree test failures recorded as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-mj.4](bob-cli-mj.4.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mj.6/README.md) | [bob-cli-mj.6](bob-cli-mj.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b5491d3`](https://github.com/bobs-org/bob-plugins/commit/b5491d3b4f5d4a5ad1bc839cd655e2b6ba01fd77) | feat(navigation): add video transport to VideoZoomModal | [bob-cli-mj.6](bob-cli-mj.6.md) | 2026-11-16 20:44:51 EST |
