# Bead: bob-cli-mj.2 — bob-plugins: the VideoZoomModal player

[Bead Pages](../README.md) / [bob-cli-mj](README.md) / bob-cli-mj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.63.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.63.linker.w0.md) · **Assignee:** `bob-cli-mj.2` · **Size:** medium
**Created:** 2026-11-16 17:31:30 EST · **Closed:** 2026-11-16 17:55:54 EST
**Plan:** [202611/video\_attachments\_z\_player.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/video_attachments_z_player.md)

## Description

plugin-video-viewer: add behavior-preserving media hooks to ImageZoomModal and build VideoZoomModal on them (start policy, Space/click play, arrow seeks, readout, zoom/pan, o/y/r, in-place failure card, full decoder teardown) with pure helpers and Node-harness tests; not yet wired to Z.

## Notes

[2026-11-16T22:55:39Z · bob-cli-mj.2] PROPOSED FOLLOW-UP: bob-plugins npm test still has 14 pre-existing failures on origin/master (11 deterministic + 3 wall-clock flakes) — bank Setup card (bob-cli-mf.4), walkMode v4 pins (bob-cli-md), block-marks date guard (bob-cli-m8), keep-moving / off-clock-link-chips / dependencies-stage perf (bob-cli-ki / bob-cli-ju), plus bracket-mode-indicator, highlights-hints, and priority-notice hex; this phase’s image+video zoom suites are 125/125 green and the 14 failures reproduce on a clean stash of this work.

[2026-11-16T22:55:54Z · bob-cli-mj.2] Verified plugin-video-viewer: ImageZoomModal media hooks, VideoZoomModal (start policy, Space/click play, arrow seeks, readout, zoom/pan, o/y/r, in-place failure card, decoder teardown) plus CSS and Node harness. npm run build; 125/125 image+origin+video zoom tests; npm run docs:check; bob plugins sync deployed bob-navigation-hotkeys. Z dispatch left to bob-cli-mj.4. No --epic-symbol leftovers. Pre-existing 14 npm test failures recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-mj.4](bob-cli-mj.4.md) ◐ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mj.2/README.md) | [bob-cli-mj.2](bob-cli-mj.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mj.2][1] | Need the phase scope, notes, and design file before closing | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mj.2/README.md

<!-- sase:referenced-by:end -->
