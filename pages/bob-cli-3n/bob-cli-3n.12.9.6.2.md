# Bead: bob-cli-3n.12.9.6.2 — Fix the mirror owner lookup, the waits-on badge, and the remaining stale refusals

[Bead Pages](../README.md) / [bob-cli-3n.12.9.6](bob-cli-3n.12.9.6.md) / bob-cli-3n.12.9.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.9.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.9.land.md) · **Assignee:** `bob-cli-3n.12.9.6.2` · **Size:** medium
**Created:** 2026-10-03 02:54:24 EDT · **Closed:** 2026-10-03 03:28:46 EDT
**Plan:** [202610/task\_dep\_links\_landing\_remaining.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_remaining.md)

## Description

nav-mirror-stage-fixes: resolve the hand-edit mirror owner in baseline coordinates, stop the stage showing "waits on 0", route the cross-note batch and counted vault stale paths through refuseDependencyStale, and make the stage tests drive the real write and marking paths.

## Notes

[2026-10-03T07:28:46Z · bob-cli-3n.12.9.6.2] nav-mirror-stage-fixes done in bob-plugins (nav 1.63.0, deployed to vault). Mirror owner resolved in burst-baseline coords and mapped forward (edited/owner/baseline lines separated in snapshot); badge counts open prereqs from own Depends-On line with waits-on only for N>=1 else scheduled-date else blocked (contract S6 updated); cross-note batch, counted-vault ref, and stale vault-commit writes refuse via refuseDependencyStale with nothing written; same-note batches guard post-batch cycles; stage tests drive real write/marking paths and addCommand capture. Verified: npm test 1380/1380, validate 6/6, stage suite 46/46 (37 pass pre-fix with exactly the 9 expected failures: 2 mirror bursts, 3 badges, 3 stale paths, 1 cycle guard), bob-cli fmt+clippy clean with tests 1560 pass plus the known bob-cli-2e capture_pomodoros flake passing alone, nav 1.63.0 synced to ~/bob. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-3n.12.9.6.1](bob-cli-3n.12.9.6.1.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3n.12.9.6.5](bob-cli-3n.12.9.6.5.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.9.6.2/README.md) | [bob-cli-3n.12.9.6.2](bob-cli-3n.12.9.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`50350db`](https://github.com/bobs-org/bob-cli/commit/50350db0f442696acef0e1d198c2e9fd2ca48f45) | docs(task-deps): state the BLOCKED badge rule in stage S6 | [bob-cli-3n.12.9.6.2](bob-cli-3n.12.9.6.2.md) | 2026-10-03 03:30:09 EDT |
