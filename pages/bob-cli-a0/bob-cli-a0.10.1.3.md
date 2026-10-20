# Bead: bob-cli-a0.10.1.3 — Write the seven plugin reference pages

[Bead Pages](../README.md) / [bob-cli-a0.10.1](bob-cli-a0.10.1.md) / bob-cli-a0.10.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.md) · **Assignee:** `bob-cli-a0.10.1.3` · **Size:** medium
**Created:** 2026-10-19 23:16:01 EDT · **Closed:** 2026-10-19 23:42:56 EDT
**Plan:** [202610/plugin\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plugin_reference.md)

## Description

plugin-pages: move the plugin-specific README details into seven usable reference pages with settings, keyboard-handler distinctions, and authoritative contract links.

## Notes

[2026-10-20T03:42:08Z · bob-cli-a0.10.1.3] Coverage mapping (README -> docs page): Plugins-table row block-id-prompt (line 20) -> docs/block-id-prompt.md (link/unlink toggle, Task Link selection, Depends-On/BLOCKS/closed-target guards, freshness+plan-budget, ^prj rules, inbox+walk behavior, api.pomodoroLinkPicker v1). Row bob-articles (line 21) -> docs/bob-articles.md (format/adopt commands, save/leave triggers, 5 settings keys+defaults from source: formatOnSave/formatOnLeave/articleTypeface/staleNumberHints/bobPath). Row bob-ledger-tools (line 22) + Task-Card-embedded snippets (lines 141-152) + bob-plan/api prose (lines 154-202) -> docs/bob-ledger-tools.md (snippets, plan block, footer, 4 marks, badges, chips/BLOCKS, stats, reading board, freshness/review/noteReady, session toggles, shared-config keys). Row bob-navigation-hotkeys (line 23) + Highlights custom-binding note (lines 336-340) -> docs/bob-navigation-hotkeys.md (Task Card overview, J/K+counts, Pomodoro moves incl. =/=NAME/Ctrl+X merge, property/dependency/move gestures, projects, Alt+N, review walk, jump history, tabs, 3 keyboard layers with Meta+Enter labeled custom vault config, Vim \s vs ledger \p). Row bob-project-tasks (line 24) -> docs/bob-project-tasks.md (task_count/open_task_count, recount, bob-ref-create snapshots incl -C flag verified in source). Row bob-vim-surround (line 25) + Task-Card-embedded keys (lines 206-215) -> docs/bob-vim-surround.md (ys/cs/ds+dot-repeat, accepted/rejected keys, padding, symmetric runs). Row task-status-cycler (line 26) + cycler api (line 204) -> docs/task-status-cycler.md (Pomodoro/task completion, placeholders, section-picker routing, Blocked cycling, link guards, successor offers+take-backs, lanes/projects/handoffs, recoverBlockedDependents/completeTaskAtCursor). Verified in source: only bob-articles has a settings tab (no loadData/addSettingTab in other six); all other README sections (Block ID defaults, BLOCKS mirrors, Task Card core, URIs, Highlights, Templater, Layout/Development/Deploy/Scope/License) stay in README for topic-migration. Generated regions untouched (diff adds 661 lines prose only); budgets max 1677/6000 words.

[2026-10-20T03:42:18Z · bob-cli-a0.10.1.3] PROPOSED FOLLOW-UP: npm test has 7 failures that reproduce without this phase work — 6 fail identically on the clean base (4x test-ledger-tools-unblocked-glyph.cjs, Keep-counts in test-navigation-decision-card-handlers.cjs, forward-promotion Depends-On case) plus 1 load-sensitive perf flake (stage ranker 16ms/keystroke: 23ms under full suite, 14/14 pass in isolation with these changes). Docs-only phase; no JS touched. Triage into task beads if not already tracked.

[2026-10-20T03:42:56Z · bob-cli-a0.10.1.3] All seven plugin reference pages complete and within budgets (max 1677/6000 words); registered/default vs handler/custom bindings distinguishable with Highlights Meta+Enter labeled custom vault config; generated regions untouched. Verified: docs:gen deterministic, docs:inventory:check pass, npm run validate pass, plugin sync exit 0. npm test 3199 pass / 7 fail — all 7 reproduce without this work (6 identical on clean base + 1 load-sensitive perf flake passing in isolation), recorded as PROPOSED FOLLOW-UP. Coverage mapping recorded in phase notes.

## Dependencies

- **Depends on:** [bob-cli-a0.10.1.2](bob-cli-a0.10.1.2.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.10.1.4](bob-cli-a0.10.1.4.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.10.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.3/README.md) | [bob-cli-a0.10.1.3](bob-cli-a0.10.1.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.10.1.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.3/README.md

<!-- sase:referenced-by:end -->
