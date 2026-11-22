# Bead: bob-cli-os — Spotify episodes become first-class podcast references

[Bead Pages](../README.md) / bob-cli-os

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.land`
**Created:** 2026-11-21 14:59:41 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/spotify_episode_refs.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md

<!-- sase:links:end -->

## Description

Every Spotify episode link given to `bob ref create`, capture, or Keep becomes one deduplicated `podcasts` reference. Its PDF is an episode dossier: cover, show, date, duration, clickable chapters, full show notes, and a highlightable transcript when the publisher's own feed proves the match. Every other Spotify link is refused, or is kept as an ordinary item, with a hint that says what to do instead. No Spotify link reaches the article engine again.

## Notes

[2026-11-22T03:01:37Z · bob-cli-on.6.1.land] DISCOVERED ISSUE (found by the bob-cli-on.6.1 land agent while running just docs-check on master 3ce97d73): the published-URLs gate fails with 'urls: 1 broken URL obligation(s): src/native/highlights_ref/podcast/feed.rs:70: docs/1.0.md -> /1.0/: no built page for /1.0'. The obligation comes from the PODCAST_NAMESPACES constant added in 0c60af45 (bob-cli-os.7, feat(ref): find the publisher feed item that proves a Spotify episode): the third namespace spelling 'https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md' contains a 'docs/…md' path that bob-docs' URL scanner reads as a reference to a bob docs page. Repro: just docs-check (stops at 'published URLs', exit 1); lint, generated drift, and the strict build pass. Fix in that phase's area: exempt the line or split the literal so the scanner does not treat it as a docs link.

[2026-11-22T03:18:31Z · bob-cli-on.10.1.land] DISCOVERED ISSUE (corroboration): bob-cli-on.10.1.4 (note #1) and bob-cli-on.10.1.6 (note #1) each hit the published-URLs docs-check failure this epic's notes already record (src/native/highlights_ref/podcast/feed.rs:70: the Podcastindex namespace string ending docs/1.0.md maps to /1.0/ with no built page) while running npm run docs:check / just docs-check for unrelated work, and confirmed it fails identically on a clean tree; bob-cli master has not changed feed.rs since (e5ee4a8d).

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-os.1](bob-cli-os.1.md) | General capture fixes the audit exposed | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-os.10](bob-cli-os.10.md) | Podcast surfaces across repos and the legacy refs | ✓ closed | small | 2026-11-21 | 1 | 1 |
| [bob-cli-os.2](bob-cli-os.2.md) | Spotify link identity, canonical dedupe, and routing guards | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-os.3](bob-cli-os.3.md) | Episode metadata ladder and show-notes segmentation | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-os.4](bob-cli-os.4.md) | Adapter render op and the episode dossier template | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-os.5](bob-cli-os.5.md) | The podcast route in bob ref create | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-os.6](bob-cli-os.6.md) | Capture jobs and Keep file episodes through the same route | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-os.7](bob-cli-os.7.md) | Publisher feed discovery and proven item match | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-os.8](bob-cli-os.8.md) | Publisher transcript parsing and paragraphing | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-os.9](bob-cli-os.9.md) | Feed enrichment in the dossier and both routes | ✓ closed | medium | 2026-11-21 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-os: Spotify episodes become first-class podcast references [in_progress]"]
    n1["bob-cli-os.1: General capture fixes the audit exposed [closed]"]
    n2["bob-cli-os.10: Podcast surfaces across repos and the legacy refs [closed]"]
    n3["bob-cli-os.2: Spotify link identity, canonical dedupe, and routing guards [closed]"]
    n4["bob-cli-os.3: Episode metadata ladder and show-notes segmentation [closed]"]
    n5["bob-cli-os.4: Adapter render op and the episode dossier template [closed]"]
    n6["bob-cli-os.5: The podcast route in bob ref create [closed]"]
    n7["bob-cli-os.6: Capture jobs and Keep file episodes through the same route [closed]"]
    n8["bob-cli-os.7: Publisher feed discovery and proven item match [closed]"]
    n9["bob-cli-os.8: Publisher transcript parsing and paragraphing [closed]"]
    n10["bob-cli-os.9: Feed enrichment in the dossier and both routes [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n1 -.-> n5
    n3 -.-> n4
    n4 -.-> n6
    n4 -.-> n8
    n4 -.-> n9
    n5 -.-> n6
    n6 -.-> n7
    n7 -.-> n10
    n8 -.-> n10
    n9 -.-> n10
    n10 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.1/README.md) | [bob-cli-os.1](bob-cli-os.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.10/README.md) | [bob-cli-os.10](bob-cli-os.10.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.2/README.md) | [bob-cli-os.2](bob-cli-os.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.3/README.md) | [bob-cli-os.3](bob-cli-os.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.4/README.md) | [bob-cli-os.4](bob-cli-os.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.5/README.md) | [bob-cli-os.5](bob-cli-os.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.6/README.md) | [bob-cli-os.6](bob-cli-os.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.7/README.md) | [bob-cli-os.7](bob-cli-os.7.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.8/README.md) | [bob-cli-os.8](bob-cli-os.8.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-os.9.md) | [bob-cli-os.9](bob-cli-os.9.md) | 1 |
| [bbugyi200.apollo.bob-cli-os.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.land/README.md) | [bob-cli-os](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ddc9e17`](https://github.com/bobs-org/bob-cli/commit/ddc9e177548417ca4bfe0b76107e00a2d649e2b6) | feat(ref)!: give Spotify links canonical identity and refuse non-episodes | [bob-cli-os.2](bob-cli-os.2.md) | 2026-11-21 16:05:39 EST |
| bob-cli | [`0114a6c`](https://github.com/bobs-org/bob-cli/commit/0114a6cc1e560df93de50edaa8821db627055702) | fix(ref): keep base62 ids out of stems, save ingest source stores, and print the recorded URL in mastheads | [bob-cli-os.1](bob-cli-os.1.md) | 2026-11-21 16:24:37 EST |
| bob-cli | [`2837fea`](https://github.com/bobs-org/bob-cli/commit/2837fea8003ddc4f5d77e730b15a7319ed7fb3ab) | feat(ref): add the Spotify episode metadata ladder and show-notes segmentation | [bob-cli-os.3](bob-cli-os.3.md) | 2026-11-21 17:21:13 EST |
| bob-cli | [`6b9139a`](https://github.com/bobs-org/bob-cli/commit/6b9139a65dc2780e839ecff3c2782a2ffcda0f61) | feat(ref): add the offline adapter render op and the podcast episode dossier | [bob-cli-os.4](bob-cli-os.4.md) | 2026-11-21 17:26:19 EST |
| bob-cli | [`0c60af4`](https://github.com/bobs-org/bob-cli/commit/0c60af4549c0ef621a815fb2594fc164276a16e0) | feat(ref): find the publisher feed item that proves a Spotify episode | [bob-cli-os.7](bob-cli-os.7.md) | 2026-11-21 21:07:05 EST |
| bob-cli | [`dbedc65`](https://github.com/bobs-org/bob-cli/commit/dbedc651f9027e8de7e48b0a58f0182e2c69b978) | feat(ref): parse publisher podcast transcripts into speaker paragraphs | [bob-cli-os.8](bob-cli-os.8.md) | 2026-11-21 23:10:10 EST |
| bob-cli | [`900772d`](https://github.com/bobs-org/bob-cli/commit/900772d9f9c9ba8746d93a116edf3970009056dd) | feat(ref): file Spotify episodes as podcasts references through the episode dossier route | [bob-cli-os.5](bob-cli-os.5.md) | 2026-11-21 23:43:55 EST |
| bob-cli | [`005f4c2`](https://github.com/bobs-org/bob-cli/commit/005f4c2b6e4e89319698d6080dfd71089ec9978d) | feat(ref): ingest Spotify episodes from capture jobs and Keep through the podcast route | [bob-cli-os.6](bob-cli-os.6.md) | 2026-11-22 00:53:30 EST |
| bob-cli | [`2f4fef6`](https://github.com/bobs-org/bob-cli/commit/2f4fef6dad5b749e944f3cf25fe31ceba351be42) | feat(ref): attach publisher feed notes and transcripts to episode dossiers | [bob-cli-os.9](bob-cli-os.9.md) | 2026-11-22 02:30:59 EST |
| bob-mac-capture | [`bob-mac-capture@310c946`](https://github.com/bobs-org/bob-mac-capture/commit/310c946b0e2f0880a623dc7453e8a4c455ff883e) | feat(refs): give podcasts refs their own Podcast kind | [bob-cli-os.10](bob-cli-os.10.md) | 2026-11-22 03:40:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.6.1.land][1] | Check whether the docs URL gate failure from os.7 is already recorded | 1 |
| read-by | [agent:bob-cli-os.1][2] | Need epic context and notes | 1 |
| read-by | [agent:bob-cli-os.2][3] | Need epic context and phase list | 2 |
| read-by | [agent:bob-cli-os.5][4] | Need epic context and notes from sibling phases | 2 |
| read-by | [agent:bob-cli-os.7][5] | See which sibling phases are in progress to avoid collisions | 2 |
| read-by | [agent:bob-cli-os.8][6] | Need epic overview and phase statuses | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-on.6.1.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.2/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.5/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.7/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.8/README.md

<!-- sase:referenced-by:end -->
