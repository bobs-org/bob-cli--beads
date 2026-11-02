# Bead: bob-cli-fs.4 — Capture events, snapshot, reporting, and bob-authored group copy

[Bead Pages](../README.md) / [bob-cli-fs](README.md) / bob-cli-fs.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5m.linker.w0.md) · **Assignee:** `bob-cli-fs.4` · **Size:** large
**Created:** 2026-11-02 05:57:12 EST · **Closed:** 2026-11-02 18:56:49 EST
**Plan:** [202611/starts\_after\_relation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/starts_after_relation.md)

## Description

capture: raise parked events from x* closes and done events from every Rust managed Done, build the batch-scoped relation-sources snapshot, report relation offers in JSON and human output, add bob-authored copy to every pull_in group, extend the net pass, and measure the budget.

## Notes

[2026-11-02T23:57:13Z · bob-cli-fs.4.1.land--1] PHASE CLOSE (by epic bob-cli-fs.4.1 landing): parked events from x*, done events from every Rust managed Done, batch-scoped relation-sources snapshot, relation offers in JSON and human output, bob-authored copy on every pull_in group, extended net pass, and measured budgets all verified on b4a17e86 plus perf tree. Apollo re-measure: x* park 152.10/219.18 vs 235.93/321.82, ! Done 183.62/232.28 vs 250.94/344.18, dependents add -8.37ms (meets 5ms); hello/x medians meet 40ms; 70ms !/x* still miss on both binaries (pre-existing, bob-cli-gc). Gates: just check exit 0, just docs-check 447 passed 1 skipped, tiny-vault SA1/SA4 human+JSON smokes ok. Epic-symbols clean on bob-cli-fs.4 and bob-cli-fs.4.1; just symvision has no recipe in this repo. Epic bob-cli-fs left to its own land agent.

## Dependencies

- **Blocks:** [bob-cli-fs.10](bob-cli-fs.10.md) ◐ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fs.11](bob-cli-fs.11.md) ◐ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-fs.2](bob-cli-fs.2.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fs.5](bob-cli-fs.5.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.4.md) | [bob-cli-fs.4](bob-cli-fs.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fs.4.1.4][1] | Need capture phase scope and decisions | 1 |
| read-by | [agent:bob-cli-fs.4.1.5][2] | Need capture phase DECISIONS and scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.4.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.4.1.5/README.md

<!-- sase:referenced-by:end -->
