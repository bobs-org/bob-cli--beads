# Bead: bob-cli-an.6.6.6.5.6.5.5.4 — Stop the stage ranker 16 ms assertion from flaking under parallel npm test

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) / bob-cli-an.6.6.6.5.6.5.5.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.4` · **Size:** small
**Created:** 2026-10-25 07:49:26 EDT · **Closed:** 2026-10-25 07:59:37 EDT
**Plan:** [202610/backlog\_batch8\_listen\_manifest\_mac\_ci\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch8_listen_manifest_mac_ci_flakes.md)

## Description

plugin-ranker-flake: resolve bob-cli-3w in bob-plugins by measuring a warmed ranker over several runs while still failing a real slowdown.

## Notes

[2026-10-25T11:59:37Z · bob-cli-an.6.6.6.5.6.5.5.4] Warmed the 1000-task stage-ranker assertion to best-of-7 after 3 JIT warmups (same 16ms budget). Verified: file alone 23/23; full npm test 3648/3648 three times (last two under 8-core busy-loop load); npm run validate exit 0; slowdown probe shows normal warmed min ~1.5ms (10x headroom) while a +25ms/call regression fails every sample. Test-only change in scripts/, no plugin source touched, no sync needed. bob-cli-3w left open for the lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.4](bob-cli-an.6.6.6.5.6.5.5.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ab71502`](https://github.com/bobs-org/bob-plugins/commit/ab7150284f726e54a4442d455ba0c11d81433d56) | test(nav): de-flake 1000-task stage-ranker 16ms budget with warmed best-of-7 timing | [bob-cli-an.6.6.6.5.6.5.5.4](bob-cli-an.6.6.6.5.6.5.5.4.md) | 2026-10-25 08:00:14 EDT |
