# Bead: bob-cli-os.5 — The podcast route in bob ref create

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.5` · **Size:** medium
**Created:** 2026-11-21 14:59:41 EST · **Closed:** 2026-11-21 23:05:58 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

episode_route: wire Spotify episodes into create (new, dry run, reread, overwrite) as podcasts refs with title stems, honest reports, the source store, help, and docs, then smoke-test live.

## Notes

[2026-11-22T04:05:26Z · bob-cli-os.5] PROPOSED FOLLOW-UP: just docs-check fails on the clean base in tools/docs/tests/test_contracts.py (registry has 55 contracts vs the pinned 54, llms.txt order, README table hash) since a0961435 added docs/task-requirements.md — reproduces with this phase’s docs change stashed; already reported by bob-cli-on.10.1.5 and in scope for bob-cli-on.10.1.6. Every other docs-check stage (lint, generated drift, strict build, offline lychee with fragments, search, tutorial, media) passes.

[2026-11-22T04:05:42Z · bob-cli-os.5] PROPOSED FOLLOW-UP: reuse a resolved Spotify short link’s final page body in bob ref create — spotify::prepare_create_target drops the body resolve_short_link downloaded, so create fetches the episode page twice for spotify.link targets; podcast::dossier::prepare already accepts prefetched_page, so threading the body (e.g. via CreateOptions) would save one request. Ingest (bob-cli-os.6) can pass it directly.

[2026-11-22T04:05:58Z · bob-cli-os.5] episode_route landed: podcast/dossier.rs (shared builder: fetch_episode → cover → notes segmentation → podcast_episode article.json with cover in assets/ → ClipAdapterClient::render; non-printing, typed DossierError, prefetched_page hook for ingest) and create/podcast_route.rs (create_podcast_route + overwrite_podcast, dispatched in create_pdf right after arXiv; podcasts default type, title stem → spotify_episode_<lower id> fallback, id = stem, PDF Info author = show, canonical source_url/dedupe, reread/overwrite parity incl. refuse_redirected_* and staged source store, persist_article_store + finish_create_intake). Help Targets line/example/-t default, ref list -t podcasts, docs/highlights-create.md (intro, example, dry-run row, Targets row, PDF-route stamping, new ## Spotify episodes). Fixed two defects the route exposed: clip_url::strip_title_extension panicked on non-ASCII titles (char boundary) and notes.rs emitted top-level inline text unwrapped so it printed outside the notes column (now one <p>). Verified: just check exit 0 (43 test binaries, 8 new CLI tests in tests/cli/highlights/podcast_create.rs + dossier/notes/clip_url unit tests); just docs-gen clean; docs-check passes all stages except the pre-existing contract-registry tests (follow-up noted). Live smoke on a throwaway git vault with real Spotify + Playwright Chromium: dry run, create (2 pages, 16 chapters, store saved, intake committed+pushed to a local bare remote), reread __v2, and -f overwrite in place all succeeded; mutool txt shows the title once, November 18, 2026, 1 h 26 min, no 'See all episodes', untruncated notes; rasterized pages at 110 dpi match the visual spec. Album/record walkers are root-only (albums_not_at_root finding; record folders are single safe segments), so ref/podcasts/ is ignored. No epic symbols; no memory edits.

## Dependencies

- **Depends on:** [bob-cli-os.3](bob-cli-os.3.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-os.4](bob-cli-os.4.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-os.6](bob-cli-os.6.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.5/README.md) | [bob-cli-os.5](bob-cli-os.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`900772d`](https://github.com/bobs-org/bob-cli/commit/900772d9f9c9ba8746d93a116edf3970009056dd) | feat(ref): file Spotify episodes as podcasts references through the episode dossier route | [bob-cli-os.5](bob-cli-os.5.md) | 2026-11-21 23:43:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-os.3][1] | check whether dependent phases are concurrently touching podcast module | 1 |
| read-by | [agent:bob-cli-os.4][2] | Check sibling phase status since it is in progress | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.4/README.md

<!-- sase:referenced-by:end -->
