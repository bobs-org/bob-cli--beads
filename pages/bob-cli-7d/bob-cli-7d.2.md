# Bead: bob-cli-7d.2 — bob-navigation-hotkeys obsidian://bob-goto-task handler

[Bead Pages](../README.md) / [bob-cli-7d](README.md) / bob-cli-7d.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4b.linker.w0.md) · **Assignee:** `bob-cli-7d.2` · **Size:** medium
**Created:** 2026-10-13 09:50:29 EDT · **Closed:** 2026-10-13 10:10:28 EDT
**Plan:** [202610/slash\_task\_goto.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/slash_task_goto.md)

## Description

plugin-goto-uri: register the read-only `bob-goto-task` protocol handler that maps the absolute path into the vault, re-finds the task by ref digest / block ID, and lands through a neutral helper factored out of the task-move landing; tests, README, version, build, sync.

## Notes

[2026-10-13T14:09:55Z · bob-cli-7d.2] plugin-goto-uri complete. bob-navigation-hotkeys 2.32.0 registers read-only obsidian://bob-goto-task. npm run build, build:check, and validate passed. URI suite 25/25 plus move/jump/review-advance 115/115 green. Full npm test 2668 pass / 5 fail, the 5 identical on clean master (bob-cli-6v, bob-cli-6w). bob plugins sync --repo <linked bob-plugins> -p bob-navigation-hotkeys: git pull skipped (dirty tree); copied manifest.json 2.16.0→2.32.0 and main.js; backups in /home/bryan/.local/state/bob-cli/plugin-backups/20261013-100940. Never passed -F.

[2026-10-13T14:09:56Z · bob-cli-7d.2] PROPOSED FOLLOW-UP: Pre-existing bob-plugins npm test failures on clean master — four unblocked-glyph cases tracked by bob-cli-6v (test-ledger-tools-unblocked-glyph.cjs: Live Preview places one glyph…, widget mousedown…, rebuild triggers…, Reading view glyphs…) and Keep counts once tracked by bob-cli-6w (test-navigation-decision-card-handlers.cjs: last notice is "Update Bob Ledger Tools to record review stats"). Reproduced identically after git stash on this checkout.

[2026-10-13T14:10:28Z · bob-cli-7d.2] plugin-goto-uri landed in bob-plugins: bob-navigation-hotkeys 2.32.0 registers read-only obsidian://bob-goto-task (parse/map/refind/land via focusTaskAnchor; no vault writes). npm run build, build:check, validate green. URI tests 25/25; move/jump/review-advance 115/115. Full npm test 2668 pass / 5 fail identical on clean master (bob-cli-6v, bob-cli-6w). bob plugins sync copied manifest+main.js (vault 2.16.0→2.32.0); backups 20261013-100940. epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-7d.4](bob-cli-7d.4.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7d.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7d.2/README.md) | [bob-cli-7d.2](bob-cli-7d.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@76924cc`](https://github.com/bobs-org/bob-plugins/commit/76924ccbf011c8bd1c542e7b66b6fd027a359c24) | feat(nav): register read-only obsidian://bob-goto-task handler | [bob-cli-7d.2](bob-cli-7d.2.md) | 2026-10-13 10:12:43 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7d.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7d.2/README.md

<!-- sase:referenced-by:end -->
