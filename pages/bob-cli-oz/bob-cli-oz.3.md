# Bead: bob-cli-oz.3 — proseField v2: the tasks mode of the LINK band, the NAME stage, and the real-Obsidian spike

[Bead Pages](../README.md) / [bob-cli-oz](README.md) / bob-cli-oz.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ff](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ff.md) · **Assignee:** `bob-cli-oz.3` · **Size:** medium
**Created:** 2026-11-21 17:39:51 EST · **Closed:** 2026-11-22 00:43:14 EST
**Plan:** [202611/prompt\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prompt_task_links.md)

## Description

nav-task-band: add the tasks mode to nav's proseField controller in new fragments (model, renderer, mode state machine). It covers the list and NAME stages, beforeinput-fed ID editing, the leftover (( hint, and API v2, plus tests, preview states, a real-Obsidian spike, and the block-id-prompt docs section.

## Notes

[2026-11-22T05:42:43Z · bob-cli-oz.3] Real-Obsidian spike: could not run live (no Electron/Obsidian on apollo: /snap/obsidian missing, OBSIDIAN_BIN empty). Headless spike-equivalent evidence instead, all in scripts/test-navigation-prose-task-band.cjs (11/11 pass): beforeinput cancellation keeps the field byte-identical through typing/paste/Backspace in NAME; IME composing blocks open/keys and NAME onInput restores the snapshot; single execCommand insertText (setRangeText fallback) keeps one-Ctrl+Z restore of ((query; Esc ladder NAME->list->close unit-tested (modal rung is the unchanged captureKeydown/scope path); held Enter never moves list->NAME->write (swallowEnter until keyup, repeat consumed without commit). beforeinput fallback is built in: every field change in NAME is snapshot-restored, so T1 holds even if Electron beforeinput proves unreliable. Per-field ownerDocument/ownerWindow keeps pop-out windows working (code-level, unverified headless). -r Recording nav-task-band spike results in phase notes

[2026-11-22T05:42:55Z · bob-cli-oz.3] PROPOSED FOLLOW-UP: docs-check published-URLs step fails on src/native/highlights_ref/podcast/feed.rs:70 (docs/1.0.md -> /1.0/: no built page for /1.0); identical to the clean-tree failure recorded in bob-cli-oz.2 notes #1-2 and tracked by bob-cli-os. This phase docs-check also shows a pre-existing plugin-apis.md budget warning (8401 words vs 8000 cap, tracked by bob-cli-ob; this phase added ~19 words net there). -r Recording pre-existing check failure as follow-up

[2026-11-22T05:43:14Z · bob-cli-oz.3] nav-task-band done: tasks mode of the LINK band in 189c (pure ID-line/row/crumb/detail model), 189d (list+NAME renderer on bob-task-band-* classes), 189e (session state machine with beforeinput-fed NAME, snapshot restore, atomic vault-process naming); 189b delegates with separate (( dismissal memory, tasks/subjects options, isTaskOpen/isNaming/setSubjects, api v2. Verified: new suite 11/11, prose/task-card/modal/roles/api regressions 64/64, log-recall/record/intention/prompt-block-id 47/47, preview self-test ok, build:check/inventory/manifest validate green, nav docs back under 6000-word cap. docs-check published-URLs failure is the pre-existing feed.rs:70 false positive (recorded as follow-up, tracked by bob-cli-os). bob plugins sync refused by sibling in-flight builds (ws15 nav, ws16 ledger-tools, both unlanded with agents running) so no -F per deployment runbook; vault deploy lands with those phases.

## Dependencies

- **Depends on:** [bob-cli-oz.2](bob-cli-oz.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oz.4](bob-cli-oz.4.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oz.5](bob-cli-oz.5.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oz.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oz.3/README.md) | [bob-cli-oz.3](bob-cli-oz.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6a2f6ce`](https://github.com/bobs-org/bob-plugins/commit/6a2f6ce5c8eb38f2f8c4265f00d9322c058341b6) | feat(nav): add tasks mode to proseField LINK band with in-band NAME stage | [bob-cli-oz.3](bob-cli-oz.3.md) | 2026-11-22 00:44:26 EST |
