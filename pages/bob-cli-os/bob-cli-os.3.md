# Bead: bob-cli-os.3 — Episode metadata ladder and show-notes segmentation

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.3` · **Size:** medium
**Created:** 2026-11-21 14:59:41 EST · **Closed:** 2026-11-21 17:19:55 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

episode_metadata: fetch and parse browserless episode metadata (page state, JSON-LD/meta, embed, oEmbed), segment show notes into notes/chapters/sponsor blocks, and download cover art, all fixture-tested.

## Notes

[2026-11-21T22:19:55Z · bob-cli-os.3] Added src/native/highlights_ref/podcast/{mod,metadata,notes,cover}.rs (library only, module gated with cfg_attr(not(test), allow(dead_code)) until episode_route wires it) and fetch::fetch_url_capped (fetch_url unchanged: same 95 MiB messages). API for later phases: metadata::fetch_episode(&SpotifyEpisode, scratch, progress, prefetched_page: Option<&Path>) -> Result<EpisodeMetadata, EpisodeError>; EpisodeMetadata{id, canonical_url, title, show, show_uri, publisher, released{instant,precision}, duration_ms, language, cover_url, notes_html, notes_text, sources: BTreeMap<EpisodeField, MetadataSource>, warnings} with published_date() in Bob's day zone and source_of(); MetadataSource::{as_str() = spotify_page|spotify_embed|spotify_oembed, label() = 'spotify page'…}; EpisodeError::{NotFound(404), HttpStatus, Fetch, NoMetadata} with message()/hint()/retryable()/status()/render(). Design choice: a 429/5xx or transport failure on the episode page is a retryable error, never a degraded fallback; embed/oEmbed failures fail open and only surface when no tier yields a title. notes::segment_notes(html, duration_ms) / segment_text -> ShowNotes{blocks: Html|Chapters|Sponsors, words} with chapters()/sponsors_html(); a plain (non-bullet) sponsor run looks at most 8 lines ahead for its separator. cover::fetch_cover(Option<&str>, dest_dir, progress) -> CoverOutcome (cover.<jpg|png|webp> by magic bytes, 5 MiB cap, one 'cover art missing: …' warning). Fixtures: tests/fixtures/spotify/ (trimmed live page/embed/oEmbed captured 2026-11-21, embed token and audio URLs removed, plus 4 drift pages) and tests/fixtures/podcast/pragmatic_engineer_notes.html. Verified: 42 unit tests (ladder order, id-mismatch rejection, JSON-LD array, oEmbed-only, 404, 429/503/timeout retryable, 5 MiB cap, U+2060 stripping, 02:00Z -> previous NY day via BOB_CONFIG_FILE timezone, 16 chapters 0:00..1:24:30 with Timestamps consumed, sponsor run demoted at the em-dash, unterminated sponsor stays, non-increasing times rejected, cover magic bytes/404/non-image/private host/cap); just check exit 0 (fmt, clippy gate, all 43 test binaries); epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-os.2](bob-cli-os.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-os.5](bob-cli-os.5.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-os.7](bob-cli-os.7.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-os.8](bob-cli-os.8.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.3/README.md) | [bob-cli-os.3](bob-cli-os.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2837fea`](https://github.com/bobs-org/bob-cli/commit/2837fea8003ddc4f5d77e730b15a7319ed7fb3ab) | feat(ref): add the Spotify episode metadata ladder and show-notes segmentation | [bob-cli-os.3](bob-cli-os.3.md) | 2026-11-21 17:21:13 EST |
