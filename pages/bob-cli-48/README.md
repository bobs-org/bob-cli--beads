# Bead: bob-cli-48 — PRE and POST checklist tiers around the \]s morning walk, with the freshness trial removed

[Bead Pages](../README.md) / bob-cli-48

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.07.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.07.linker.w1.md) · **Assignee:** `bob-cli-48.land`
**Created:** 2026-10-04 09:05:22 EDT · **Closed:** 2026-10-04 11:43:50 EDT
**Plan:** [202610/gtd\_pre\_post\_review\_tiers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gtd_pre_post_review_tiers.md)

## Description

The ]s walk opens with every open, actionable-today #gtd #pre task (the gtd_daily.md chores) and closes with the #gtd #post Morning review. Bryan resolves each of those rows by completing it in the walk, and checking Morning review last certifies the review. No doc, vault note, decision record, or bead waits on a freshness trial any more.

## Notes

[2026-10-04T15:43:35Z · bob-cli-48.land] DISCOVERED ISSUE (land, verification gate carried forward from bob-cli-48.6 note #1/#2): the MacBook still runs pre-epic plugins (last inspected: ledger 1.28.2, nav 2.2.1; cycler already 1.24.0). Custom plugins are gitignored in the vault, and per docs/vault-git-sync.md 'Custom plugins' they deploy on the Mac only by running 'ssh mac bob plugins sync' by hand. The land run's SSH to kellys-macbook-pro timed out again (the Mac is offline with its lid closed), so no agent can finish this now. It is safe to wait: older plugins skip recurring #gtd rows, so the Mac simply does not show PRE/POST. The plan's completion rule accepts checks recorded as a gate, so no task bead was filed, and no catalog task type fits a manual deploy. Remaining when the Mac is on: run 'ssh mac bob plugins sync', reload Obsidian, then do the GUI walk checks listed in bob-cli-48.6 note #1.

[2026-10-04T15:43:50Z · bob-cli-48.land] Landed. Step 1: read all six closed phases and their notes, then checked the code. bob-cli has the trial removal and decision amendments (354b5ae), schema 9 PRE/POST (f873b7b; CL1-CL12 and the nine-tier test in state_tests.rs, the checklist CLI fixture), and the ritual docs (b1e8d30). bob-plugins has cycler 1.24.0 (c8ec83f, API v2 completeTaskAtCursor), ledger 1.29.0 (d5584a0, namespace v7 checklistTiers), and nav 2.3.0 (252ec0e: gates, text-first cursor, day-scoped anchor, complete-and-advance, batch skips). On master b1e8d30, cargo fmt and cargo test pass. just all stops only at the pre-existing pomodoro_name.rs:808 clippy deny, which bob-cli-28 owns. bob-plugins build:check, npm test 1792/1792, and validate 6/6 all pass, and the three plugins in ~/bob are byte-identical to source. Installed bob reports schema 9 with pre_due 7 and post_due 1 in gtd_daily file order, PRE first and POST last, with no checklist lints. The vault tags, the Morning review closeout, the rotten.md tally removal, and the bob-cli-3h wake note are all in place, and no trial references remain beyond the deliberate ones. Step 2: reviewed the concurrent work. bob-cli: b13f96c/192e8b5/76df6b6 (command tree; the epic's docs use canonical names) and b5a8ac2 (Ctrl+[ docs). bob-plugins: c1762af/5d074dc/b854201/cd89f31 (fragment and test splits; nav phase edited fragments, cycler tests kept in test-task-status-cycler-task-links-api.cjs), 31e5c0e (Ctrl+[ survives in nav 2.3.0), 5b476ad (ledger 1.28.2 perf, included in 1.29.0), and 0e6620a. None conflicts with the epic, and no code change was needed. Follow-ups: the clippy deny from .1 and .3 went to epic bob-cli-28 as a DISCOVERED ISSUE note, not a task, since its closeout owns it. The ranker flake from .2, .4, and .5 got a +1 on bob-cli-3w. The Mac plugin deploy from .6 is recorded as a gate on this epic (Mac offline; deploy is manual; old plugins are inert) along with the GUI walk checks from .6 note #1; no task, since no type fits a manual deploy. bob-cli-3y got a note: this epic's amendment now covers its walk-order item. No --epic-symbol entries.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-48.1](bob-cli-48.1.md) | Remove the freshness trial and tag the gtd\_daily.md chores | ✓ closed | small | 2026-10-04 | 1 | 1 |
| [bob-cli-48.2](bob-cli-48.2.md) | task-status-cycler completion API v2 | ✓ closed | small | 2026-10-04 | 1 | 1 |
| [bob-cli-48.3](bob-cli-48.3.md) | Checklist tier contract and the Rust evaluator (schema 9) | ✓ closed | medium | 2026-10-04 | 1 | 1 |
| [bob-cli-48.4](bob-cli-48.4.md) | bob-ledger-tools checklist tiers (freshness namespace v7) | ✓ closed | medium | 2026-10-04 | 1 | 1 |
| [bob-cli-48.5](bob-cli-48.5.md) | Navigation walk support, complete-and-advance, and text-first cursor identity | ✓ closed | medium | 2026-10-04 | 1 | 1 |
| [bob-cli-48.6](bob-cli-48.6.md) | Ritual rewrite, deploy, and live verification | ✓ closed | small | 2026-10-04 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-48: PRE and POST checklist tiers around the ]s morning walk, with the freshness trial removed [closed]"]
    n1["bob-cli-48.1: Remove the freshness trial and tag the gtd_daily.md chores [closed]"]
    n2["bob-cli-48.2: task-status-cycler completion API v2 [closed]"]
    n3["bob-cli-48.3: Checklist tier contract and the Rust evaluator (schema 9) [closed]"]
    n4["bob-cli-48.4: bob-ledger-tools checklist tiers (freshness namespace v7) [closed]"]
    n5["bob-cli-48.5: Navigation walk support, complete-and-advance, and text-first cursor identity [closed]"]
    n6["bob-cli-48.6: Ritual rewrite, deploy, and live verification [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n3
    n2 -.-> n5
    n2 -.-> n6
    n3 -.-> n4
    n3 -.-> n6
    n4 -.-> n5
    n4 -.-> n6
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-48.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-48.1/README.md) | [bob-cli-48.1](bob-cli-48.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-48.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-48.2/README.md) | [bob-cli-48.2](bob-cli-48.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-48.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-48.3.md) | [bob-cli-48.3](bob-cli-48.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-48.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-48.4/README.md) | [bob-cli-48.4](bob-cli-48.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-48.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-48.5/README.md) | [bob-cli-48.5](bob-cli-48.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-48.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-48.6/README.md) | [bob-cli-48.6](bob-cli-48.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-48.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-48.land/README.md) | [bob-cli-48](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c8ec83f`](https://github.com/bobs-org/bob-plugins/commit/c8ec83fae6a094a5c3762418200e2e5b91f4e0f3) | feat(task-status-cycler): add completeTaskAtCursor API v2 | [bob-cli-48.2](bob-cli-48.2.md) | 2026-10-04 09:21:55 EDT |
| bob-cli | [`354b5ae`](https://github.com/bobs-org/bob-cli/commit/354b5ae5e57beeb1d68f52ca3508dc6f21a1c4c4) | docs(freshness): remove trial gates and tag daily checklist chores | [bob-cli-48.1](bob-cli-48.1.md) | 2026-10-04 09:22:47 EDT |
| bob-cli | [`f873b7b`](https://github.com/bobs-org/bob-cli/commit/f873b7b6d6d3d6ee4f8bed8d698e4f7969ae589b) | feat(freshness): add PRE/POST checklist tiers (schema 9) | [bob-cli-48.3](bob-cli-48.3.md) | 2026-10-04 09:53:01 EDT |
| bob-plugins | [`bob-plugins@d5584a0`](https://github.com/bobs-org/bob-plugins/commit/d5584a088cc6ae45228649cf185fab2b08822136) | feat(bob-ledger-tools): add PRE/POST checklist tiers | [bob-cli-48.4](bob-cli-48.4.md) | 2026-10-04 10:32:53 EDT |
| bob-plugins | [`bob-plugins@252ec0e`](https://github.com/bobs-org/bob-plugins/commit/252ec0ecbd59fd604cbfa0f76b88e60219d9cc91) | feat(navigation): teach PRE/POST review walk complete-and-advance | [bob-cli-48.5](bob-cli-48.5.md) | 2026-10-04 11:08:45 EDT |
| bob-cli | [`b1e8d30`](https://github.com/bobs-org/bob-cli/commit/b1e8d30e92270986672b8e7e89055f56e1382eeb) | docs(freshness): rewrite morning ritual for PRE/POST closeout | [bob-cli-48.6](bob-cli-48.6.md) | 2026-10-04 11:30:38 EDT |
| bob-cli--plans | [`bob-cli--plans@23d1b79`](https://github.com/bobs-org/bob-cli--plans/commit/23d1b790081ec34c04aaa573673fbeea63a235cd) | chore(plans): mark gtd\_pre\_post\_review\_tiers done after bob-cli-48 lands | [bob-cli-48](README.md) | 2026-10-04 11:44:37 EDT |
