# Bead: bob-cli-pl.4.1.2 — Home-card host, title adoption, foot, and lifecycle integration

[Bead Pages](../README.md) / [bob-cli-pl.4.1](bob-cli-pl.4.1.md) / bob-cli-pl.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.4--1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.4.md) · **Assignee:** `bob-cli-pl.4.1.2` · **Size:** medium
**Created:** 2026-11-24 09:51:08 EST · **Closed:** 2026-11-24 10:45:01 EST
**Plan:** [202611/local\_home\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/local_home_cards.md)

## Description

mount-foot: mount the presentation in desktop Live Preview and Reading through the shared host and title kit, integrate the property foot and local invalidation, and test cleanup, exclusions, collapse, truthful inventory marks, and no writes or card-triggered subprocesses. Keep native Properties visible.

## Notes

[2026-11-24T15:44:33Z · bob-cli-pl.4.1.2] Host/foot entry points for card-live and editor-settings: BobLedgerToolsHomeCardMixin (249d-plugin-home-card-host.js) owns the shared adapter — homePropertyCardHost(), paintHomeCardReading(), buildHomeCardDecorations(), homeCardModelFor(), homeCardOpenSetting() (small callback seam routing policy chips by setting id; today opens openPropertyEditor filePath/key/mode:browse); BobLedgerToolsHomeCardFootMixin (249e-plugin-home-card-foot.js) owns the foot — homeCardFootSpec()/homeCardFootExtra()/homeCardFootHandlers(), homeCardAppendFoot()/homeCardTrackFoot(). Report-backed card-live patches can reuse exported homeCardModel/homeCardBuildEl plus the propertyCardAdoptPatch seam; invalidation flows through scheduleHomeCardRefresh() (metadata/Tasks/vault/date). Collapse: homeCardIsCollapsed()/homeCardSetCollapsed() per-normalized-path session Map.

[2026-11-24T15:45:01Z · bob-cli-pl.4.1.2] mount-foot done and verified in bob-plugins at 5717d518+uncommitted: one shared home adapter (249d host mixin, createPropertyCardHost kind=home, readingPriority 46, allowEmbedDisplay false, titleOwnership true) mounts the pure Area/Project presentation in desktop Live Preview and Reading with title adoption, per-path session collapse, modifier-aware links, and the editor browse seam; native Properties stays wholly visible (no FrontmatterOwn/OwnFrontmatter, no key hiding). Foot mixin (249e) appends the shared foot after content outside the collapsible body with truthful where-marks and the 5-key managed fold; area-missing-created silent, project says no created date. Paint reads only metadata cache, confirmed source, local home resolver, api.noteReady — zero writes/spawns asserted by unit spy plus source scan. New test-ledger-tools-home-card-host.cjs (10 tests, in test:unit) covers gates, denied contexts, collapse, where-marks, inert-vs-live chips, title/^prj preservation, no-write/no-spawn. Focused suites 25/25 pass (model/dom/host), album/record/intention 103/103, build:check + validate-manifests + docs:inventory:check green; vault synced via landed-commit recipe (clean sync then rebuilt mount-foot deploy).

## Dependencies

- **Depends on:** [bob-cli-pl.4.1.1](bob-cli-pl.4.1.1.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-pl.4.1.3](bob-cli-pl.4.1.3.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.4.1.2/README.md) | [bob-cli-pl.4.1.2](bob-cli-pl.4.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.4.1.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.4.1.2/README.md

<!-- sase:referenced-by:end -->
