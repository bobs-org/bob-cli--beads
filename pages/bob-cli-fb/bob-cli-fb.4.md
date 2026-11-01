# Bead: bob-cli-fb.4 — Obsidian cycler engine

[Bead Pages](../README.md) / [bob-cli-fb](README.md) / bob-cli-fb.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bz](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bz.md) · **Assignee:** `bob-cli-fb.4` · **Size:** large
**Created:** 2026-11-01 12:29:36 EST · **Closed:** 2026-11-01 17:12:43 EST
**Plan:** [202611/leaf\_project\_keep\_moving\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/leaf_project_keep_moving_offers.md)

## Description

cycler: port the rule to task-status-cycler for every Obsidian close surface. Covers leaf detection, gates, offers, the picker model, notice text, the receipt, and the config loader.

## Notes

[2026-11-01T19:43:29Z · bob-cli-fb.4--1] PROPOSED FOLLOW-UP: Restore the bob-plugins npm test gate on this host: command-mode DOM coverage lacks Chromium, and four unrelated ledger-tools checks fail in isolation (freshness namespace reload, Gcal layout-ready listener, note-ready startup scan count, relation-index startup scan). The Task Status Cycler tests passed; docs:check and manifest validation passed.

[2026-11-01T22:12:05Z · bob-cli-fb.4--1] PROPOSED FOLLOW-UP: Byte-order offer paths in the cycler — successorOfferOrderCompare uses localeCompare while Rust OfferOrderKey compares PathBuf bytes, so mixed-case note paths order differently across engines (all offer groups, pre-existing)

[2026-11-01T22:12:43Z · bob-cli-fb.4--1] Keep-moving finish done in bob-plugins linked checkout (uncommitted diff on top of 1d66ffd: 8 files, +367/-47 — cycler src, manifest 1.43.1, docs, 2 test files). Cycler gates: 52/52 pass (keep-moving + successor-picker). docs:check passed (447 passed, 1 skipped). validate-manifests 8/8 valid. Full npm test: 6 failures, all base-tree/environmental — 4 known ledger-tools failures per note #1 (freshness-namespace reload, gcal-events layout-ready, note-ready startup storm, relation-index startup replay), 1 Chromium-less command-mode DOM test (no Chromium on host), 1 Live Preview perf bound that passes in isolation (3619ms solo vs 6677ms under full-suite load; changed files touch only cycler/docs/tests). bob plugins sync -F task-status-cycler from this checkout; vault manifest confirms 1.43.1 (backup in plugin-backups/20261101-171156). Byte-order follow-up recorded as note #2. Live Obsidian verification left to Bryan.

## Dependencies

- **Depends on:** [bob-cli-fb.1](bob-cli-fb.1.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-fb.3](bob-cli-fb.3.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fb.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.4.md) | [bob-cli-fb.4](bob-cli-fb.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fb.4--1][1] | Review assigned phase scope and record any unrelated gate issue correctly | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.4.md

<!-- sase:referenced-by:end -->
