# Bead: bob-cli-2o — Close the day, tag the week: plan budget, #now, and ledger guardrails

[Bead Pages](../README.md) / bob-cli-2o

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.land`
**Created:** 2026-09-29 18:09:56 EDT · **Closed:** 2026-09-29 23:28:12 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

Today's Pomodoro plan is a visible, capped, closed list (GTD + 3 themes, about 10 Task Links) and this week's bets live in a `#now` tag. One shared budget definition shows the same numbers in `bob plan`, task-status-hooks, tmux, `bob capture`, Bob Mac Capture, and Obsidian. New gestures let Bryan drop, defer, and tag work from the ledger itself, and nothing rewrites the plan behind Bryan's back.

## Notes

[2026-09-30T02:33:45Z · bob-cli-2o.land] FOLLOW-UP TRIAGE (bob-cli-2o.land): (1) clippy deny at tests/cli/capture/pomodoro_name.rs:808 ('|| true', overly_complex_bool_expr), proposed by .1/.3/.4/.5/.6/.9/.13: not caused by this epic (bob-cli-28.1 via 7d1c8dd); routed via /sase_new_task as a DISCOVERED ISSUE corroboration note on active epic bob-cli-28, whose closeout owns it; no task created. (2) Pre-existing clippy warnings (.9 cites pomodoro_shift.rs:581): +1 on bob-cli-v with the current count; exactly one warning comes from this epic (manual_contains, capture_complete.rs:1372, 35b96b3), and the closeout tale fixes it. (3) Vault missing bob-project-tasks/bob-vim-surround/task-status-cycler (.7): declined, already resolved: rollout's full bob plugins sync deployed all six bob-plugins; verified present in ~/bob/.obsidian/plugins. (4) System TZ Etc/UTC flips bob's day at 20:00 EDT (.13): not caused by this epic (env.rs current_datetime uses Local::now); new task bob-cli-2q (bug, medium). (5) Landing observation, not proposed by any phase: src/native/capture_complete.rs is 3790 lines, and it was already 2938 before this epic. Declined as a separate task; the tale splits the files this epic pushed past ~1500 lines (config.rs, tests/cli/capture/parse_pomodoro.rs).

