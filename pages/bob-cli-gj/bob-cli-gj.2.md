# Bead: bob-cli-gj.2 — bob-cli note pull grammar, planner, picks, and output

[Bead Pages](../README.md) / [bob-cli-gj](README.md) / bob-cli-gj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.17g](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.17g.md) · **Assignee:** `bob-cli-gj.2` · **Size:** large
**Created:** 2026-11-03 11:56:54 EST · **Closed:** 2026-11-04 08:31:26 EST
**Plan:** [202611/note\_pull.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_pull.md)

## Description

cli: implement the lone-header `note_pull` kind in the capture language and capture-parse. Build the staged planner that classifies residents, keys, orders, places, and writes picks; wire it into pull-in numbering, the net pass, refusals, inbox routing, JSON, and human output; add tests for every NP vector.

## Notes

[2026-11-04T13:33:36Z · bob-cli-gj.2.1.land] CLI phase closure evidence: grammar is revision 10 and lone @route parses as note_pull; planner classification and explicit picks, net filtering, refusals, inbox routing, additive JSON, human output, and NP1–NP28 coverage are complete. Child epic bob-cli-gj.2.1 and all four child phases are closed. The final landing added move-aware note-pull net identity and met the 70 ms p95 target on the isolated vault. cargo check --all-targets --locked passes; focused note-pull, theme, index, and traversal tests pass. just check failures were reproduced on clean base; docs-check is blocked by the missing front matter in sase/memory/glossary/task-merge.md. bob-cli-gj.3 remains the active Mac Capture phase; parent epic bob-cli-gj remains open.

## Dependencies

- **Depends on:** [bob-cli-gj.1](bob-cli-gj.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gj.3](bob-cli-gj.3.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.2.md) | [bob-cli-gj.2](bob-cli-gj.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gj.2.1.1][1] | Need CLI phase scope and decisions | 1 |
| read-by | [agent:bob-cli-gj.2.1.2][2] | Need CLI phase scope and decisions | 1 |
| read-by | [agent:bob-cli-gj.2.1.3][3] | Need parent phase decisions and remaining-work notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gj.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gj.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gj.2.1.3/README.md

<!-- sase:referenced-by:end -->
