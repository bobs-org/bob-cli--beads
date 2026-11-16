# Bead: bob-cli-mc.4 — Digits in the Ctrl+W prefix, palette commands, go live

[Bead Pages](../README.md) / [bob-cli-mc](README.md) / bob-cli-mc.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4y.linker.w0.md) · **Assignee:** `bob-cli-mc.4` · **Size:** medium
**Created:** 2026-11-16 11:01:02 EST · **Closed:** 2026-11-16 13:03:34 EST
**Plan:** [202611/obsidian\_ctrl\_w\_numbered\_tab\_jump.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_numbered_tab_jump.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:01c4b6734c1d0581a8faaa73 | attached via sase artifact create --bead |
| related | file:explicit:22ddba1181ce676acfa6f0c5 | attached via sase artifact create --bead |
| related | file:explicit:2b653daca9b7a99760fa4c25 | attached via sase artifact create --bead |
| related | file:explicit:53c812ebb3141af90edcb666 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

prefix: wire digits into the Ctrl+W state machine with an armed-catalog freeze, light the numerals with the card, flash on success, add Jump to tab 1–9 commands, flip the dormant seams, bump the minor version, and prove it on real Obsidian.

## Notes

[2026-11-16T18:03:10Z · bob-cli-mc.4] GO LIVE: athena xvfb-run /snap/bin/obsidian --only tabs 31/31 PASS (pass=true, skipped=0). Report file:explicit:22ddba1181ce676acfa6f0c5 plugin 2.85.0 (minor after landed walk-mode 2.84.0). Prefix: Ctrl+W 4 → [ WP-A  WP-B' ] | [ WP-C  WP-D* ]; Ctrl+W Ctrl+3 global WP-C* (not group-local E); Numpad 2 → WP-B*; blocked 7+Esc identical; 0 and Shift+# consumed; already-here 2 unchanged; DOM parity 9 numbered / 4 unnumbered; open left tab WP-C 3→4; L renumber WP-A=1 WP-C=2 WP-B=3; sidebar keeps numerals; single tab none; lit with card gone after Esc; flash on WP-D ~220ms; Linux idle hide + Ctrl+W closed 2→1. Screenshots idle/lit/flash file:explicit:01c4b6734c1d0581a8faaa73 file:explicit:53c812ebb3141af90edcb666 file:explicit:2b653daca9b7a99760fa4c25. bob plugins sync copied manifest+main.js+styles.css 2.85.0.

[2026-11-16T18:03:34Z · bob-cli-mc.4] Verified: digits map in normalizeWindowPrefixKeydown (held-Ctrl, numpad; 0/# unmapped; Cmd+3 pass-through cancel); armed-catalog freeze + arm-generation isCurrent; focus-tab dispatch with lit/unlit/flash/blocked/stale/superseded/fluent; palette window-jump-tab-1..9 no hotkeys; stamper onload + tabNumbers:true + Linux defaultPrevented refresh; nav 2.85.0; unit 66 pass; athena xvfb --only tabs 31/31 PASS (file:explicit:22ddba1181ce676acfa6f0c5); bob plugins sync copied 2.85.0. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-mc.2](bob-cli-mc.2.md) ✓ · ⧖ 2026-11-16
- **Depends on:** [bob-cli-mc.3](bob-cli-mc.3.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mc.5](bob-cli-mc.5.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mc.4/README.md) | [bob-cli-mc.4](bob-cli-mc.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@91e9097`](https://github.com/bobs-org/bob-plugins/commit/91e909791a86fa30bba0b8b11c712e03a80e4dd4) | feat(navigation): ship Ctrl+W numbered tab jump 2.85.0 | [bob-cli-mc.4](bob-cli-mc.4.md) | 2026-11-16 13:04:58 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mc.4][1] | Need full description, notes, design file, and DECISIONS | 8 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mc.4/README.md

<!-- sase:referenced-by:end -->
