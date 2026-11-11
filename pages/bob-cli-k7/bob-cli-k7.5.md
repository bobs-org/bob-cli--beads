# Bead: bob-cli-k7.5 — Live Preview, Reading view, look, and liveness

[Bead Pages](../README.md) / [bob-cli-k7](README.md) / bob-cli-k7.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b8.md) · **Assignee:** `bob-cli-k7.5` · **Size:** medium
**Created:** 2026-11-11 07:57:58 EST · **Closed:** 2026-11-11 11:15:52 EST
**Plan:** [202611/keep\_moving\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/keep_moving_link_marks.md)

## Description

mark-surface: in bob-ledger-tools, render the mark in Live Preview and Reading view, with the shared source-text cache, refresh triggers, baton-pass tick, toggle, CSS, off-clock chip at side 4, docs, a real-Obsidian e2e, build, and sync.

## Notes

[2026-11-11T16:15:32Z · bob-cli-k7.5] PROPOSED FOLLOW-UP: docs budget gate red on bob-ledger-tools (6101 words vs the 6000 reference/ cap): k7.5 added the plan-required contract docs (+104 lint-words on a file that sat at 5997) and the gate already fails identically on 5 pre-existing pages (mac-capture capture-panel/capture-previews/keyboard/protocol, nav-hotkeys). Triage: split the plugin doc or adjust the reference cap; `npm run docs:check` cannot go green until then.

[2026-11-11T16:15:52Z · bob-cli-k7.5] mark-surface done and verified: 271g Live Preview (side 3, shared source-text cache, baton LRU tick, toggle) + 271h Reading (KP3/KP4 insertion, stale-host sweep) wired via setupMarkFamilies; LRU 32->64 with fill fan-out; off-clock chip to side 4 (+271d skip, 269 allow-list, ink fallback per contract); 141d tooltip titles stripped to clean prose (KT1). Tests: 13 surface vectors, 208-file node set incl. parity + neighbors all green; real-Obsidian e2e 47 pass/1 principled skip (KB7 ⏭4, baton, KP2 live order, tooltip, clicks, toggle, screenshots; tick-burst skipped: this display never fires animationstart, proven via unmodified frees/off-chip controls which show the same Reading/animation gaps). Synced to vault (1.110.0 verified). Follow-up filed for the docs budget overage.

## Dependencies

- **Depends on:** [bob-cli-k7.4](bob-cli-k7.4.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k7.6](bob-cli-k7.6.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k7.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k7.5/README.md) | [bob-cli-k7.5](bob-cli-k7.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@27b99dd`](https://github.com/bobs-org/bob-plugins/commit/27b99ddd0f927e659d2241913c8fa2116d439eee) | feat(ledger-tools): render keep-moving marks in Live Preview and Reading view Shows a quiet mark after the last planned Task Link of a leaf project: shared source-text cache, refresh fan-out, baton-pass tick, session toggle, off-clock chip at side 4, contract docs, surface unit tests, real-Obsidian e2e. Tooltip titles stripped to clean prose (KT1). | [bob-cli-k7.5](bob-cli-k7.5.md) | 2026-11-11 11:19:38 EST |
