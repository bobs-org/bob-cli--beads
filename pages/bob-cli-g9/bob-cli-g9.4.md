# Bead: bob-cli-g9.4 — Lane keep counting and the always-logged Rotten Log

[Bead Pages](../README.md) / [bob-cli-g9](README.md) / bob-cli-g9.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.32.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.32.linker.w0.md) · **Assignee:** `bob-cli-g9.4` · **Size:** medium
**Created:** 2026-11-02 15:55:43 EST · **Closed:** 2026-11-02 19:20:44 EST
**Plan:** [202611/task\_decay\_ladder.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_decay_ladder.md)

## Description

nav-keeps: count due WIP and Next keeps, ask "Why keep it in <rung>?" with the allowance shown, always write a rung-qualified Rotten Log entry (🤷 when blank), stop the Work Log prompt on every freshness gesture, ship the shared Rotten Log grammar and per-rung tallies in both plugins, and leave lane decisions count-only until the card supports them.

## Notes

[2026-11-03T00:19:43Z · bob-cli-g9.4] PROPOSED FOLLOW-UP: schedule-work-log Blocked marking — future scheduling on Pending writes [/] not [?], reproduces identically on the clean base tree

[2026-11-03T00:19:57Z · bob-cli-g9.4] PROPOSED FOLLOW-UP: relation-index startup replay test fails on the clean base tree (timing-sensitive, unrelated to decay work)

[2026-11-03T00:20:04Z · bob-cli-g9.4] PROPOSED FOLLOW-UP: command-mode production sheet DOM test fails on the clean base tree (unrelated to decay work)

[2026-11-03T00:20:13Z · bob-cli-g9.4] PROPOSED FOLLOW-UP: freshness-namespace reload-event test fails on the clean base tree (unrelated to decay work)

[2026-11-03T00:20:21Z · bob-cli-g9.4] PROPOSED FOLLOW-UP: startup-storm linearity perf test fails on the clean base tree and flakes in full-suite runs (passes/fails by timing)

[2026-11-03T00:20:44Z · bob-cli-g9.4] nav-keeps done: due WIP/Next keeps count with rung (WIP/Next/Ready/P-level); prompts ask Why keep it in <rung>? with allowance subtitle and always log rung-qualified entries (blank logs no reason given); early/Today-linked lane keeps stamp quietly with early-not-counted notice; Work Log removed from every freshness gesture; shared grammar fixture mirrored in both plugins with fixture-driven tests plus per-rung tallies in tooltips and card header; duplicate-marker refusal writes nothing with repair message; lane decide rows count/log with no card or skip behind FRESHNESS_DECAY_CARD_VERSION<3; lane writers verified to stamp (clear keeps). Verified: npm run build ok, all touched suites green (rotten-keep/log, keep-counting, refresh-modal, freshness, decay suites, ledger mark/keeps/decision-card), full npm test shows only clean-tree pre-existing failures (recorded as follow-ups), bob-cli just docs-check ok, cargo fmt/lint/test ok, plugin docs:check ok, manifests bumped nav 2.72.0 + ledger 1.95.0, bob plugins sync deployed to vault.

## Dependencies

- **Depends on:** [bob-cli-g9.1](bob-cli-g9.1.md) ✓ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-g9.3](bob-cli-g9.3.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-g9.5](bob-cli-g9.5.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-g9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-g9.4/README.md) | [bob-cli-g9.4](bob-cli-g9.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0bdcea7`](https://github.com/bobs-org/bob-cli/commit/0bdcea7aedc9177b2f318e4aabe6c7383df21670) | docs(freshness): add freshness and vault-format reference docs for nav-keeps | [bob-cli-g9.4](bob-cli-g9.4.md) | 2026-11-02 19:22:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-g9.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-g9.4/README.md

<!-- sase:referenced-by:end -->
