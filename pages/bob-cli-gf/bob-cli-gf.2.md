# Bead: bob-cli-gf.2 — The chip in bob-ledger-tools (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-gf](README.md) / bob-cli-gf.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c9.md) · **Assignee:** `bob-cli-gf.2` · **Size:** medium
**Created:** 2026-11-03 09:51:50 EST · **Closed:** 2026-11-03 10:48:33 EST
**Plan:** [202611/off\_clock\_link\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_link_chips.md)

## Description

chip: implement the contract in bob-ledger-tools — pure core, Live Preview widget, Reading-view sweep, shared CSS, toggle, liveness, unit and parity tests, plugin docs, build, and bob plugins sync.

## Notes

[2026-11-03T15:39:25Z · 17b--code] COORDINATION NOTE (from a planning agent; not remaining work and not an earlier attempt at this phase): Epic bob-cli-gg (Event link times) edits the same bob-plugins files in parallel, and gf's plan does not mention it. Before committing, read the CROSS-EPIC COORDINATION note on epic bob-cli-gf (`sase bead read bob-cli-gf`) and fetch bob-plugins master. If gg's commit is already there, apply items 1–4: rebase, keep both features, rebuild `main.js` instead of hand-merging it, bump `manifest.json` past master, and never sync with `-F` over gg's deploy.

[2026-11-03T15:47:32Z · bob-cli-gf.2--3] PROPOSED FOLLOW-UP: Stabilize five existing npm test failures reproduced with the same assertions on clean base HEAD 175acedcf6c9ccfde92f81c223217f1ea2018e6b: test-command-mode-sheet-sequence-dom cannot find Chromium; test-ledger-tools-freshness-namespace misses reload-open-search-results; test-ledger-tools-note-ready startup scan count is 1 instead of 2; test-ledger-tools-relation-index does not finish its scan after layout-ready; test-navigation-hotkeys-schedule-work-log expected the Pending row to become [?] but it stayed [/]. The clean-base-only test-ledger-tools-freshness-mark-surfaces large-child performance failure does not need follow-up because the phase worktree passed it.

[2026-11-03T15:48:33Z · bob-cli-gf.2--3] Implemented and built the off-clock Task Link chip for Live Preview and Reading view, including historical rows, clock parity, cache refresh, toggle, tests, and docs. Focused regressions passed (173); npm run validate and npm run docs:check passed. npm test has five failures that reproduce on clean base and are recorded as a PROPOSED FOLLOW-UP. bob plugins sync --repo deployed the 1.96.0 plugin; git diff --check passed; epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-gf.1](bob-cli-gf.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gf.3](bob-cli-gf.3.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gf.2.md) | [bob-cli-gf.2](bob-cli-gf.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@23d401b`](https://github.com/bobs-org/bob-plugins/commit/23d401bc95fca3e92baed6a5565a98833a4b653b) | feat(ledger-tools): add off-clock link chips | [bob-cli-gf.2](bob-cli-gf.2.md) | 2026-11-03 10:50:05 EST |
