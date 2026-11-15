# Bead: bob-cli-ln.4 — bob areas sync, nightly step, and Highlights coverage

[Bead Pages](../README.md) / [bob-cli-ln](README.md) / bob-cli-ln.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e2.md) · **Assignee:** `bob-cli-ln.4` · **Size:** medium
**Created:** 2026-11-14 16:33:04 EST · **Closed:** 2026-11-14 22:29:06 EST
**Plan:** [202611/areas\_catalog.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/areas_catalog.md)

## Description

areas-sync: add the guarded `bob areas sync` writer and dry run, the nightly step before projects, the Highlights regression test, integration tests, sync docs, and a read-only preview against the real vault.

## Notes

[2026-11-15T03:28:49Z · bob-cli-ln.4] PROPOSED FOLLOW-UP: docs-check offline lychee reports a broken bank/index.html link to reference/plugins/bob-navigation-hotkeys#bank-walk; neither docs/bank.md nor the plugin reference page is touched by this phase, so it reproduces independently of areas-sync — triage as a docs/bank-plugin link task -r Recording pre-existing docs-check lychee failure found during areas-sync verification

[2026-11-15T03:29:06Z · bob-cli-ln.4] areas-sync done: guarded bob areas sync writer + dry-run with areas: sync catalogs (N notes) commits, nightly areas step before projects (9-step order + help/about/confirm text), [!areas] Highlights regression test, 6 new CLI integration tests (5-host commit, noop, dry-run, damaged, reparent, placement both orders, nightly), sync/nightly docs plus json-outputs row, regenerated CLI reference and help snapshots. Verified: focused suites pass (areas 15, notebooks_catalog, albums_sync, vault_sync, periods, catalog, help, lib areas/highlights), fmt clean, clippy gate error-free, read-only real-vault preview shows exactly area/cash/gtd/inbox/love.md changing with area.md matching the contract. One pre-existing docs-check lychee failure recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-ln.3](bob-cli-ln.3.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-ln.6](bob-cli-ln.6.md) ◐ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-ln.7](bob-cli-ln.7.md) ✓ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ln.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.4/README.md) | [bob-cli-ln.4](bob-cli-ln.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`81a4b02`](https://github.com/bobs-org/bob-cli/commit/81a4b022a8037eee9f734f50ade09c284362dd89) | feat(areas): add guarded areas sync writer, nightly step, and coverage | [bob-cli-ln.4](bob-cli-ln.4.md) | 2026-11-14 22:31:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ln.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.4/README.md

<!-- sase:referenced-by:end -->
