# Bead: bob-cli-qq.10.5 — Delete the cabinets gate, convert the tests, deploy, and smoke

[Bead Pages](../README.md) / [bob-cli-qq.10](bob-cli-qq.10.md) / bob-cli-qq.10.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.g7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.g7.md) · **Assignee:** `bob-cli-qq.10.5` · **Size:** medium
**Created:** 2026-11-27 09:12:20 EST · **Closed:** 2026-11-27 17:16:33 EST
**Plan:** [202611/finish\_property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_property_card_cabinets.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:b43b18736a494f39c0fdc3fc | switch-on smoke evidence bundle (run-3 report, 67 PNGs, regression probe) |
| related | file:explicit:c3a82701e970e5187726a714 | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

switch-on: delete 240w and every gate branch, and drop the dead preview keys from the runner. Convert the closed-gate tests, extend the passive suite, and give the runner a gate-free mode. Then build, test, run bob plugins sync, and run the post-switch smoke with prose Outline and a ref card.

## Notes

[2026-11-27T22:16:03Z · bob-cli-qq.10.5] PROPOSED FOLLOW-UP: Prune the dead pre-cabinet Properties-foot chrome — after switch-on propertyCardFootBuildEl always builds the cabinet panel, so the legacy .bob-property-card-foot-disclosure / -chevron / -stamp CSS and the legacy fold-row CSS reached only by unmapped fold kinds (240s fallback) are dead or nearly dead in styles.css; remove them with a screenshot diff.

[2026-11-27T22:16:10Z · bob-cli-qq.10.5] PROPOSED FOLLOW-UP: Make the cabinets runner screenshot matrix start from a reset panel state — LP "at rest" area shots keep Notebooks/Albums open from earlier runner steps (cabinet state is session-shared), so only the Reading shots show the four closed content cabinets; call resetPanels before each rest capture (scripts/obsidian-cabinets-e2e.cjs).

[2026-11-27T22:16:17Z · bob-cli-qq.10.5] PROPOSED FOLLOW-UP: Check the ref card kicker on a ref with no kind — the cabinets runner ref fixture (no kind property) renders "REF · REF · CASH" (species word repeated); verify against qp intent and the live vault refs, outside cabinets scope (249r ref card).

[2026-11-27T22:16:33Z · bob-cli-qq.10.5] Switch-on done in bob-plugins on top of 592c3c9a (bob-ledger-tools 1.173.0, deployed with bob plugins sync, no -F; two upstream-landed refusals handled per the refusal protocol by rebasing and re-bumping). Deleted 240w-plugin-cabinet-gate.js, its fragments entry, the plugin-data load/unload, and all 26 propertyCardCabinetsGateLive branches (open path kept). Also removed a stray console.log in 240wk, moved the bank Setup / album Schema focus-restore keys onto the disclosure button, and fixed a Reading-absorption race the switch exposed: 241al no longer untags nodes owned by a live replacement mount. Master also missed absorption on the first Reading open; it escaped after reloads only because of the async gate load. Converted 17 closed-gate suites to live-structure regressions; the kit test now proves stale cabinetsPreview/cardPreviewKinds/refCardPreview keys neither disable cabinets nor throw; extended the passive suite with real cabinet paint/toggle/pick/cancel/overlay (zero writes/spawns). The runner is gate-free: no preview keys; gate-closed baseline/perf-inline/parity retired; parity now runs against the stored regions; added a Reading-absorbed-after-reload check plus ref and Source-mode captures; validation.md updated. build:check, docs inventory, docs:check pass; test:unit 10427 pass / 1 fail (test-snooze-model-vectors, identical on clean master); test:perf 28/28. Athena smoke run-3: 103/103, 0 exceptions, 0 console errors, all 67 PNGs reviewed and every epic-acceptance item confirmed. Evidence: file:explicit:b43b18736a494f39c0fdc3fc (bundle), file:explicit:c3a82701e970e5187726a714 (review), both linked to bob-cli-qq.9.

## Dependencies

- **Depends on:** [bob-cli-qq.10.4](bob-cli-qq.10.4.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-qq.10.6](bob-cli-qq.10.6.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-ra.2](../bob-cli-ra/bob-cli-ra.2.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-ra.4](../bob-cli-ra/bob-cli-ra.4.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.10.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.5/README.md) | [bob-cli-qq.10.5](bob-cli-qq.10.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@64268af`](https://github.com/bobs-org/bob-plugins/commit/64268af9b91195b065e69cedbfc67733d91b4222) | feat(cabinets)!: switch property-card cabinets on and delete the preview gate | [bob-cli-qq.10.5](bob-cli-qq.10.5.md) | 2026-11-27 17:17:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qq.10.5][1] | Confirm switch-on evidence artifacts are attached | 2 |
| read-by | [agent:research.6o.final][2] | Consolidating link-walk research: need current cabinets finishing-phase status to sequence parallel work | 1 |
| read-by | [agent:research.6o.gem][3] | Check remaining bob-cli-qq work and property-card kit seams for parallel execution analysis | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6o.final/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6o.gem/README.md

<!-- sase:referenced-by:end -->
