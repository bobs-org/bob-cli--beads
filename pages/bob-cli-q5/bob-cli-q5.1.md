# Bead: bob-cli-q5.1 — bob snooze core, wake writer, and tick step

[Bead Pages](../README.md) / [bob-cli-q5](README.md) / bob-cli-q5.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fx.md) · **Assignee:** `bob-cli-q5.1` · **Size:** large
**Created:** 2026-11-25 10:22:52 EST
**Plan:** [202611/snoozed\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md)

## Description

wake-engine: the snooze module (row grammar, states, time grammar), the bob snooze list/add/drop/wake CLI with guarded writes, never-running wake placement, struck history rows, the first-position tick step, the wake receipt plus Darwin post plus desktop fallback, the trailing-section writer audit, shared vectors, and docs/snooze.md.

## Notes

[2026-11-25T15:33:48Z · bob-cli-q5.1] PLANNING: Inspected clean HEAD 814b6583 and the approved snoozed_tasks design; no prior phase notes or snooze implementation were present. Authored and validated a five-phase child epic (row-model, mutation-planners, guarded-cli, wake-delivery, writer-audit), preserving all outer decisions. The child land agent owns verification and closure of bob-cli-q5.1; no implementation changes or status changes made. No epic-symbol entries currently reference this phase. Existing routing runs first and subtree relocation appends, so explicit never-running/top-insertion variants are required.

## Dependencies

- **Blocks:** [bob-cli-q5.2](bob-cli-q5.2.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.3](bob-cli-q5.3.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.md) | [bob-cli-q5.1](bob-cli-q5.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.1.1.2][1] | Need the enclosing phase and final decisions | 1 |
| read-by | [agent:bob-cli-q5.1.1.4][2] | Need the enclosing phase and final decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.4/README.md

<!-- sase:referenced-by:end -->
