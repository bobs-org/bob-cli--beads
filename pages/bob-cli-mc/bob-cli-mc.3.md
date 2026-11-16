# Bead: bob-cli-mc.3 — Tab numerals, card tabs row, and previews

[Bead Pages](../README.md) / [bob-cli-mc](README.md) / bob-cli-mc.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4y.linker.w0.md) · **Assignee:** `bob-cli-mc.3` · **Size:** medium
**Created:** 2026-11-16 11:01:02 EST · **Closed:** 2026-11-16 12:04:27 EST
**Plan:** [202611/obsidian\_ctrl\_w\_numbered\_tab\_jump.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_numbered_tab_jump.md)

## Description

paint: build the dormant tab-numeral stamper and CSS (idle, lit, here, flash, stacked) and the card's pill ranges and tabs row, with a light/dark preview harness and unit tests.

## Notes

[2026-11-16T17:04:04Z · bob-cli-mc.3] PROPOSED FOLLOW-UP: full test:unit shows the same pre-existing reds triaged by bob-cli-mc.1 (perf budgets, block-marks hardcoded-date guard, relation/highlights chips); 9 failures reproduce on clean HEAD (verified block-marks self-test on a clean worktree at 2e15ec3), none in window-prefix suites

[2026-11-16T17:04:27Z · bob-cli-mc.3] Paint phase done: dormant tab stamper (689 mixin, data-bob-tab/aria, lit/flash, all refresh/unload rules), Window tab numerals CSS (idle/lit/here/flash/stacked/reduced, theme vars only), card pill ranges + tabs row behind tabNumbers:true (byte-identical off, aria + nudge covered), preview rebuilt to 13 light/dark states on real header structure with production catalog (26 PNGs, no layout failures, lit contrast 5.8/6.3:1, PNGs reviewed), tests: 8 new stamper + 4 new card tests green, all 95 window suites green; full test:unit 9 reds all pre-existing (block-marks self-test verified failing on clean HEAD at 2e15ec3). Sync attempted per AGENTS.md but vault holds WS-10 sibling uncommitted build (actions phase still RUNNING) so no force; land agent to rebase (keep both fragments.json sides, either main.js, rebuild) and sync after sibling lands.

## Dependencies

- **Depends on:** [bob-cli-mc.1](bob-cli-mc.1.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mc.4](bob-cli-mc.4.md) ◐ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mc.3/README.md) | [bob-cli-mc.3](bob-cli-mc.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6b5a7b3`](https://github.com/bobs-org/bob-plugins/commit/6b5a7b3b5793120b44d76dfec6389cf8282e1ed2) | feat(navigation): paint dormant tab numerals, card tabs row, and previews | [bob-cli-mc.3](bob-cli-mc.3.md) | 2026-11-16 12:19:15 EST |
