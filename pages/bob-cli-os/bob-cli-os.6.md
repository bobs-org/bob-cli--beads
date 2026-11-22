# Bead: bob-cli-os.6 — Capture jobs and Keep file episodes through the same route

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.6` · **Size:** medium
**Created:** 2026-11-21 14:59:41 EST · **Closed:** 2026-11-22 00:52:14 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

episode_ingest: route Spotify episodes in ingest_url through the shared dossier builder, carry ?t= from the original URL, turn %l into a hint, and type every failure.

## Notes

[2026-11-22T05:52:00Z · bob-cli-os.6] PROPOSED FOLLOW-UP: just docs-check false-positive on src/native/highlights_ref/podcast/feed.rs:70 — Podcasting 2.0 GitHub URL https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md is parsed as local /1.0; reproduces on clean HEAD 900772d9 and is outside this phase (just check does not run docs-check)

[2026-11-22T05:52:14Z · bob-cli-os.6] ingest_url routes Spotify episodes through ingest_podcast_route (podcasts, ready) with original URL so ?t= becomes shared_at_secs; capture/Keep %l is a listen_hint and jobs file without listen; typed EpisodeError kinds; jobs/gkeep/capture/%l/in_library tests pass; just check green (fmt, lint, 3983 CLI tests)

## Dependencies

- **Depends on:** [bob-cli-os.5](bob-cli-os.5.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-os.9](bob-cli-os.9.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.6/README.md) | [bob-cli-os.6](bob-cli-os.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`005f4c2`](https://github.com/bobs-org/bob-cli/commit/005f4c2b6e4e89319698d6080dfd71089ec9978d) | feat(ref): ingest Spotify episodes from capture jobs and Keep through the podcast route | [bob-cli-os.6](bob-cli-os.6.md) | 2026-11-22 00:53:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-os.10][1] | Check sibling phase status and any follow-up notes relevant to rollout | 1 |
| read-by | [agent:bob-cli-os.6][2] | Need the phase scope, design file, notes, and DECISIONS before finishing remaining tests | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.10/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.6/README.md

<!-- sase:referenced-by:end -->
