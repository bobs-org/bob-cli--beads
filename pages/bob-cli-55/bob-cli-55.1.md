# Bead: bob-cli-55.1 — bob-cli rename, schema 10, and docs

[Bead Pages](../README.md) / [bob-cli-55](README.md) / bob-cli-55.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5i](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5i.md) · **Assignee:** `bob-cli-55.1` · **Size:** medium
**Created:** 2026-10-07 09:55:36 EDT · **Closed:** 2026-10-07 10:07:40 EDT
**Plan:** [202610/review\_footer\_short\_labels\_tickler.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/review_footer_short_labels_tickler.md)

## Description

cli-tickler: rename the Rust returned walk tier to tickler (TICKLER in human output), bump bob freshness JSON to schema 10, update tests and the D4 fixture vector, and document the tickler tier, the WIP alias, and the footer short labels in bob-cli docs and README.

## Notes

[2026-10-07T14:07:19Z · bob-cli-55.1] PROPOSED FOLLOW-UP: clippy logic-bug error in tests/cli/capture/pomodoro_name.rs:808 (|| true) fails just lint identically on clean base

[2026-10-07T14:07:24Z · bob-cli-55.1] PROPOSED FOLLOW-UP: lib test completion::kinds::every_value_arg_has_a_decision fails identically on clean base (ref create:audio lacks kinds decision)

[2026-10-07T14:07:29Z · bob-cli-55.1] PROPOSED FOLLOW-UP: real-vault freshness list fails in this env with Tasks JS sandbox init interrupted error, identically on clean base; verified tickler output on fixture vault instead

[2026-10-07T14:07:40Z · bob-cli-55.1] Renamed Returned tier to Tickler (Tier::Tickler, by_tier.tickler, TICKLER output), schema 9->10, D4-tickler vector, docs+README WIP alias and footer short labels. Verified: cargo fmt ok, 111 lib + 43 CLI freshness tests pass, fixture-vault list shows tickler/TICKLER and JSON schema 10 with tickler key, rg leaves only unrelated English + intentional schema-10/v8 rename notes. just-lint clippy error, one completion-kinds test, and real-vault sandbox failure all reproduce identically on clean base (recorded as follow-ups).

## Dependencies

- **Blocks:** [bob-cli-55.3](bob-cli-55.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-55.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-55.1/README.md) | [bob-cli-55.1](bob-cli-55.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e5d12ca`](https://github.com/bobs-org/bob-cli/commit/e5d12ca4407baca64a859f89402d2d245dea5582) | feat(freshness): rename Returned walk tier to Tickler, schema 10 | [bob-cli-55.1](bob-cli-55.1.md) | 2026-10-07 10:08:58 EDT |
