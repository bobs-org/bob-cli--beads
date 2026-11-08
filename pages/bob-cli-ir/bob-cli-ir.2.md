# Bead: bob-cli-ir.2 — Records schema, catalog, renderer, and planner

[Bead Pages](../README.md) / [bob-cli-ir](README.md) / bob-cli-ir.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1a0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1a0.md) · **Assignee:** `bob-cli-ir.2` · **Size:** large
**Created:** 2026-11-08 11:06:11 EST
**Plan:** [202611/record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_notes.md)

## Description

records-engine: add the records config block and its validation, the per-folder catalog, the filename rule, the YAML renderer, and the record planner in a new records module, plus the records contract doc.

## Notes

[2026-11-08T18:39:38Z · bob-cli-ir.2.1.land] Child landing review found remaining epic-caused catalog/update safety defects and planner/doc contract gaps in bob-cli-ir.2.1 at 86af3d5e. See that epic landing-review note and file:explicit:0463132eb6eafca3abae823e. A medium repair tale will finish bob-cli-ir.2.1 and then close this phase normally after just check/docs-check; this phase remains open until then. The sole child PROPOSED FOLLOW-UP (bob-cli-ir.2.1.3 schema clippy failures) is already fixed by b9db7007, so no new task was filed. Containing epic bob-cli-ir remains the outer lander responsibility.

[2026-11-08T19:23:03Z · bob-cli-ir.2.1.land] BLOCKED CLOSEOUT at origin/master 9e0bcdd81aa8f39b4d0559df440a839e38fd582d: bob-cli-ir.2.1 implementation is complete and its focused records suite (64 passed, 1 ignored), just docs-gen, and just docs-check pass, but required `sase tool run check` ToolRun 4dbaae8977c2e80294c41a26c9844e73 fails on eight denied clippy::collapsible_if findings in newly landed Gmail sync files (`file.rs` lines 1117, 1961, 2116; `watch_apply.rs` lines 591, 600, 613, 625, 633). The records-specific lint from the check was fixed. These changes are outside records scope. Per the approved landing plan, leave bob-cli-ir.2 open and do not mark plan:202611/records_engine.md done until the required check is green; see blocker note on bob-cli-ir.2.1. Its only prior proposed follow-up (schema clippy note on bob-cli-ir.2.1.3) was already resolved by b9db7007; no duplicate task filed. Empty epic-symbol inventories; no symvision recipe.

## Dependencies

- **Blocks:** [bob-cli-ir.3](bob-cli-ir.3.md) ◐ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.5](bob-cli-ir.5.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.2.md) | [bob-cli-ir.2](bob-cli-ir.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.3t.mus][1] | research record notes unlock potential | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.3t.mus/README.md

<!-- sase:referenced-by:end -->
