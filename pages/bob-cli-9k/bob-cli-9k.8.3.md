# Bead: bob-cli-9k.8.3 — bob-plugins: JS mirror parity and Stats panel fixes

[Bead Pages](../README.md) / [bob-cli-9k.8](bob-cli-9k.8.md) / bob-cli-9k.8.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-9k.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.land.md) · **Assignee:** `bob-cli-9k.8.3` · **Size:** medium
**Created:** 2026-10-18 20:20:12 EDT · **Closed:** 2026-10-18 21:30:22 EDT
**Plan:** [202610/pomodoro\_homes\_landing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes_landing.md)

## Description

plugins: copy the updated vectors, bring the bob-ledger-tools homes mirror to parity with Rust (share rounding, lead home, any-day ^gtd home, review label, `[t::]` minutes, frontmatter shapes, closed-entry state, health), keep chips to Live Preview and Reading view with embed support, make chart pins refresh the Where the time went panel, fix the Themes pinned span, review hue, count/task marks, saved view choice, fix-it copy, and drill-down labels, update the README table, then test, validate, and sync.

## Notes

[2026-10-19T01:30:08Z · bob-cli-9k.8.3] PROPOSED FOLLOW-UP: Live Obsidian Reading/LP chip screenshot and dash_stats chart-pin on the Mac — athena has no Obsidian process, Mac SSH timed out; vault plugin is 1.58.0 and DOM tests cover Reading, Source skip, embed src, light/dark CSS, and chart-pin redraw.

[2026-10-19T01:30:22Z · bob-cli-9k.8.3] JS homes mirror matches Rust on every shared vector (copied from bob-cli 77c77410, byte-identical) and on the live 4w window: 269/269 sessions[].homes minutes and shares identical. Chips skip Source, Reading finds embed src/data-src, [t::] minutes, largest-remainder shares, lead-by-task-count, any-day ^gtd review, nested-array parent/type. Chart pin now statsRenderLocally so Where the time went and Themes follow the pin; @review:* uses area hue; count metrics keep dots/mini-bars; saved homesView is kept; fix-it copy and unnamed drill-down labels match. npm test 3109 pass / 6 known failures (unblocked-glyph, keep counts, forward conversion: bob-cli-6v/6w/7i). npm run validate green. bob-ledger-tools 1.58.0 and README nav 2.46.0. bob plugins sync copied main.js+manifest; --dry-run empty. epic-symbols none. Live Obsidian GUI unverified on athena (no Obsidian; Mac SSH timed out).

## Dependencies

- **Depends on:** [bob-cli-9k.8.1](bob-cli-9k.8.1.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.3/README.md) | [bob-cli-9k.8.3](bob-cli-9k.8.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ed72a42`](https://github.com/bobs-org/bob-plugins/commit/ed72a4201560e53221198b503c3945b9e9606e98) | feat(ledger-tools): bring pomodoro homes JS mirror to Rust parity | [bob-cli-9k.8.3](bob-cli-9k.8.3.md) | 2026-10-18 21:32:14 EDT |
