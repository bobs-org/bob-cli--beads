# Bead: bob-cli-m0.1 — Real-Obsidian layout and keyboard spike

[Bead Pages](../README.md) / [bob-cli-m0](README.md) / bob-cli-m0.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e9.md) · **Assignee:** `bob-cli-m0.1` · **Size:** medium
**Created:** 2026-11-15 20:01:48 EST · **Closed:** 2026-11-15 21:02:57 EST
**Plan:** [202611/obsidian\_ctrl\_w\_window\_prefix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_window_prefix.md)

## Description

spike: build the window-prefix CDP e2e harness and prove lossless cross-group tab moves, split create/collapse, and keyboard precedence in real Obsidian.

## Notes

[2026-11-16T02:02:07Z · bob-cli-m0.1] PROPOSED FOLLOW-UP: pre-existing bob-plugins gate failures unrelated to the spike (reproduced on pristine HEAD worktree / load flakes): test-obsidian-block-marks-e2e --self-test fails with "fixture must use relative dates, not hardcoded contract dates"; 4 perf-budget tests (event-link-times, frees-marks, keep-moving-marks-surface, off-clock-link-chips) fail only under full-suite load and pass in isolation. Spike scripts themselves are green.

[2026-11-16T02:02:34Z · bob-cli-m0.1] SPIKE VERDICT: lossless move PROVEN on Obsidian 1.15.1/athena-xvfb (Electron 43.8.9). Harness scripts/obsidian-window-prefix-e2e.cjs + -lib.cjs + test wrapper committed; --self-test green; real run 15/15 PASS twice (report.json sha-pinned, sourceSha 1caabb8 + uncommitted spike scripts). (1) MOVE LOSSLESS: sourceGroup.removeChild(leaf) -> dest.insertChild(i,leaf) -> dest.selectTab(leaf) -> dest.recomputeChildrenDimensions() -> sourceGroup.recomputeChildrenDimensions() -> workspace.onLayoutChange() -> workspace.setActiveLeaf(leaf,{focus:true}) -> workspace.requestSaveLayout(). Same leaf object + same editor (tagged identity), type->move->u restores exact text, cursor/folds/pin preserved, go-back history works post-move (go-forward flaky at BASELINE: passed 1/3 runs, pre-existing, do not depend on it), reading-view + PDF + 1px-PNG leaves render after reparent. Scroll: remove/insert preserve scrollTop; dest.selectTab RESETS it to 0 (stepwise proof); manual restore post-move sticks (executor must save/restore scroll around selectTab). Pin via leaf.togglePinned()/leaf.pinned (nav plugin toggleCurrentTabPin calls it). (2) COLLAPSE: leaf.detach() on a split-last tab auto-collapses the split (closeCalls leaf.detach:ok, no explicit call needed); width redistributes to neighbours (340->680); requestSaveLayout + app reload preserves layout. Caveat: the windows last leaf never closes (file-less empty placeholder persists; harness reuses it). (3) CREATE: createLeafBySplit(leaf,vertical,before) makes a new split holding ONE empty placeholder leaf and NEVER empties the source mid-op. before=true AND before=false both land the new split on the RIGHT in 1.15.1 (flag does not select side; create-left needs another call shape). duplicateLeaf(leaf,split,vertical) focuses a NEW leaf on the same file (view mounts async ~800ms; read-after-write must wait). (4) KEYBOARD: (a) unbound Ctrl+W: window capture listener fires BEFORE CodeMirror/bubble, defaultPrevented=false, nothing closes. (b) default Linux binding: Close tab runs FIRST, capture sees defaultPrevented=true, active tab closes 2->1. (c) pushed catch-all Scope (constructed via app.scope.constructor; global Scope undefined; keymap exposes pushScope/popScope) intercepts bound Ctrl+L (palette stays shut) AND plain letters (no text/cursor change); binding live without Scope. (d) popScope removes a non-top scope under an open modal without throwing; keyboard healthy after. (e) insert-mode Ctrl+W passes through and deletes exactly one word. (f) app.scope.register([Ctrl],w) does NOT preempt a bound Close (handler never fired; tab still closed first). (5) FACTS: no native focus/move split commands with split/tab/group/column in the id, BUT native editor:focus-left/right/top/bottom exist (full 373-command list in report.allCommands); .workspace-tabs.mod-active present (1); getMostRecentLeaf is function (selected-tab resolution works); leaf.loadIfDeferred is function; background tabs stay loaded in practice; bundled Vim exposes map/unmap/mapCommand/buildKeyMap but NO nmap; per-editor Vim state lives at editor.cm.cm.state.vim (inner cm, NOT editor.cm.state.vim; matches house resolveVimCodeMirror); partial matching PROVEN (map <C-w>q->l, keyBuffer [<C-w>] pending, q completes, cursor moves, unmap cleans); idle <C-w> entry NOT directly observed (buildKeyMap() returns undefined; nmap absent) - settle via asar source read if needed; does not block design (4a/4c prove interception order). hotkeyManager get/setHotkeys available. HARNESS CAVEATS for later phases: iterateRootLeaves STOPS when the callback returns truthy (always use block-body callbacks; the bisect proves 1-vs-3); detach() cannot remove the windows last leaf; selectTab resets scrollTop; duplicateLeaf views mount async; go-forward flaky at baseline.

[2026-11-16T02:02:57Z · bob-cli-m0.1] Spike complete: harness committed (obsidian-window-prefix-e2e.cjs/-lib.cjs/test wrapper + test:unit entry), self-test + build:check green, real Obsidian 1.15.1 run on athena 15/15 PASS twice. Verdict: lossless reparent proven with exact call sequence; detach auto-collapses + reload stable; create/duplicate placement mapped; keyboard (a)-(f) answered with evidence; later-phase facts recorded. SPIKE VERDICT + follow-up notes on bead. No plugin fragments changed (main.js untouched). Pre-existing failures (block-marks dates, perf flakes) reproduced on clean base, filed as follow-up. bob plugins sync: nav bundle refused (ws13 uncommitted deploy, no -F per AGENTS.md) but moot - my tree changes no plugin output.

## Dependencies

- **Blocks:** [bob-cli-m0.3](bob-cli-m0.3.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-m0.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.1/README.md) | [bob-cli-m0.1](bob-cli-m0.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a2550d6`](https://github.com/bobs-org/bob-plugins/commit/a2550d69ef0cf0606dd4bd3647c7a43646d9e7f2) | feat(nav): add Ctrl+W window-prefix real-Obsidian spike e2e harness | [bob-cli-m0.1](bob-cli-m0.1.md) | 2026-11-15 21:05:21 EST |
