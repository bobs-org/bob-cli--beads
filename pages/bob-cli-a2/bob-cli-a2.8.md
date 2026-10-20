# Bead: bob-cli-a2.8 — bob-ledger-tools live relation index and api.relationIndex

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.8` · **Size:** medium
**Created:** 2026-10-20 09:08:22 EDT · **Closed:** 2026-10-20 11:01:43 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

relation-index: build a raw-text relation index in bob-ledger-tools. It does a prefiltered startup scan including done/, reparses per file on change, delete, and rename, overlays unsaved editor text, publishes forward and reverse maps together, and resolves targets by path plus block id. Publish it as api.relationIndex v1 with label suggestions. Measure cold and warm costs.

## Notes

[2026-10-20T15:01:27Z · bob-cli-a2.8--1] Implemented and verified api.relationIndex v1 in bob-ledger-tools. Built and synced only bob-ledger-tools 1.59.3. Benchmark: 6,432 Markdown files, 3,162 prefiltered relation sources, zero existing edges; cold scan 256.87 ms. Warm update: 292,989 bytes with 250 synthetic same-note relations in 13.21 ms.

Verification: npm run validate passed all 7 plugins. Targeted note-ready, relation-index, and unload tests passed 60/60. Full npm test passed 3,292/3,298; the six failures match clean base 524bf72: four unblocked-glyph tests tracked by bob-cli-6v, Keep counts once tracked by bob-cli-6w, and forward conversion tracked by bob-cli-7i. npm run docs:check had 437 passed, 2 failed, 2 skipped; its two Material-theme failures reproduce identically on clean base because the installed mkdocs only offers mkdocs and readthedocs themes. bob plugins sync --no-pull -p bob-ledger-tools succeeded. epic-symbols reported no entries.

PROPOSED FOLLOW-UP: Resolve the six clean-base npm test failures: four unblocked-glyph tests (bob-cli-6v), Keep counts once (bob-cli-6w), and forward conversion (bob-cli-7i); this run reproduced the same failures at clean bob-plugins 524bf72.

PROPOSED FOLLOW-UP: Make docs:check provide the Material theme or skip the two Material-only tests when it is absent. test_templates_in_material and test_component_chips_in_material fail on current and clean-base runs because installed mkdocs offers only mkdocs and readthedocs themes.

[2026-10-20T15:01:43Z · bob-cli-a2.8--1] Verified api.relationIndex v1, build and validation, 60 targeted tests, measured performance, and successful bob-ledger-tools 1.59.3 sync; clean-base suite and docs failures are recorded in the phase note.

## Dependencies

- **Blocks:** [bob-cli-a2.10](bob-cli-a2.10.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a2.11](bob-cli-a2.11.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.3](bob-cli-a2.3.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-a2.8.md) | [bob-cli-a2.8](bob-cli-a2.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8d33457`](https://github.com/bobs-org/bob-plugins/commit/8d334570f89eec68978464a3126f4ff911621f19) | feat(ledger-tools): add live task relation index | [bob-cli-a2.8](bob-cli-a2.8.md) | 2026-10-20 11:10:12 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a2.8--1][1] | Need the phase scope, design file, notes, and current status | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-a2.8.md

<!-- sase:referenced-by:end -->
