# Bead: bob-cli-pf.4.1.4 — Property name completion and positioned creation

[Bead Pages](../README.md) / [bob-cli-pf.4.1](bob-cli-pf.4.1.md) / bob-cli-pf.4.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.md) · **Assignee:** `bob-cli-pf.4.1.4` · **Size:** medium
**Created:** 2026-11-22 23:01:42 EST · **Closed:** 2026-11-23 01:33:12 EST
**Plan:** [202611/property\_editor\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_core.md)

## Description

add-flow: implement positioned insertion, vault name/type/count completion, literal-name override, and atomic first-property creation through typed stages.

## Notes

[2026-11-23T06:32:55Z · bob-cli-pf.4.1.4] PROPOSED FOLLOW-UP: Full npm test still flakes the existing 25ms wall-clock budgets in scripts/test-ledger-tools-event-link-times.cjs:1069 (108.4ms) and scripts/test-ledger-tools-frees-marks.cjs:481 (310ms) under suite load; both pass in isolation (event-link-times 5.6ms). Tracked by bob-cli-km and bob-cli-io.

[2026-11-23T06:33:12Z · bob-cli-pf.4.1.4] Add-flow is wired inside the property editor: o inserts below the selected source key, O above, Mod+; at the end. Name completion uses metadataCache.getAllPropertyInfos() with a cache-derived fallback that does not invent types; Tab/Enter takes the completion type and Shift+Enter keeps a literal text key. Empty/duplicate/invalid names are rejected locally, prospective ownership is left to bob, and name/value cancel writes nothing. First-property create is one prop.set against the empty-mapping fingerprint; undo/redo round-trip. Verified with npm run build, the new add tests plus stages/shell (34), isolated re-runs of prose-field-roles after the bob-text marker, and bob plugins sync. epic-symbols had no leftovers. Full npm test still hit the existing event-link-times/frees-marks 25ms flakes (bob-cli-km, bob-cli-io); those pass in isolation.

## Dependencies

- **Depends on:** [bob-cli-pf.4.1.3](bob-cli-pf.4.1.3.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pf.4.1.5](bob-cli-pf.4.1.5.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.4.1.4/README.md) | [bob-cli-pf.4.1.4](bob-cli-pf.4.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@15e1fa6`](https://github.com/bobs-org/bob-plugins/commit/15e1fa6bbbb3785b261d7cbcc79d89490d422541) | feat(property-editor): add positioned creation with vault name completion | [bob-cli-pf.4.1.4](bob-cli-pf.4.1.4.md) | 2026-11-23 01:34:36 EST |
