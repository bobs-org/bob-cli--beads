# Bead: bob-cli-k3.2 — Album recognition, the vault schema registry, and bob albums list and check

[Bead Pages](../README.md) / [bob-cli-k3](README.md) / bob-cli-k3.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.43.linker.w0` · **Assignee:** `bob-cli-k3.2` · **Size:** large
**Created:** 2026-11-11 04:56:43 EST · **Closed:** 2026-11-11 09:09:55 EST
**Plan:** [202611/album\_and\_record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md)

## Description

album-model: recognize `type: "[[album]]"` and `type: "[[record]]"`, parse album frontmatter (top-level facts plus one nested `record:` schema) with key-path and line diagnostics, build the vault-aware record-kind registry with per-album isolation and the album-wins transition rule over config, and ship the read-only `bob albums list` and `check` with beautiful human output and JSON.

## Notes

[2026-11-11T13:32:17Z · bob-cli-k3.2.1.land] CHILD LANDING BLOCKER: bob-cli-k3.2.1 verification found remaining resolver confinement, invalid-schema noun-claim recovery, report I/O/provenance, grouping shape, diagnostic compatibility, and album documentation gaps. Its land audit and follow-up triage are recorded on bob-cli-k3.2.1; a bounded repair tale will finish that child and then close only this parent phase normally. Do not unblock album-records by forcing closure. API handoff for bob-cli-k3.4 after repair: albums::registry::AlbumRegistry::{discover,from_snapshot,resolve_route}, resolve_route_head with explicit vault/config and optional known inventory, SourcedRecordType/RecordTypeSource, and RouteResolution distinguish album/config/invalid/unclaimed; TargetOnly does not prove global uniqueness. Use usable_types and preserve invalid claims (no fallback for a broken album). albums::grouping::group_records is the pure grouping seam for later index consumers. Keep capture/records consumers and config retirement in their assigned later phases.

[2026-11-11T14:10:28Z · bob-cli-k3.2.1.land] Album-model scope complete after closing child epic bob-cli-k3.2.1. Recognition, schema diagnostics, vault registry with album-wins and no config fallback for broken claims, and read-only bob albums list/check are landed. API handoff for bob-cli-k3.4: AlbumRegistry::{discover,from_snapshot,resolve_route}, resolve_route_head(vault, config, route, known), SourcedRecordType/RecordTypeSource, RouteResolution album/config/invalid/unclaimed/DiscoveryIncomplete, TargetOnly does not prove global uniqueness, usable_types plus invalid claims, albums::grouping::group_records. just check passed; json-outputs under the 6000-word cap; five inherited mounted docs budgets remain on bob-cli-jz / bob-cli-h9. epic-symbols empty. No just symvision recipe. Leave bob-cli-k3 and plan:202611/album_and_record_notes.md open.

## Dependencies

- **Blocks:** [bob-cli-k3.4](bob-cli-k3.4.md) ✓ · ⧖ 2026-11-11

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.47.mus][1] | Need album recognition and schema registry details for bank album research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.mus/README.md

<!-- sase:referenced-by:end -->
