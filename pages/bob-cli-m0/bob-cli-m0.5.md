# Bead: bob-cli-m0.5 — Ctrl+W prefix state machine

[Bead Pages](../README.md) / [bob-cli-m0](README.md) / bob-cli-m0.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e9.md) · **Assignee:** `bob-cli-m0.5` · **Size:** medium
**Created:** 2026-11-15 20:01:48 EST · **Closed:** 2026-11-16 08:23:06 EST
**Plan:** [202611/obsidian\_ctrl\_w\_window\_prefix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_window_prefix.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:33a8fb6bd8eea753811de289 | attached via sase artifact create --bead |
| related | file:explicit:55d6a09e11f47cb0ecee0a5d | attached via sase artifact create --bead |
| related | file:explicit:e771d096dd4571d1141e3edb | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

prefix: wire the capture listener, armed keymap scope, arming gate, dispatch, cancel paths, and two-tier hint timing into a reliable Ctrl+W prefix.

## Notes

[2026-11-16T13:23:06Z · bob-cli-m0.5] Ctrl+W prefix mixin wired (687) with capture listeners, Scope, arming gate, dispatch, cancel, 300ms two-tier hint. linux_ctrl_w=keep: Linux bound Ctrl+W stays Close tab. Unit 31/31. Athena --only prefix e2e all pass including Ctrl+W l/h/L/H on [WP-A WP-B*] | [WP-C], toggle, Ctrl+L, Esc identical, unmapped j, insert word-delete, copy-card pass-through, reading view + empty tab arm, pending d, hint ring + card at 300ms, Linux Close idle. Screenshots file:explicit:e771d096dd4571d1141e3edb (ring) and file:explicit:55d6a09e11f47cb0ecee0a5d (card). Nav 2.83.0 synced. Live join/create-split invariants now follow activeLeaf (selectedTab is display-only in Obsidian).

## Dependencies

- **Depends on:** [bob-cli-m0.3](bob-cli-m0.3.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-m0.4](bob-cli-m0.4.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-m0.6](bob-cli-m0.6.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-m0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.5/README.md) | [bob-cli-m0.5](bob-cli-m0.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c725370`](https://github.com/bobs-org/bob-plugins/commit/c72537068ac0601f42069cd8af3f53d928614ba8) | feat(navigation): add Ctrl+W prefix state machine | [bob-cli-m0.5](bob-cli-m0.5.md) | 2026-11-16 08:25:23 EST |
