# Bead: bob-cli-2y.5 — Define Today once; NEXT/PENDING lanes replace NOW in bob plan and the hooks

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.5` · **Size:** medium
**Created:** 2026-09-30 16:42:00 EDT · **Closed:** 2026-09-30 17:30:28 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

today-core: Rust Today engine with conformance vectors in docs/plan.md, lane meters and caps replacing NOW, bob plan JSON schema 2 with today_tasks, and the hooks plan_budget line.

## Notes

[2026-09-30T21:30:11Z · bob-cli-2y.5] PROPOSED FOLLOW-UP: cargo clippy --all-targets deny-error clippy::logic_bug at tests/cli/capture/pomodoro_name.rs:808 (|| true) fails on the clean base tree too (untouched file, also recorded on bob-cli-2y.2); blocks clippy-gated just lint, not cargo test

[2026-09-30T21:30:28Z · bob-cli-2y.5] today-core done: new Today engine (today_links/today_tasks, T1-T9 vectors in docs/plan.md + 9 unit tests), NEXT/PENDING lane queries + count_lanes replacing NOW, plan JSON schema 2 (today/today_tasks/next/pending, max_next/max_pending), human TODAY section + hooks plan line, config max_now ignored-compat, README + hooks docs updated. Verified: cargo test full suite green (1344 lib + 652 CLI incl. rewritten tests/cli/plan.rs lane/Today/schema-2 tests + hooks plan-budget test), cargo fmt clean. Pre-existing clippy deny-error at untouched tests/cli/capture/pomodoro_name.rs:808 recorded as follow-up (fails on clean base too).

## Dependencies

- **Depends on:** [bob-cli-2y.2](bob-cli-2y.2.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2y.6](bob-cli-2y.6.md) ◐ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2y.7](bob-cli-2y.7.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.5/README.md) | [bob-cli-2y.5](bob-cli-2y.5.md) | 0 |
