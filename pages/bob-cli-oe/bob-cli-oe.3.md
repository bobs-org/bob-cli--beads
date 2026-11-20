# Bead: bob-cli-oe.3 — Obsidian landing API, walk follow, and receipt line

[Bead Pages](../README.md) / [bob-cli-oe](README.md) / bob-cli-oe.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5m.linker.w0.md) · **Assignee:** `bob-cli-oe.3` · **Size:** medium
**Created:** 2026-11-20 17:03:14 EST · **Closed:** 2026-11-20 18:05:45 EST
**Plan:** [202611/successor\_jump\_pin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_pin.md)

## Description

nav-jump-landing: add nav `api.landOnTask(target)`, which re-finds the task by identity (never by a clamped line), focuses it, records a Vim jump, and flashes the line. Add reviewWalk v2 `continue(origin, {follow})`, which parks the walk before landing, and a notice v5 `↗ “S”` receipt line.

## Notes

[2026-11-20T23:04:04Z · bob-cli-oe.3] PROPOSED FOLLOW-UP: npm test load-flake of event-link-times 39.6ms and frees-marks 126ms vs 25ms budgets under the full suite; isolated rerun passed on this tree and on clean HEAD 63cd4ee (15.8ms / 21.3ms). Tracked by bob-cli-km and bob-cli-io. docs:check still fails on clean HEAD via docs/reference/vault-format.md 6016/6000 (bob-cli-it); plugin-apis.md stayed under 8000 after tightening.

[2026-11-20T23:05:45Z · bob-cli-oe.3] nav-jump-landing: additive api.landOnTask re-finds by identity (planned/block-id/unique text/unique description, never clamps), records a Vim jump, flashes, and leaves the ]s walk. reviewWalk v2 continue(origin,{follow}) parks then lands with one composed toast and holds the lock until landing; stale/off-landing still lands; without follow, v1 is unchanged. notice v5 appends a trailing ↗ “S” receipt. Plugin 2.94.0, docs/develop/plugin-apis.md updated, vault synced. npm test: 7980 pass; two load-flakes (event-link-times 39.6ms, frees-marks 126ms vs 25ms) pass in isolation on this tree and on clean HEAD 63cd4ee — cited bob-cli-km and bob-cli-io. docs:check fails on clean HEAD via vault-format.md 6016/6000 (bob-cli-it); plugin-apis.md stayed under 8000.

## Dependencies

- **Depends on:** [bob-cli-oe.2](bob-cli-oe.2.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-oe.4](bob-cli-oe.4.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.3/README.md) | [bob-cli-oe.3](bob-cli-oe.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1a6ff79`](https://github.com/bobs-org/bob-plugins/commit/1a6ff799afb94108c7cca87593b3d3e15cbb1bd8) | feat(nav): add landOnTask, reviewWalk v2 follow, and notice v5 jump receipt | [bob-cli-oe.3](bob-cli-oe.3.md) | 2026-11-20 18:07:09 EST |
