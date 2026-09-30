# Bead: bob-cli-2o.6 — bob-cli: first-class \`#now\` in capture

[Bead Pages](../README.md) / [bob-cli-2o](README.md) / bob-cli-2o.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.6` · **Size:** medium
**Created:** 2026-09-29 18:09:56 EDT · **Closed:** 2026-09-29 20:48:21 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

now-token: accept `#now` after the route marker, color it with a `now_tag` span, complete a partial `#n`/`#no` to `#now`, and list Ready `#now` tasks (flagged `now`) in the `^` active-task picker.

## Notes

[2026-09-30T00:48:00Z · bob-cli-2o.6] PROPOSED FOLLOW-UP: clippy deny failure in tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr, `|| true`) reproduces identically on the clean base tree and keeps `just all` red; no task bead tracks it yet

[2026-09-30T00:48:21Z · bob-cli-2o.6] now-token done: trailing #now resolves route then moves to body end (writes '- [ ] #task <body> #now [created::..] ^id'); #now before route works; solo-link/toggle/operator+#now is the Alt+N usage error; now_tag spans + #n/#no Incomplete(needs now_tag); capture-complete now_tag single candidate; ^ picker lists Ready #now after Next with now flag; docs/capture.md updated; cargo test all green (1257 lib + 590 cli), fmt clean, clippy failure pre-existing on base (recorded as follow-up)

## Dependencies

- **Blocks:** [bob-cli-2o.12](bob-cli-2o.12.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.13](bob-cli-2o.13.md) ◐ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.5](bob-cli-2o.5.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.6/README.md) | [bob-cli-2o.6](bob-cli-2o.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d28f8cd`](https://github.com/bobs-org/bob-cli/commit/d28f8cd218bf0e85344a776746e07c23dcfd56be) | feat(capture): first-class #now tag for new tasks | [bob-cli-2o.6](bob-cli-2o.6.md) | 2026-09-29 20:53:49 EDT |
