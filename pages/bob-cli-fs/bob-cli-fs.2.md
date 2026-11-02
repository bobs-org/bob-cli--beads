# Bead: bob-cli-fs.2 — Rust policy and relation-successor engine

[Bead Pages](../README.md) / [bob-cli-fs](README.md) / bob-cli-fs.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5m.linker.w0.md) · **Assignee:** `bob-cli-fs.2` · **Size:** large
**Created:** 2026-11-02 05:57:11 EST
**Plan:** [202611/starts\_after\_relation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/starts_after_relation.md)

## Description

core: add relations.successor_labels and the LabelEffect policy, build the pure relation-successor planner and copy builder, and integrate relation offers into plan_successors (dedup, order, keys, placement), all pinned by the shared vectors.

## Dependencies

- **Depends on:** [bob-cli-fs.1](bob-cli-fs.1.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fs.3](bob-cli-fs.3.md) ◐ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fs.4](bob-cli-fs.4.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.2.md) | [bob-cli-fs.2](bob-cli-fs.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fs.2.1.1][1] | Need phase-level constraints and authorized decisions | 1 |
| read-by | [agent:bob-cli-fs.2.1.2][2] | Need parent phase DECISIONS and remaining work notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.2/README.md

<!-- sase:referenced-by:end -->
