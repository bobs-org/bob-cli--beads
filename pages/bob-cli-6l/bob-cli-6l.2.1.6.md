# Bead: bob-cli-6l.2.1.6 — Assemble compute, prove the schema, and document the engine

[Bead Pages](../README.md) / [bob-cli-6l.2.1](bob-cli-6l.2.1.md) / bob-cli-6l.2.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.2.md) · **Assignee:** `bob-cli-6l.2.1.6` · **Size:** medium
**Created:** 2026-10-11 07:36:42 EDT · **Closed:** 2026-10-11 11:01:39 EDT
**Plan:** [202610/daily\_stats\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats_engine.md)

## Description

integration: wire the completed components into compute(&StatsRequest), add the golden fixture vault and independent expected report values, document all engine contracts and limitations in docs/stats.md, and verify read-only behavior, deterministic output, and the repository checks. Leave the enclosing phase and all ancestor closure to the child epic land agent.

## Notes

[2026-10-11T14:59:51Z · bob-cli-6l.2.1.6] PROPOSED FOLLOW-UP: cli capture::r#ref listen-worker tests fail identically on clean base 0d014c0 (failed_percent_listen_worker_keeps_listen_retry_guidance, percent_listen_reference_runs_existing_worker_and_installs_audio; audio worker env issue, unrelated to stats)

[2026-10-11T15:01:39Z · bob-cli-6l.2.1.6] compute() wired in stats/compute.rs with golden fixture vault (M1-M17 hand-computed), schema/error/determinism/read-only/duration-parity/grouped/default-range tests plus opt-in live-vault parity (sessions exact, worked floor, done Oct10 reconciled 37=45-7-1); docs/stats.md filled (kinds, catalog, config, quality, windows, schema, M-vector, limitations, later/rejected, ~2.4s live measurement); fixed #ref-tag kind classification, missing-vault Io surfacing, and grouped-bucket today exclusion (each with focused unit tests); just check green except 2 pre-existing cli listen failures reproduced on clean base (recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-6l.2.1.3](bob-cli-6l.2.1.3.md) ✓ · ⧖ 2026-10-11
- **Depends on:** [bob-cli-6l.2.1.5](bob-cli-6l.2.1.5.md) ✓ · ⧖ 2026-10-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.2.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.6/README.md) | [bob-cli-6l.2.1.6](bob-cli-6l.2.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f9324da`](https://github.com/bobs-org/bob-cli/commit/f9324da87f989be6388c4db3650f9bfc15c6f48e) | feat(stats): assemble compute, prove the schema, and document the engine | [bob-cli-6l.2.1.6](bob-cli-6l.2.1.6.md) | 2026-10-11 11:03:23 EDT |
