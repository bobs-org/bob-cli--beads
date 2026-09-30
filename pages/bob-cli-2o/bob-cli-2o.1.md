# Bead: bob-cli-2o.1 — bob-cli: shared plan-budget core, config block, and \`bob plan\`

[Bead Pages](../README.md) / [bob-cli-2o](README.md) / bob-cli-2o.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.1` · **Size:** medium
**Created:** 2026-09-29 18:09:56 EDT · **Closed:** 2026-09-29 18:41:29 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

plan-core: add the `plan:` config block, a pure ledger budget and lint engine, a NOW counter built on the native Tasks engine, the read-only `bob plan` command (human and JSON), and `docs/plan.md` as the authoritative definition with conformance examples.

## Notes

[2026-09-29T22:41:12Z · bob-cli-2o.1] PROPOSED FOLLOW-UP: clippy fails on the clean base tree (tests/cli/capture/pomodoro_name.rs:808 `|| true` tautology is a clippy logic-bug error), so `just lint` is red independent of plan-core; fix or track separately

[2026-09-29T22:41:29Z · bob-cli-2o.1] plan-core done: plan: config block with load_plan_config, pure ledger budget/lint engine (all 7 conformance examples as unit tests), NOW counter via native Tasks engine plus whole-token has_now_tag filter, read-only bob plan human+JSON with exit 0/1/2, docs/plan.md plus README/docs/justfile updates. Verified: cargo test all green (1210 lib incl 15 plan_budget + 4 config, 552 cli incl 8 new plan tests), cargo fmt clean, no new clippy warnings; the one clippy error is pre-existing on the clean base (recorded as PROPOSED FOLLOW-UP). epic-symbols: none.

## Dependencies

- **Blocks:** [bob-cli-2o.13](bob-cli-2o.13.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.3](bob-cli-2o.3.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.4](bob-cli-2o.4.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.5](bob-cli-2o.5.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.7](bob-cli-2o.7.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.1/README.md) | [bob-cli-2o.1](bob-cli-2o.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`db89ee8`](https://github.com/bobs-org/bob-cli/commit/db89ee8af0ea3f9830fe2d2b9511f76983daeca4) | feat(plan): add plan config, budget engine, and read-only bob plan command | [bob-cli-2o.1](bob-cli-2o.1.md) | 2026-09-29 18:44:26 EDT |
