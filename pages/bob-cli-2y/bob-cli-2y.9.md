# Bead: bob-cli-2y.9 — Alt+N commits or releases a lane; #now leaves Bob Navigation Hotkeys

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.9` · **Size:** medium
**Created:** 2026-09-30 16:42:00 EDT · **Closed:** 2026-09-30 18:04:48 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

release-key: retarget Alt+N and the Ctrl+Shift+P pinned row from the #now toggle to commit (Ready to Next) and release (Next/In Progress to Ready, unlinking today), and delete every #now path.

## Notes

[2026-09-30T22:04:48Z · bob-cli-2y.9] Alt+N now commits Ready to Next / releases Next+Pending to Ready with today-link prune and optional Work Log prompt; #now paths deleted (rg clean); npm test 873 pass, validate 6/6, manifest 1.42.0, README updated, Work Log strand updated, hotkeys.json has no toggle-now-tag binding, plugin synced to vault

## Dependencies

- **Blocks:** [bob-cli-2y.10](bob-cli-2y.10.md) ◐ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.7](bob-cli-2y.7.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.8](bob-cli-2y.8.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.9/README.md) | [bob-cli-2y.9](bob-cli-2y.9.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`473cca3`](https://github.com/bobs-org/bob-cli/commit/473cca3e0882e0fd73156a45cfbd235f97b682d4) | docs(memory): Alt+N release prompts for the Work Log summary | [bob-cli-2y.9](bob-cli-2y.9.md) | 2026-09-30 18:07:05 EDT |
| bob-plugins | [`bob-plugins@053a076`](https://github.com/bobs-org/bob-plugins/commit/053a07640a26d2f44c71c0e0774efa8af25eacf5) | feat(nav-hotkeys): Alt+N commits or releases the lane; #now removed | [bob-cli-2y.9](bob-cli-2y.9.md) | 2026-09-30 18:07:37 EDT |
