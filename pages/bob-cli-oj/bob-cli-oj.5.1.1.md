# Bead: bob-cli-oj.5.1.1 — Kit group-row builder, rail missing-target states, and their CSS

[Bead Pages](../README.md) / [bob-cli-oj.5.1](bob-cli-oj.5.1.md) / bob-cli-oj.5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.md) · **Assignee:** `bob-cli-oj.5.1.1` · **Size:** medium
**Created:** 2026-11-21 12:21:10 EST · **Closed:** 2026-11-21 12:47:16 EST
**Plan:** [202611/group\_rail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/group_rail.md)

## Description

row-kit: add propertyCardBuildGroupRow (new 240l fragment, exported through a new 374d fragment), let propertyCardBuildRail take per-item `state` and an optional `group` row between the step row and the children strip, add the CSS for both rows (light, dark, narrow below 28rem, forced-colors, reduced motion), unit-test the builder, then build, test, bump, commit, and sync.

## Notes

[2026-11-21T17:46:40Z · bob-cli-oj.5.1.1] PROPOSED FOLLOW-UP: Load-sensitive Ledger/Nav timing tests flake only under the parallel full npm test — this phase saw test-ledger-tools-event-link-times.cjs:1069 (28.5/33.6 ms vs 25), test-ledger-tools-frees-marks.cjs:481 (73 ms vs 25), test-navigation-dependencies-stage-performance.cjs:64 (cubic-growth ratio), test-command-mode-sheet-sequence-dom.cjs:173 (30 s timeout), and a minute-rollover race in test-ledger-tools-gcal-events.cjs:761 (nowMinutes 761 vs 762); every file passes in isolation. Same class as the follow-up already recorded on bob-cli-oj.1; consider moving wall-time asserts to the serial perf lane and pinning the gcal test clock.

[2026-11-21T17:47:00Z · bob-cli-oj.5.1.1] PROPOSED FOLLOW-UP: bob-plugins docs/reference/plugins/bob-navigation-hotkeys.md is over the 6000-word reference budget (6247) on origin/master 7b44b29, failing npm run docs:check identically on the clean base (likely since the bob-cli-om.3 prose-field docs); no open bead tracks it. The other docs:check error (vault-format.md 6037/6000) is tracked by bob-cli-oc.

[2026-11-21T17:47:16Z · bob-cli-oj.5.1.1] row-kit landed in bob-plugins Ledger Tools 1.150.0 (on origin/master 7b44b29; commit via this turn's finalizer). New 240l propertyCardBuildGroupRow (arms with state/wrap/glyphs/narrow labels, centre position with sr label + wide/narrow, tick track or >21 bar+thumb), exported via new 374d; 240g propertyCardBuildRail takes per-item/chip state + ghostReason + tooltip (unresolved => creatable; exists DOM byte-identical, pinned by a serialization test), optional spec.group row between step row and children, group-only rails skip the empty step row, return gains group. CSS in its own 'Property-card group row (bob-cli-oj group-rail)' block right after the kit block: dashed+ creatable, dotted faint ghost, no unresolved underline on stated items, group grid/type/ticks/bar, narrow below 28rem for bob-property-card and record-walk containers, forced-colors (CanvasText/GrayText/Highlight), reduced motion. Verified: new scripts/test-ledger-tools-property-card-group-row.cjs 13/13 (registered in test:unit); identity + intention title-block tests unchanged and green; npm run build:check green; full npm test 8191/8197 with only load/timing flakes that pass in isolation (recorded as PROPOSED FOLLOW-UP); docs:check fails only on base budget errors (nav-hotkeys reference 6247/6000, vault-format 6037/6000 = bob-cli-oc), identical on the clean base. Throwaway Obsidian render (light/dark x 900/375 + forced-colors) checked: narrow collapses to '« 2025-Q4 · 1/13 · Q2 »', measured text/border contrast >= 5.15:1 for every state after pulling muted 15% and faint 45% toward --text-normal. bob plugins sync deployed 1.150.0; bob plugins list --no-pull shows synced.

## Dependencies

- **Blocks:** [bob-cli-oj.5.1.2](bob-cli-oj.5.1.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.5.1.3](bob-cli-oj.5.1.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md) | [bob-cli-oj.5.1.1](bob-cli-oj.5.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.5.1.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-oj.5.1.2][2] | Need row-kit closing note: version, commit, API | 1 |
| read-by | [agent:bob-cli-oj.5.1.3][3] | Need row-kit closing note: version, commit, API details | 1 |
| read-by | [agent:bob-cli-oj.5.1.4][4] | Need sibling phase notes (versions, commits, follow-ups) for rail-proof | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.4/README.md

<!-- sase:referenced-by:end -->
