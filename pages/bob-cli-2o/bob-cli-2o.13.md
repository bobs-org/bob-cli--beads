# Bead: bob-cli-2o.13 — Rollout: PLAN chip, daily template block, config knobs, install, and end-to-end check

[Bead Pages](../README.md) / [bob-cli-2o](README.md) / bob-cli-2o.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.13` · **Size:** small
**Created:** 2026-09-29 18:09:57 EDT · **Closed:** 2026-09-29 22:00:37 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

rollout: switch the dash NOW chip to the API and add the PLAN chip; add the `bob-plan` block to the daily template and to today's note; add the commented `plan:` block to the chezmoi-managed config; reinstall `bob` on apollo and sync the plugins; run an end-to-end check; hand Bryan the manual checklist.

## Notes

[2026-09-30T02:00:05Z · bob-cli-2o.13] E2E (BOB_DAY_FILE=~/bob/2026/20260929.md): bob plan -> PLAN 19/3 themes - 73/10 links, NOW 0/15, status over, exit 0; json caps {3,10,15,false}; tmux-pomodoro -> #[reverse]plan 19/3 x 73/10#[noreverse]; task-status-hooks plan_budget matches; capture dry-run plan_budget before=after + dest role=next_up; capture-parse now_tag span ok; =x1~2 drop outcome ok; vault-sync clean tree, pushed, local==remote 396868ff. just all: fmt ok, cargo test 1267+596+27 pass; clippy deny on untouched tests/cli/capture/pomodoro_name.rs:808 (see follow-up).

[2026-09-30T02:00:16Z · bob-cli-2o.13] PROPOSED FOLLOW-UP: clippy --all-targets fails on clean master at tests/cli/capture/pomodoro_name.rs:808 (deny overly_complex_bool_expr on `|| true` tail); reproduces on untouched tree, blocks `just all` gate

[2026-09-30T02:00:22Z · bob-cli-2o.13] PROPOSED FOLLOW-UP: system TZ is Etc/UTC so Local::now day flips at 8pm EDT; after 8pm bob plan/capture target tomorrow note while vault days are EDT (tonight: said 2026-09-30, real day 2026-09-29); consider TZ-aware or vault-local day selection

[2026-09-30T02:00:37Z · bob-cli-2o.13] Rollout done: dash NOW via ledger-tools api + cyan PLAN chip (awaited async planBudget); bob-plan block in daily template + 20260929 note; plan: defaults in chezmoi source, applied, ~/.config in sync; cargo install ok; plugins sync 7 copied/9 unchanged; e2e all pass (plan/tmux/hooks/capture/parse/vault-sync pushed); cargo test 1890 pass; pre-existing clippy failure recorded as follow-up, reproduces on clean tree

## Dependencies

- **Depends on:** [bob-cli-2o.1](bob-cli-2o.1.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.10](bob-cli-2o.10.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.12](bob-cli-2o.12.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.2](bob-cli-2o.2.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.3](bob-cli-2o.3.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.6](bob-cli-2o.6.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.7](bob-cli-2o.7.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.9](bob-cli-2o.9.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.13/README.md) | [bob-cli-2o.13](bob-cli-2o.13.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@2d048c5`](https://github.com/bbugyi200/dotfiles/commit/2d048c58958271c67e47bea6f23e0479d28e3704) | feat(bob): add commented plan defaults to chezmoi bob config | [bob-cli-2o.13](bob-cli-2o.13.md) | 2026-09-29 22:02:38 EDT |
