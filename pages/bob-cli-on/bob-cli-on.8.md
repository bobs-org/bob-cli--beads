# Bead: bob-cli-on.8 — Requirements on the capture successor card

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.8` · **Size:** large
**Created:** 2026-11-21 11:13:26 EST · **Closed:** 2026-11-22 14:47:55 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

close-engine: build per-owner requirement groups for managed Done closes, the met/drop/carry/pull-in verdicts with overlap and staleness refusals, CLI flags and the --req-choice gate, JSON and receipts, RV vectors, and §12 docs.

## Notes

[2026-11-22T19:49:26Z · bob-cli-on.8.1.land] Phase close-engine delivered. Child epic bob-cli-on.8.1 closed done after landing tale plan:202611/req_close_landing_fixes.md. Per-owner requirement groups, Met/Drop/Carry/CarryPulled with overlap and staleness refusals, CLI flags and --req-choice, JSON/receipts, and RV vectors are in: docs/task-dependencies.md §§12.5, 12.13, 12.14, 12.25, 12.26; docs/reference/json-outputs.md; tests/fixtures/req_close/vectors.json schema_version 1, RV1–RV44+. Overlap ancestry now walks owner.nodes (RV44); Pomodoro close x! carry+pull-in uses the closing continuation; req_* dead-code suppressions removed. just check and just docs-check passed on HEAD 96a23f50 plus this landing's dirty tree. sase bead epic-symbols is empty for bob-cli-on.8 and bob-cli-on.8.1. Parent epic bob-cli-on stays open.

## Dependencies

- **Blocks:** [bob-cli-on.11](bob-cli-on.11.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.15](bob-cli-on.15.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.17](bob-cli-on.17.md) ◐ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.2](bob-cli-on.2.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.6](bob-cli-on.6.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.7](bob-cli-on.7.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.md) | [bob-cli-on.8](bob-cli-on.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.7][1] | Check what the close-engine phase expects from carry_req (my phase's library entry) | 1 |
| read-by | [agent:bob-cli-on.8.1.1][2] | Need grandparent epic DECISIONS that this phase must honor | 1 |
| read-by | [agent:research.5u.gem][3] | Inspect display-related and remaining phases of bob-cli-on | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.gem/README.md

<!-- sase:referenced-by:end -->
