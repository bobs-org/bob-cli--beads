# Bead: bob-cli-a1.1 — Line-scoped image target resolver

[Bead Pages](../README.md) / [bob-cli-a1](README.md) / bob-cli-a1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.26.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.26.linker.w0.md) · **Assignee:** `bob-cli-a1.1` · **Size:** medium
**Created:** 2026-10-20 09:07:41 EDT · **Closed:** 2026-10-20 09:19:48 EDT
**Plan:** [202610/z\_image\_zoom.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/z_image_zoom.md)

## Description

target: add the bob-navigation-hotkeys image-zoom mixin fragment that finds embed, wikilink, and Markdown image references on the live cursor line, skips inline and fenced code, picks one by the containing/next/previous rule, and resolves it against the source note to a resource URL or an exact notice, with fixture tests.

## Notes

[2026-10-20T13:19:34Z · bob-cli-a1.1] PROPOSED FOLLOW-UP: Add decisions record that Z opens a read-only owned image viewer and native mouse paths stay native (image_zoom_record skipped per epic decision no)

[2026-10-20T13:19:40Z · bob-cli-a1.1] PROPOSED FOLLOW-UP: Pre-existing bob-plugins failures reproduce on clean base (6 stable: ledger-tools-unblocked-glyph x4, decision-card keeps, forward-promotion Depends-On; plus flaky 16ms stage-ranker perf) — unrelated to image-zoom target phase, full suite 3224/3231 pass

[2026-10-20T13:19:48Z · bob-cli-a1.1] Added 679-plugin-image-zoom mixin (findInlineCodeSpans, findImageZoomRefs, isImageZoomCandidate, pickImageZoomRef, resolveImageZoomTargetOnLine) with 13 fixture tests passing; npm run build, validate, docs:check, git diff --check pass; bob plugins sync scoped dry-run+real pass; 6 pre-existing failures reproduce on base plus 1 perf flake recorded as follow-ups

## Dependencies

- **Blocks:** [bob-cli-a1.3](bob-cli-a1.3.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a1.1/README.md) | [bob-cli-a1.1](bob-cli-a1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7c6d037`](https://github.com/bobs-org/bob-plugins/commit/7c6d03799c2e206f95a77fe704d9f18061fa9899) | feat(navigation-hotkeys): add line-scoped image target resolver for Z zoom | [bob-cli-a1.1](bob-cli-a1.1.md) | 2026-10-20 09:20:39 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a1.1][1] | Need the phase scope and design file | 4 |
| read-by | [agent:bob-cli-a1.2][2] | See how target phase recorded the skipped memory follow-up | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a1.2/README.md

<!-- sase:referenced-by:end -->
