# Bead: bob-cli-pf.5.1.3 — Extract lossless property source and clipboard fragments

[Bead Pages](../README.md) / [bob-cli-pf.5.1](bob-cli-pf.5.1.md) / bob-cli-pf.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.5.md) · **Assignee:** `bob-cli-pf.5.1.3` · **Size:** medium
**Created:** 2026-11-23 12:39:51 EST · **Closed:** 2026-11-23 14:34:19 EST
**Plan:** [202611/property\_editor\_parity.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_parity.md)

## Description

source-fragments: build a read-only, source-ordered YAML fragment adapter for exact property copying, source-seeded YAML stages, and validated clipboard mappings without changing bob's writer contract.

## Notes

[2026-11-23T19:34:11Z · bob-cli-pf.5.1.3] Full npm run test:unit: 9114/9121 pass; only 2 failures are perf-budget timings in test-ledger-tools-event-link-times.cjs (351ms/580ms vs 25ms budget under full-suite load). Both pass in isolation on this tree (15.9ms) and on clean HEAD (12.9ms): machine-load noise, not a regression.

[2026-11-23T19:34:19Z · bob-cli-pf.5.1.3] source-fragments done: 298r YAML source adapter (ordered entries, exact spans, trivia, valueYaml, opaque refusals), clipboard decoder, bounded snapshot reader, flow/block assembler, all exported via 379 and registered in fragments.json + test:unit. New suite 13/13 pass; all 10 property-editor suites 147/147 pass; build, build:check, docs inventory, docs:check green; bob-ledger-tools deployed byte-identical to vault. Full unit: only 2 load-noise perf failures, green in isolation. No epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-pf.5.1.2](bob-cli-pf.5.1.2.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pf.5.1.4](bob-cli-pf.5.1.4.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.3/README.md) | [bob-cli-pf.5.1.3](bob-cli-pf.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@310ce9b`](https://github.com/bobs-org/bob-plugins/commit/310ce9bb13192512d12a0dd1604615b4401d2296) | feat(property-editor): add read-only YAML source and clipboard fragments | [bob-cli-pf.5.1.3](bob-cli-pf.5.1.3.md) | 2026-11-23 14:35:17 EST |
