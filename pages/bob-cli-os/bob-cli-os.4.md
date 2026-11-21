# Bead: bob-cli-os.4 — Adapter render op and the episode dossier template

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.4` · **Size:** medium
**Created:** 2026-11-21 14:59:41 EST · **Closed:** 2026-11-21 17:25:03 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

dossier_render: add the offline adapter `render` op and the podcast-episode dossier layout, CSS, and source view, plus the Rust client method and fake-adapter support.

## Notes

[2026-11-21T22:24:27Z · bob-cli-os.4] PROPOSED FOLLOW-UP: just docs-check fails on the clean base — docs/reference/plugins/bob-navigation-hotkeys.md is over its word budget (6307 > 6000 for reference/); reproduces identically without this phase and is already recorded in bob-cli-om notes.

[2026-11-21T22:24:40Z · bob-cli-os.4] PROPOSED FOLLOW-UP: Chrome PDF bookmarks drop the space at a wrapped h1 line break — the dossier outline reads "Software factories and codereviews with Harjot Gill"; the same masthead-title h1 likely affects every wrapped web article title, so investigate a renderer-side fix (e.g. an explicit outline title) rather than a podcast-only patch.

[2026-11-21T22:24:48Z · bob-cli-os.4] HANDOFF for episode_route: call ClipAdapterClient::render(&RenderRequest::new(article_json, workdir, out_pdf, tables)) -> RenderSuccess (alias of ComposeSuccess, so the compose store helpers apply). Write article.json per the plan contract with the cover at assets/<file> next to it; render/ (source.html, code-anchors.json) goes under workdir. Payload errors come back as invalid_request. The Shared-at pill shows only for 0 < shared_at_secs and shared_at_secs*1000 < duration_ms. Fake adapter: FakeClip answers "op":"render" (respond_render / render_called / default_render). Visual-check artifacts: file:explicit:f961c2af21dfd931a580d332, file:explicit:832796f116d9189089f4d580, file:explicit:65e025fca761902b2c5e4b4f, file:explicit:f1abd845ad8347e2a9224d7b.

[2026-11-21T22:25:03Z · bob-cli-os.4] Adapter render op (protocol 1, offline, invalid_request payload errors) plus the podcast_episode dossier branch in web_clip_render (shared nh3 sanitize_html with images and empty anchors dropped, cover card, pills, chapters with optional ?t= links, sponsors card, provenance footer, lang, source view with plain chapter list) and reader.css styles. Rust ClipAdapterClient::render + RenderRequest/RenderSuccess with unit tests that drive a /bin/sh adapter; FakeClip answers op render with a direct test; docs/highlights-clip.md documents the op. Verified: just check green (7663 lib + 3926 cli tests, fmt, clippy); just check-web-clip-adapter green including the new pure checks and a browser-backed op_render run; visual check of the real-episode fixture rasterized with mutool draw -r 110 (2 pages, bookmarks Title > Show notes > Chapters) plus a bare-card variant, stored as artifacts. just docs-check fails only on the pre-existing bob-navigation-hotkeys.md budget (identical on clean base; follow-up noted).

## Dependencies

- **Depends on:** [bob-cli-os.1](bob-cli-os.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-os.5](bob-cli-os.5.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.4/README.md) | [bob-cli-os.4](bob-cli-os.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6b9139a`](https://github.com/bobs-org/bob-cli/commit/6b9139a65dc2780e839ecff3c2782a2ffcda0f61) | feat(ref): add the offline adapter render op and the podcast episode dossier | [bob-cli-os.4](bob-cli-os.4.md) | 2026-11-21 17:26:19 EST |
