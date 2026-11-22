# Bead: bob-cli-os.7 — Publisher feed discovery and proven item match

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.7` · **Size:** medium
**Created:** 2026-11-21 14:59:41 EST · **Closed:** 2026-11-21 21:05:43 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

feed_match: find the show's public RSS feed through iTunes Search, parse it safely with a capped fetch, and accept only a unique item agreeing on two of three signals.

## Notes

[2026-11-22T02:05:29Z · bob-cli-os.7] API for transcript_dossier (os.9): podcast/feed.rs find_feed_item(&EpisodeMetadata, PodcastEnrich, scratch, deadline: Instant, progress) -> FeedOutcome {Matched(FeedItem), NoFeed(reason), NoMatch(reason; ties start "ambiguous:"), DeadlineExceeded, Off}. Off makes no request; DeadlineExceeded maps to "feed lookup stopped after 45 s". FeedItem: feed_url/feed_host (post-redirect), guid, title, pub_date, duration_secs (drift guard), notes_html (content:encoded else description, invisibles stripped), transcripts [{url,mime,language,rel}], chapters Option<FeedChaptersLink{url,mime}>, matched_on + matched_on_label() ("title, date" for the dry-run line). fetch_feed_chapters(&link, scratch, deadline, progress) -> ChaptersOutcome {Chapters(Vec<notes::Chapter>), Ignored(reason), DeadlineExceeded}; parse_chapters_json is pure. fetch.rs gained fetch_url_before(url, dest, max_time, max_bytes, deadline, progress) + deadline_spent(deadline) — use them for the 10 MiB transcript download so one 45 s budget covers feed + transcript. Config: HighlightsConfig::podcast_enrich() parses highlights.podcasts.enrich auto|off (default auto); its docs (configuration.md + highlights-create.md) are still owed by transcript_dossier per the plan. Test seam: podcast::test_support::FakeSpotify now has serve_url(exact URL) and an itunes surface.

[2026-11-22T02:05:43Z · bob-cli-os.7] podcast/feed.rs: iTunes Search -> up to 3 ranked public RSS feeds (25 MiB/30 s capped, roxmltree with DTDs refused) -> unique item agreeing on 2 of title/date(36 h)/duration(max 5 s, 2 %); fails open with NoFeed/NoMatch/DeadlineExceeded/Off. Podcasting 2.0 chapters JSON fetch+parse; highlights.podcasts.enrich auto|off in config/mod.rs; deadline-aware fetch_url_before in fetch.rs. Real trimmed Pragmatic Engineer iTunes result + feed fixtures (matches episode 4UgVFWty2I8hGAgSvT7pjC on all three signals). 23 feed tests cover 0/1/several candidates, 404-then-second feed, ranking, tie, DAI drift, over-cap, malformed XML, DTD refusal, private feed URL, enrich off (no requests in fake curl log), spent deadline. just check: fmt + clippy clean; cargo test --workspace 12450 passed, 0 failed.

## Dependencies

- **Depends on:** [bob-cli-os.3](bob-cli-os.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-os.9](bob-cli-os.9.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.7/README.md) | [bob-cli-os.7](bob-cli-os.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0c60af4`](https://github.com/bobs-org/bob-cli/commit/0c60af4549c0ef621a815fb2594fc164276a16e0) | feat(ref): find the publisher feed item that proves a Spotify episode | [bob-cli-os.7](bob-cli-os.7.md) | 2026-11-21 21:07:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-os.3][1] | check whether dependent phases are concurrently touching podcast module | 1 |
| read-by | [agent:bob-cli-os.7][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.7/README.md

<!-- sase:referenced-by:end -->
