# Bead: bob-cli-7c.1 — Successor Offers contract, vectors, and docs

[Bead Pages](../README.md) / [bob-cli-7c](README.md) / bob-cli-7c.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.11.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.11.linker.w0.md) · **Assignee:** `bob-cli-7c.1` · **Size:** medium
**Created:** 2026-10-13 09:48:12 EDT · **Closed:** 2026-10-13 10:15:00 EDT
**Plan:** [202610/successor\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_offers.md)

## Description

contract: rewrite task-dependencies §12 as Successor Offers (offer ladder, project offers, pull-in offers, breaker deletion, selection, pick writes, keys, JSON, CLI flags, nav picker API), add the SO vector table, retire SL17/PP15/PDC2, and update capture/plan/freshness docs plus the README, getting-started, and hooks mentions.

## Notes

[2026-10-13T14:15:00Z · bob-cli-7c.1] Rewrote docs/task-dependencies.md §12 as Successor Offers (offer ladder, project offers, pull-in offers, breaker deletion, selection, pick writes, keys, JSON, CLI flags, nav picker API). Added SO1–SO32. Retired SL17 and PP15 (ids kept). Replaced PDC2 with project-group offers. Updated capture.md (step 6, close JSON, -p/--pull-in, pull_in_choice_required, not_linked including project_member/not_selected/no_destination), plan.md link_unblocked, freshness.md §5 pick stamps, README, getting-started, task-status-hooks, and docs/README. epic-symbols: no leftovers. Docs-only; memory stays on bob-cli-7c.8. Repo has no markdown formatter; cargo fmt is N/A for these files.

[2026-10-13T14:33:19Z · bob-cli-7c.1--1] PROPOSED FOLLOW-UP: just check fails identically on clean HEAD 92515f1 — capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio (ref.rs:942 NotFound) and failed_percent_listen_worker_keeps_listen_retry_guidance (ref.rs:991 listen runner was invoked); already tracked by bob-cli-6m

## Dependencies

- **Blocks:** [bob-cli-7c.2](bob-cli-7c.2.md) ◐ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.4](bob-cli-7c.4.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.5](bob-cli-7c.5.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7c.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.1.md) | [bob-cli-7c.1](bob-cli-7c.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2d1adfa`](https://github.com/bobs-org/bob-cli/commit/2d1adfa7d7c794929e8e198a013379f059e7f8fb) | docs(tasks): rewrite successor links as Successor Offers | [bob-cli-7c.1](bob-cli-7c.1.md) | 2026-10-13 10:35:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7c.1--1][1] | Need the phase scope, notes, and design file after failed just check | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.1.md

<!-- sase:referenced-by:end -->
