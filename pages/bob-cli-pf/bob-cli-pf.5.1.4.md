# Bead: bob-cli-pf.5.1.4 — Add the validated multiline YAML value stage

[Bead Pages](../README.md) / [bob-cli-pf.5.1](bob-cli-pf.5.1.md) / bob-cli-pf.5.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.5.md) · **Assignee:** `bob-cli-pf.5.1.4` · **Size:** small
**Created:** 2026-11-23 12:39:51 EST · **Closed:** 2026-11-23 15:06:04 EST
**Plan:** [202611/property\_editor\_parity.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_parity.md)

## Description

yaml-stage: add source-seeded YAML value editing through prop.set_yaml and the existing preview latch; retain opaque-key refusals and the source excursion.

## Notes

[2026-11-23T20:05:54Z · bob-cli-pf.5.1.4] PROPOSED FOLLOW-UP: wall-clock perf budgets in test-ledger-tools-event-link-times.cjs (25 ms, took ~130 ms) and test-ledger-tools-frees-marks.cjs (25 ms, took ~360-575 ms) fail under full-suite load but pass 40/40 in isolation; consider raising budgets or marking them load-tolerant

[2026-11-23T20:06:04Z · bob-cli-pf.5.1.4] yaml-stage done: new 298s fragment adds the source-seeded multiline YAML stage (Enter on loose maps/opaque rows, All-actions Edit value as YAML, single prop.set_yaml op through the 250 ms dry-run and preview latch, plain Enter newline, Mod+Enter save, Esc cancel, opaque/prop_opaque refusals verbatim with draft retained, y/Ctrl+E excursion untouched). 25 new tests pass; all 188 property-editor suites pass; build, build:check, docs:check, docs inventory pass; bob-ledger-tools synced to the vault. Full npm test: 9139 pass, 2 pre-existing load-sensitive perf-budget flakes (recorded as follow-up). No epic symbols.

## Dependencies

- **Depends on:** [bob-cli-pf.5.1.3](bob-cli-pf.5.1.3.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pf.5.1.5](bob-cli-pf.5.1.5.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.4/README.md) | [bob-cli-pf.5.1.4](bob-cli-pf.5.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1d78b50`](https://github.com/bobs-org/bob-plugins/commit/1d78b500e156b45563ec7cd38787bf4aab1e42bd) | feat(property-editor): add the validated multiline YAML value stage | [bob-cli-pf.5.1.4](bob-cli-pf.5.1.4.md) | 2026-11-23 15:07:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.5.1.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.4/README.md

<!-- sase:referenced-by:end -->
