# Bead: bob-cli-os.2 — Spotify link identity, canonical dedupe, and routing guards

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.2` · **Size:** medium
**Created:** 2026-11-21 14:59:41 EST · **Closed:** 2026-11-21 16:04:12 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

spotify_identity: add the spotify.rs link grammar with canonical case-preserving identity and ?t= capture, resolve short links, gate capture/Keep admission, and refuse non-episodes, -L, -H, and collections with teaching hints.

## Notes

[2026-11-21T21:03:38Z · bob-cli-os.2] PROPOSED FOLLOW-UP: just docs-check fails on plugin reference word budgets unrelated to this phase — docs/reference/plugins/bob-ledger-tools.md (6042 > 6000) and bob-navigation-hotkeys.md (6307 > 6000) are over the reference/ cap (plus a develop/plugin-apis.md warning); this phase touches neither file, and the bank row notes epic (bob-cli-oo) recently grew bob-ledger-tools docs. Trim those pages in bob-plugins (their source repo).

[2026-11-21T21:03:49Z · bob-cli-os.2] PROPOSED FOLLOW-UP: just docs-gen regenerated docs/reference/glossary.md (Bank Row note-tail sentence) — HEAD dfe20ca3 changed the glossary memory without regenerating the page; this phase commits the regenerated page.

[2026-11-21T21:04:12Z · bob-cli-os.2] Added src/native/highlights_ref/spotify.rs (pure SpotifyLink grammar: open/play hosts, intl-*/embed/embed-podcast, spotify: URIs, 22-char case-preserved ids, ?t= shared_at, exact short-link hosts; resolve_short_link via fetch_url; teaching refusals). validate_and_clean/dedupe_key_for canonicalize every Spotify entity to https://open.spotify.com/<kind>/<id>, so legacy si/sci refs (exact stored source_url tested) dedupe with no migration; ref find classifies spotify: URIs as url queries. RouteHint::Podcast for episodes and short links; UrlRoutingPolicy::admits refuses non-episode Spotify entities and paths. create normalizes the TARGET once before preflight (URI -> canonical, short link resolved) and refuses -L, -H, non-episodes (exit 2, table messages); collection refuses Spotify links; ingest_url resolves short links before both dedupe probes and types non-episodes as permanent unsupported_content. Docs: highlights-create (Spotify section, Dedupe, -H), highlights-clip, capture, ref, ref-jobs, gkeep; create -H help. Verified: just check exit 0 (12331 passed, 0 failed); new unit tests (spotify, clip_url, url_routing, ref_library, gkeep plan, ingest) and CLI tests (tests/cli/highlights/spotify.rs, capture ref) pass; just docs-gen run; just docs-check fails only on pre-existing plugin reference word budgets (recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Blocks:** [bob-cli-os.3](bob-cli-os.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.2/README.md) | [bob-cli-os.2](bob-cli-os.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ddc9e17`](https://github.com/bobs-org/bob-cli/commit/ddc9e177548417ca4bfe0b76107e00a2d649e2b6) | feat(ref)!: give Spotify links canonical identity and refuse non-episodes | [bob-cli-os.2](bob-cli-os.2.md) | 2026-11-21 16:05:39 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-os.2][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-oz.5][2] | Identify the protected ledger bundle work before deciding on replacement | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oz.5.md

<!-- sase:referenced-by:end -->
