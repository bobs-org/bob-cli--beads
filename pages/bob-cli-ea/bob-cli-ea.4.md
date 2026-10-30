# Bead: bob-cli-ea.4 — bob gcal skeleton, gog transport, login, logout, doctor, calendars

[Bead Pages](../README.md) / [bob-cli-ea](README.md) / bob-cli-ea.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2w.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2w.linker.w0.md) · **Assignee:** `bob-cli-ea.4` · **Size:** medium
**Created:** 2026-10-29 19:40:04 EDT · **Closed:** 2026-10-29 21:38:35 EDT
**Plan:** [202610/bob\_gcal\_daily\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_gcal_daily_events.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-ef][1] | Phase that extracted gkeep's runner into subprocess_runner and proposed this follow-up (note #1) |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ef/README.md

<!-- sase:links:end -->

## Description

gcal-auth: extract gkeep's hardened subprocess runner, add the gcal module, config block, and gog transport with the BOB_GCAL_GOG test seam, ship login, logout, doctor, and calendars with beautiful output, register the command, and write the setup contract and guide.

## Notes

[2026-10-30T01:09:28Z · bob-cli-ea.4] PROPOSED FOLLOW-UP: Extract highlights_ref/clip_adapter.rs onto shared subprocess_runner — clip_adapter still has its own process_group/ETXTBSY/drain_pipe copy after gkeep was extracted for gcal.

[2026-10-30T01:12:34Z · bob-cli-ea.4] Verified docs-gen, docs-check, gcal_auth+gcal_cli FakeGog tests, clippy deny gates, and no leftover --epic-symbol entries. just check is the remaining host verification gate.

[2026-10-30T01:38:35Z · bob-cli-ea.4--1] Registered bob gcal (login, logout, doctor, calendars) with gog transport and BOB_GCAL_GOG. Verified gcal_auth (23) and gcal_cli (5) FakeGog tests, catalog count 58, Integrations alphabetical order (gcal before gkeep), root help snapshots, fmt, clippy deny gates, and no leftover --epic-symbol entries. Pinned capture-related archive mtime test to BOB_NOW so the 30-day window does not drift with wall-clock.

[2026-10-30T02:04:58Z · bob-cli-ea.4--2] Regenerated CLI reference via just docs-gen so gcal sorts before gkeep in docs/reference/cli/index.md and mkdocs.yml Integrations nav; docs_reference::cli_reference_is_current now passes.

## Dependencies

- **Blocks:** [bob-cli-ea.5](bob-cli-ea.5.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ea.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ea.4.md) | [bob-cli-ea.4](bob-cli-ea.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`26e6b1d`](https://github.com/bobs-org/bob-cli/commit/26e6b1d1e50b0c9c70daa497214e7f5420c60283) | feat(gcal): add bob gcal login, logout, doctor, and calendars | [bob-cli-ea.4](bob-cli-ea.4.md) | 2026-10-29 23:27:30 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ea.4--3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ea.4.md

<!-- sase:referenced-by:end -->
