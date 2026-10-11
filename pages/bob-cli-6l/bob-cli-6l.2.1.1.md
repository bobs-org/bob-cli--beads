# Bead: bob-cli-6l.2.1.1 — Define the stats model and configurable metric registry

[Bead Pages](../README.md) / [bob-cli-6l.2.1](bob-cli-6l.2.1.md) / bob-cli-6l.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.2.md) · **Assignee:** `bob-cli-6l.2.1.1` · **Size:** medium
**Created:** 2026-10-11 07:36:42 EDT · **Closed:** 2026-10-11 08:27:41 EDT
**Plan:** [202610/daily\_stats\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats_engine.md)

## Description

contracts: implement the schema-1 report and request types, isolated stats configuration, eleven built-ins through the same entry validator as custom metrics, and formula parsing and dependency validation. Establish the interfaces below; do not add a CLI or a placeholder compute implementation.

## Notes

[2026-10-11T12:27:20Z · bob-cli-6l.2.1.1] PROPOSED FOLLOW-UP: CLI tests capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio and failed_percent_listen_worker_keeps_listen_retry_guidance fail identically on clean master (listen.log missing / listen runner not invoked, isolation and just check); unrelated to stats contracts. No existing task bead tracks these two tests (bob-cli-5l is lib ETXTBSY).

[2026-10-11T12:27:41Z · bob-cli-6l.2.1.1] Verified contracts: schema-1 StatsRequest/StatsError/StatsReport/DailyValue/StatsIndex types, isolated stats: YAML loader that cannot break plan/freshness/highlights/gkeep, eleven builtins as literal YAML through the same parser as custom metrics, task_kind: task|prj|ref, formula AST (ints/ids/unary minus/parens/+-*/) with cycle/unknown-ref invalidation, hide keeps deps/explicit select, invalid redefinition does not fall back. 32 native::stats/config::stats tests passed. cargo fmt and clippy clean for this work. just check otherwise green; two capture percent-listen CLI tests fail identically on clean master (see follow-up note). No CLI or compute(). No epic-symbol leftovers. Did not close parent bob-cli-6l.2.1.

## Dependencies

- **Blocks:** [bob-cli-6l.2.1.2](bob-cli-6l.2.1.2.md) ◐ · ⧖ 2026-10-11
- **Blocks:** [bob-cli-6l.2.1.3](bob-cli-6l.2.1.3.md) ◐ · ⧖ 2026-10-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.1/README.md) | [bob-cli-6l.2.1.1](bob-cli-6l.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d513f01`](https://github.com/bobs-org/bob-cli/commit/d513f013bb713434f631f488c00bd531487b1a36) | feat(stats): define engine types, isolated config, and metric registry | [bob-cli-6l.2.1.1](bob-cli-6l.2.1.1.md) | 2026-10-11 08:29:03 EDT |
