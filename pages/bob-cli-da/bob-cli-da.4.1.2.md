# Bead: bob-cli-da.4.1.2 — Integrate the assets crate with the daily release train

[Bead Pages](../README.md) / [bob-cli-da.4.1](bob-cli-da.4.1.md) / bob-cli-da.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-da.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.md) · **Assignee:** `bob-cli-da.4.1.2` · **Size:** medium
**Created:** 2026-10-27 16:43:43 EDT · **Closed:** 2026-10-27 17:39:27 EDT
**Plan:** [202610/embedded\_assets\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/embedded_assets_split.md)

## Description

release-integration: verify independent assets versioning and unique tags under the existing release-plz train, cover multi-package release output and preview behavior, update release documentation, and supply final package measurements. Follow the release-integration section below; leave closure of bob-cli-da.4 to this child epic's land agent.

## Notes

[2026-10-27T21:39:10Z · bob-cli-da.4.1.2] PROPOSED FOLLOW-UP: how-the-release-train-works.md still calls the assets split a future design choice — update that guide sentence now that bob-obsidian-assets ships on the shared train.

[2026-10-27T21:39:14Z · bob-cli-da.4.1.2] PROPOSED FOLLOW-UP: decisions:bob-cli-releases-ride-a-daily-train reopen condition (package size forcing an assets crate) is now true; this epic forbade memory edits, so file a successor record rather than editing the accepted note.

[2026-10-27T21:39:27Z · bob-cli-da.4.1.2] Release integration verified with pinned release-plz 0.3.173. Config parses unique tags v{{version}} vs bob-obsidian-assets-v{{version}}; assets git_release_enable=false. Disposable fixture: root-only 0.4.0->0.4.1 assets 0.1.0 unchanged; assets change 0.1.0->0.1.1 with root dep 0.1.0->0.1.1. Full-repo clone: root 0.4.0->0.5.0, assets initial 0.1.0, tags v0.5.0 vs bob-obsidian-assets-v0.1.0; clone discarded with no retained edits. Binary outputs still select package_name==bob-obsidian; mixed/assets-only/empty covered. just check-release-tools 108 tests; just docs-check 447 passed 1 skipped (fonts generation deps absent); just package-check full verify: bob-obsidian 3,217,425B (3.07 MiB, 4.93 MiB headroom), bob-obsidian-assets 5,004,764B (4.77 MiB, 3.23 MiB headroom). No epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-da.4.1.1](bob-cli-da.4.1.1.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-da.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.1.2.md) | [bob-cli-da.4.1.2](bob-cli-da.4.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3cc6351`](https://github.com/bobs-org/bob-cli/commit/3cc6351158e074791330ad539761ad9dbcadd2f6) | feat(release): integrate bob-obsidian-assets with the daily train | [bob-cli-da.4.1.2](bob-cli-da.4.1.2.md) | 2026-10-27 17:59:20 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-da.4.1.2--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.1.2.md

<!-- sase:referenced-by:end -->
