# Bead: bob-cli-56.2 — bob-navigation-hotkeys Task Link lane toggle and api.taskLinkLane

[Bead Pages](../README.md) / [bob-cli-56](README.md) / bob-cli-56.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5j](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5j.md) · **Assignee:** `bob-cli-56.2` · **Size:** medium
**Created:** 2026-10-07 10:18:29 EDT · **Closed:** 2026-10-07 10:39:49 EDT
**Plan:** [202610/in\_progress\_task\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/in_progress_task_link_marks.md)

## Description

link-lane-toggle: build the two-state Next <-> In Progress toggle for Pomodoro Task Links on the Alt+N link pipeline (matcher, start-wins batch planner, a styled optional Work Log prompt, preimage-checked commit, notices, progressMarks hint) and expose it as nav `api.taskLinkLane` v1, with tests L1-L15.

## Notes

[2026-10-07T14:39:40Z · bob-cli-56.2] PROPOSED FOLLOW-UP: bob plugins sync defaults to ~/projects/github/bobs-org/bob-plugins and git-pulls it, so running it bare from a linked SASE worktree reverts sibling phases vault deployments (here it rolled vault ledger-tools 1.34.0 back to 1.33.0; restored from the sync backup and redeployed nav-only with --repo/-p) — consider documenting --repo/-p sync for concurrent phase workers

[2026-10-07T14:39:49Z · bob-cli-56.2] nav api.taskLinkLane v1 shipped (manifest 2.12.0): 245 core (matches/decide/plan/notice/prompt-state), allowClosed resolver, 196 Move-to-Next modal + bob-tll styles, 525 orchestration + api wiring. Verified: new suite 31/31 (L1-L15), full npm test 2136/0, validate 6/6, nav-only vault sync; sibling ledger-tools 1.34.0 vault deployment restored byte-identical after a bare sync reverted it

## Dependencies

- **Blocks:** [bob-cli-56.3](bob-cli-56.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-56.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-56.2/README.md) | [bob-cli-56.2](bob-cli-56.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@936fec4`](https://github.com/bobs-org/bob-plugins/commit/936fec4621fb6c2c846247be3fb3e23bb7cd2d45) | feat(nav): Pomodoro Task Link Next/In Progress lane toggle with api.taskLinkLane v1 | [bob-cli-56.2](bob-cli-56.2.md) | 2026-10-07 10:42:34 EDT |
