# Bead: bob-cli-qq.5 — The \`\_\` dispatch and numbered cabinet pick

[Bead Pages](../README.md) / [bob-cli-qq](README.md) / bob-cli-qq.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6m.linker.w0.md) · **Assignee:** `bob-cli-qq.5` · **Size:** medium
**Created:** 2026-11-26 16:09:02 EST · **Closed:** 2026-11-26 20:53:20 EST
**Plan:** [202611/property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_cabinets.md)

## Description

keys: route `_` to the details fold (zero extras), a direct toggle (one), or an armed pick (two or more). The pick uses a Scope plus a capture listener, and snapshots semantic kinds. It lights the on-card digits and the footer overlay. `__` toggles 1 and `-` toggles Properties; Esc, `q`, and Ctrl+[ cancel. Disarm triggers and palette parity are included.

## Notes

[2026-11-27T01:53:20Z · bob-cli-qq.5] qq.5 keys implemented in bob-plugins: new 240wm pick state machine (0/1/2+ routing, Scope+capture listener, semantic snapshot, 150ms footer overlay, badges via PaintPick, Esc/q/Ctrl-[ cancel, __/- handling, out-of-range nudge, repaint/vanish guards, palette parity, unload release) with 248m dispatch hunks; exports/fragments/manifest 1.172.0/test wired. Verified: npm run build exit 0, build:check exit 0, focused suites 137 pass incl 6 new cabinets-keys tests, epic-symbols clean, bob plugins sync up-to-date (workspace changes uncommitted for land).

## Dependencies

- **Depends on:** [bob-cli-qq.2](bob-cli-qq.2.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qq.4](bob-cli-qq.4.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qq.8](bob-cli-qq.8.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.5/README.md) | [bob-cli-qq.5](bob-cli-qq.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5e2c0bd`](https://github.com/bobs-org/bob-plugins/commit/5e2c0bd54aaeb8c6fe4012f36277f0ace0fb0bde) | feat(cabinets): add numbered cabinet pick and \_ dispatch | [bob-cli-qq.5](bob-cli-qq.5.md) | 2026-11-26 20:54:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qq.5][1] | Need full phase scope, notes, and design links | 2 |
| read-by | [agent:bob-cli-qq.7][2] | list epic children statuses | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.7/README.md

<!-- sase:referenced-by:end -->