[2026-09-30T03:28:12Z · bob-cli-2o.land] Closed by explicit `sase stitch create -B close` after create_commit landed 25c1b2f ("feat(plan): land bob-cli-2o closeout - config isolation, ledger parity, capture guards, docs"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-2o` if more work remains.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-2o.1](bob-cli-2o.1.md) | bob-cli: shared plan-budget core, config block, and \`bob plan\` | ✓ closed | medium | 2026-09-29 | 1 | 1 |
| [bob-cli-2o.10](bob-cli-2o.10.md) | bob-plugins: plan budget in the Ctrl+Shift+Enter Notice | ✓ closed | small | 2026-09-29 | 1 | 1 |
| [bob-cli-2o.11](bob-cli-2o.11.md) | Bob Mac Capture: plan budget meter, destination row, and create-row cap badge | ✓ closed | medium | 2026-09-29 | 1 | 0 |
| [bob-cli-2o.12](bob-cli-2o.12.md) | Bob Mac Capture: drop outcome, \`#now\` token, and NOW badges | ✓ closed | medium | 2026-09-29 | 1 | 0 |
| [bob-cli-2o.13](bob-cli-2o.13.md) | Rollout: PLAN chip, daily template block, config knobs, install, and end-to-end check | ✓ closed | small | 2026-09-29 | 1 | 0 |
| [bob-cli-2o.2](bob-cli-2o.2.md) | Vault: NOW chip, NOW section, and the gtd\_daily chore swap | ✓ closed | small | 2026-09-29 | 1 | 0 |
| [bob-cli-2o.3](bob-cli-2o.3.md) | bob-cli: plan budget in task-status-hooks and the tmux segment | ✓ closed | small | 2026-09-29 | 1 | 1 |
| [bob-cli-2o.4](bob-cli-2o.4.md) | bob-cli: capture plan-budget warnings, strict mode, and implicit destination | ✓ closed | medium | 2026-09-29 | 1 | 1 |
| [bob-cli-2o.5](bob-cli-2o.5.md) | bob-cli: \`~\<K\>\` drop outcome for \`=x\` closes | ✓ closed | medium | 2026-09-29 | 1 | 1 |
| [bob-cli-2o.6](bob-cli-2o.6.md) | bob-cli: first-class \`#now\` in capture | ✓ closed | medium | 2026-09-29 | 1 | 1 |
| [bob-cli-2o.7](bob-cli-2o.7.md) | bob-plugins: Bob Ledger Tools plan view, \`bob-plan\` block, and public API | ✓ closed | medium | 2026-09-29 | 1 | 1 |
| [bob-cli-2o.8](bob-cli-2o.8.md) | bob-plugins: Ctrl+Shift+P edits the task behind a Task Link | ✓ closed | medium | 2026-09-29 | 1 | 1 |
| [bob-cli-2o.9](bob-cli-2o.9.md) | bob-plugins: toggle #now from task lines and Task Links | ✓ closed | medium | 2026-09-29 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-2o: Close the day, tag the week: plan budget, #now, and ledger guardrails [closed]"]
    n1["bob-cli-2o.1: bob-cli: shared plan-budget core, config block, and `bob plan` [closed]"]
    n2["bob-cli-2o.10: bob-plugins: plan budget in the Ctrl+Shift+Enter Notice [closed]"]
    n3["bob-cli-2o.11: Bob Mac Capture: plan budget meter, destination row, and create-row cap badge [closed]"]
    n4["bob-cli-2o.12: Bob Mac Capture: drop outcome, `#now` token, and NOW badges [closed]"]
    n5["bob-cli-2o.13: Rollout: PLAN chip, daily template block, config knobs, install, and end-to-end check [closed]"]
    n6["bob-cli-2o.2: Vault: NOW chip, NOW section, and the gtd_daily chore swap [closed]"]
    n7["bob-cli-2o.3: bob-cli: plan budget in task-status-hooks and the tmux segment [closed]"]
    n8["bob-cli-2o.4: bob-cli: capture plan-budget warnings, strict mode, and implicit destination [closed]"]
    n9["bob-cli-2o.5: bob-cli: `~&lt;K&gt;` drop outcome for `=x` closes [closed]"]
    n10["bob-cli-2o.6: bob-cli: first-class `#now` in capture [closed]"]
    n11["bob-cli-2o.7: bob-plugins: Bob Ledger Tools plan view, `bob-plan` block, and public API [closed]"]
    n12["bob-cli-2o.8: bob-plugins: Ctrl+Shift+P edits the task behind a Task Link [closed]"]
    n13["bob-cli-2o.9: bob-plugins: toggle #now from task lines and Task Links [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n1 -.-> n5
    n1 -.-> n7
    n1 -.-> n8
    n1 -.-> n9
    n1 -.-> n11
    n2 -.-> n5
    n3 -.-> n4
    n4 -.-> n5
    n6 -.-> n5
    n7 -.-> n5
    n8 -.-> n3
    n8 -.-> n9
    n9 -.-> n4
    n9 -.-> n10
    n10 -.-> n4
    n10 -.-> n5
    n11 -.-> n2
    n11 -.-> n5
    n11 -.-> n13
    n12 -.-> n13
    n13 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.1/README.md) | [bob-cli-2o.1](bob-cli-2o.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-2o.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.10/README.md) | [bob-cli-2o.10](bob-cli-2o.10.md) | 1 |
| [bbugyi200.apollo.bob-cli-2o.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2o.11.md) | [bob-cli-2o.11](bob-cli-2o.11.md) | 0 |
| [bbugyi200.apollo.bob-cli-2o.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.12/README.md) | [bob-cli-2o.12](bob-cli-2o.12.md) | 0 |
| [bbugyi200.apollo.bob-cli-2o.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.13/README.md) | [bob-cli-2o.13](bob-cli-2o.13.md) | 0 |
| [bbugyi200.apollo.bob-cli-2o.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.2/README.md) | [bob-cli-2o.2](bob-cli-2o.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-2o.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.3/README.md) | [bob-cli-2o.3](bob-cli-2o.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-2o.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.4/README.md) | [bob-cli-2o.4](bob-cli-2o.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-2o.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.5/README.md) | [bob-cli-2o.5](bob-cli-2o.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-2o.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.6/README.md) | [bob-cli-2o.6](bob-cli-2o.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-2o.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.7/README.md) | [bob-cli-2o.7](bob-cli-2o.7.md) | 1 |
| [bbugyi200.apollo.bob-cli-2o.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.8/README.md) | [bob-cli-2o.8](bob-cli-2o.8.md) | 1 |
| [bbugyi200.apollo.bob-cli-2o.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2o.9.md) | [bob-cli-2o.9](bob-cli-2o.9.md) | 1 |
| [bbugyi200.apollo.bob-cli-2o.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2o.land.md) | [bob-cli-2o](README.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e89f38f`](https://github.com/bobs-org/bob-plugins/commit/e89f38f699df3d31dce035df4c9f1a9926910746) | feat(bob-navigation-hotkeys): task-link property picker with counted batch planning | [bob-cli-2o.8](bob-cli-2o.8.md) | 2026-09-29 18:30:22 EDT |
| bob-cli | [`db89ee8`](https://github.com/bobs-org/bob-cli/commit/db89ee8af0ea3f9830fe2d2b9511f76983daeca4) | feat(plan): add plan config, budget engine, and read-only bob plan command | [bob-cli-2o.1](bob-cli-2o.1.md) | 2026-09-29 18:44:26 EDT |
| bob-plugins | [`bob-plugins@ddc01ac`](https://github.com/bobs-org/bob-plugins/commit/ddc01ac2a81f1b233e5dd6b6981bb52dbae01703) | feat(bob-ledger-tools): plan-budget mirror, live bob-plan block, and versioned api | [bob-cli-2o.7](bob-cli-2o.7.md) | 2026-09-29 19:15:43 EDT |
| bob-cli | [`f481c7a`](https://github.com/bobs-org/bob-cli/commit/f481c7a065f99806018167f6e712de543e5251ad) | feat(hooks-tmux): plan budget in task-status-hooks and the tmux segment | [bob-cli-2o.3](bob-cli-2o.3.md) | 2026-09-29 19:19:10 EDT |
| bob-plugins | [`bob-plugins@8557a63`](https://github.com/bobs-org/bob-plugins/commit/8557a63de5c9e664e526080fca6f8c786ad080ee) | feat(block-id-prompt): append plan budget meter to link, unlink, and Task Link Notices | [bob-cli-2o.10](bob-cli-2o.10.md) | 2026-09-29 19:24:05 EDT |
| bob-cli | [`35b96b3`](https://github.com/bobs-org/bob-cli/commit/35b96b3d734e1d21b42905312233e54afbcfc482) | feat(capture): plan-budget warnings, strict mode, and destination roles | [bob-cli-2o.4](bob-cli-2o.4.md) | 2026-09-29 19:33:21 EDT |
| bob-plugins | [`bob-plugins@b68618f`](https://github.com/bobs-org/bob-plugins/commit/b68618ff0347c34c4b58086c490278110ec52f35) | feat(bob-navigation-hotkeys): toggle #now from task lines and Task Links | [bob-cli-2o.9](bob-cli-2o.9.md) | 2026-09-29 19:38:01 EDT |
| bob-cli | [`754d1f3`](https://github.com/bobs-org/bob-cli/commit/754d1f31fe7feffb81c85d4ed55c17888f15a65f) | feat(capture): \`~\<K\>\` drop outcome for \`=x\` closes | [bob-cli-2o.5](bob-cli-2o.5.md) | 2026-09-29 20:11:18 EDT |
| bob-cli | [`d28f8cd`](https://github.com/bobs-org/bob-cli/commit/d28f8cd218bf0e85344a776746e07c23dcfd56be) | feat(capture): first-class #now tag for new tasks | [bob-cli-2o.6](bob-cli-2o.6.md) | 2026-09-29 20:53:49 EDT |
| bob-cli | [`25c1b2f`](https://github.com/bobs-org/bob-cli/commit/25c1b2f2cc2f0af4753c7c52442ce4ebfaf4e920) | feat(plan): land bob-cli-2o closeout - config isolation, ledger parity, capture guards, docs | [bob-cli-2o](README.md) | 2026-09-29 23:27:51 EDT |
| bob-plugins | [`bob-plugins@17fbc09`](https://github.com/bobs-org/bob-plugins/commit/17fbc097fb8599464f16ac635ed1240817e61e55) | feat(ledger): plan-budget closeout parity, render child, live re-render, notices | [bob-cli-2o](README.md) | 2026-09-29 23:28:23 EDT |
| bob-cli--plans | [`bob-cli--plans@33bdf16`](https://github.com/bobs-org/bob-cli--plans/commit/33bdf167372ba47e0dedbf5de48ac9d6674dc878) | chore(plans): mark epic and closeout plans done | [bob-cli-2o](README.md) | 2026-09-29 23:29:06 EDT |
