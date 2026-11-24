# Bead: bob-cli-pf.4.1 — Complete the core note property editor

[Bead Pages](../README.md) / [bob-cli-pf.4](bob-cli-pf.4.md) / bob-cli-pf.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.md) · **Assignee:** `bob-cli-pf.4.1.land`
**Created:** 2026-11-22 23:01:42 EST · **Closed:** 2026-11-23 12:29:52 EST
**Plan:** [202611/property\_editor\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_core.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/property_editor_core.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_core.md

<!-- sase:links:end -->

## Description

Any Markdown note supports guarded keyboard-first property editing, add/delete, undo/redo, ownership routing, and YAML return through the verified =+ editor.

## Notes

[2026-11-23T08:06:08Z · bob-cli-pf.4.1.land] LAND TRIAGE of phase PROPOSED FOLLOW-UPs: (1) event-link-times 25ms budget flake (pf.4.1.1 #1, .3 #1, .4 #1) is a duplicate of bob-cli-km — +1 recorded; (2) frees-marks 25ms budget flake (same notes) is a duplicate of bob-cli-io — +1 recorded; (3) taskLinks keystroke p95 12.21/12ms flake from pf.4.1.6 #1 is a duplicate of bob-cli-pg — +1 recorded; (4) period-notes stub ensure failure (pf.4.1.1 #1, .2 #1) declined: already fixed by phase commit a7c91350's date fix, scripts/test-ledger-tools-period-notes.cjs passes on master; (5) nav req-close-twin byte drift (pf.4.1.1 #1) declined: fixed by 21331f33, scripts/test-req-close-twin-copies.cjs passes (22/22 with period-notes); (6) pf.4.1.3's clean-base nested-checkout fixture-path failures declined: an artifact of that agent running a base checkout under .sase/, not a repo defect. No new task beads created; none of these were caused by this epic.

[2026-11-23T08:08:27Z · bob-cli-pf.4.1.land] LAND VERIFICATION (bob-cli-pf.4.1.land): all six phases closed and their code is present in bob-plugins (298..298m, 379, 248m + arm, 242e props excursion, 160-sheet-rank CM row, docs/property-editor.md + cross-links); focused suites pass (property-update 23, shell 11, stages 9, add 15, entrypoints 19, CM surface 3, e2e self-test 2); epic-symbols none. Integration: commits since the epic started (bob-plugins 21331f33, e1ed13f0, 44e0f7e1, 3eb30fc3; bob-cli 9c9c972c, 51c31c00, 2b626d01) are requirement/docs work with no property-editor overlap; bob-cli 39661003 (props text|json, -d, derived/template roles) landed before phase 1 and the client already uses -f json / -d and trusts bob's roles. NOT COMPLETE: source review confirmed epic-caused defects — cancel/close during a save leaves pendingApply stuck and drops the write's history (298i apply/cancel); undo/redo lack an in-flight guard (298f/298c); modal sessions are not registered for generation bumps so Enter can hang at Checking value (298d/298f); any props show error envelope marks bob as old (298d); no onEscapeKey override; y/Ctrl+E leaves the modal open and picks the first leaf (298f/298m); requested key lost on reconcile (cacheRows index ids vs key::line) and Done reopens rows[0]; propertyPublishOverlay is a no-op so cards/drawers never see overlays; recovery diagnostics/error line not shown; datetime always gains an offset/seconds; tags stage coerces untouched items; null text + Enter writes ""; exact add-name loses to highlighted substring; o/O can drop a stage draft; stale phase-era UI strings. The real-Obsidian acceptance never ran (apollo has no Obsidian; athena does) and the harness covers only a fraction of the required bullets; docs/develop/validation.md lacks the harness. Remaining work proposed as child epic plan sase_plan_property_editor_landing_repairs.md (phases write-safety, row-fidelity, acceptance-writes, acceptance-surfaces) with parent_bead bob-cli-pf.4.1.

[2026-11-23T17:29:52Z · bob-cli-pf.4.1.7.land] All six original core-editor phases remain closed and present. Child repair epic bob-cli-pf.4.1.7 is complete: write-safety, row-fidelity, write and surface acceptance, plus YAML-Done selection (same key, duplicate occurrence, nearest survivor). Athena 130/130 with reviewed screenshots. Inherited decisions unchanged (bank foot, per-note drawer). No leftover epic-symbols. Post-child bob-cli/bob-plugins SHAs are still f6cf62cf / b2c37102. Unrelated drawer/task_reqs and clippy collapsible_if failures stay with their owners. pf.5/pf.6 remain later phases.

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.4.1.1][1] | Need DECISIONS section that phase workers must honor | 2 |
| read-by | [agent:bob-cli-pf.4.1.2][2] | Need parent epic decisions | 1 |
| read-by | [agent:bob-cli-pf.4.1.4][3] | Need parent epic DECISIONS that bind this phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.4.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.4.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.4.1.4/README.md

<!-- sase:referenced-by:end -->
