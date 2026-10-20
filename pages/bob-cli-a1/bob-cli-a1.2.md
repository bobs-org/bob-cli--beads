# Bead: bob-cli-a1.2 — Owned ImageZoomModal viewer

[Bead Pages](../README.md) / [bob-cli-a1](README.md) / bob-cli-a1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.26.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.26.linker.w0.md) · **Assignee:** `bob-cli-a1.2` · **Size:** medium
**Created:** 2026-10-20 09:07:41 EDT · **Closed:** 2026-10-20 09:27:32 EDT
**Plan:** [202610/z\_image\_zoom.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/z_image_zoom.md)

## Description

viewer: add a public-API Modal fragment plus CSS that opens an image fitted to the window with bounded zoom, device-pixel 1:1, keyboard/drag/wheel pan and zoom, backdrop and key close, a guarded opening keystroke, and full listener cleanup, with geometry, key-map, and lifecycle tests.

## Notes

[2026-10-20T13:27:06Z · bob-cli-a1.2] PROPOSED FOLLOW-UP: Add decisions record that Z opens a read-only owned image viewer and native mouse paths stay native (image_zoom_record skipped per epic decision no)

[2026-10-20T13:27:12Z · bob-cli-a1.2] PROPOSED FOLLOW-UP: Pre-existing bob-plugins npm test failures reproduce on clean base — unblocked-glyph x4 (bob-cli-6v), Keep counts once (bob-cli-6w), forward conversion Depends-On (bob-cli-7i); plus flaky 16ms stage-ranker (bob-cli-3w)

[2026-10-20T13:27:32Z · bob-cli-a1.2] Added ImageZoomModal (src/207-image-zoom-modal.js) plus CSS and 47 geometry/key/lifecycle tests; npm run build, validate, git diff --check pass; 60/60 target+viewer tests pass after rebase onto a1.1; scoped bob plugins sync copied main.js and styles.css; 6 clean-base npm test failures (6v/6w/7i) plus flaky 3w recorded as follow-ups; skipped image_zoom_record per epic decision

## Dependencies

- **Blocks:** [bob-cli-a1.3](bob-cli-a1.3.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a1.2/README.md) | [bob-cli-a1.2](bob-cli-a1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5e21b03`](https://github.com/bobs-org/bob-plugins/commit/5e21b03cb5152b3407da61e44111e0568cb3405e) | feat(navigation-hotkeys): add owned ImageZoomModal viewer for Z zoom | [bob-cli-a1.2](bob-cli-a1.2.md) | 2026-10-20 09:29:09 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a1.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a1.2/README.md

<!-- sase:referenced-by:end -->
