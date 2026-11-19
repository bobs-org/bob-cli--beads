# Bead: bob-cli-ni.5 — Make-or-edit card and Alt+Click edit

[Bead Pages](../README.md) / [bob-cli-ni](README.md) / bob-cli-ni.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5g.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5g.linker.w0.md) · **Assignee:** `bob-cli-ni.5` · **Size:** large
**Created:** 2026-11-19 10:05:34 EST · **Closed:** 2026-11-19 13:55:23 EST
**Plan:** [202611/copy\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/copy_chips.md)

## Description

author: add the Mod+Shift+Y card that makes, converts, or edits a chip with a live preview, writing the result in one undo step, plus Alt+Click to edit.

## Notes

[2026-11-19T18:54:55Z · bob-cli-ni.5] PROPOSED FOLLOW-UP: test-navigation-copy-card-model.cjs missing copy-chip C-row — npm test reports the Copy card model has no copy-chip C row. Reproduced on clean HEAD febfc6b before this phase's plugin work. Authoring plan forbids redoing the Copy card C row; land or a later phase should decide whether that test needs a C-row fixture.

[2026-11-19T18:55:15Z · bob-cli-ni.5] PROPOSED FOLLOW-UP: ledger-tools 25ms perf flakes under parallel npm test — two ledger-tools timing budgets failed in the full npm test run and passed when run in isolation. Unrelated to bob-copy-chips authoring; worth a flake/perf pass if the 25ms budgets keep tripping under load.

[2026-11-19T18:55:23Z · bob-cli-ni.5] Authoring phase done: Make-or-edit (Mod+Shift+Y) plus Live Preview Alt+Click edit in bob-copy-chips 0.4.0. Athena Xvfb e2e PASS on snapshot /tmp/bob-copy-chips-author-e2e-20261119T185126 with SHA-256 manifest 69e643f3f9d024ddfc0c0f436cd7d1429f5aabde53bed20fd6e6b68fe5c92f01, main.js 103d027c6cad65fdc37f01e179587d32d9553ed8f4f8989bf747289dc6cc49a5, styles.css b2db4ab9b91b8bf2c6e6b1d62ad6c6136497df144d8293887bed05610ddddb74. Deployed those exact bytes with bob plugins sync --no-pull -p bob-copy-chips. Offline author/cursor/fence/live-preview unit tests passed; npm run validate and docs:check passed. Reload Obsidian to pick up 0.4.0.

## Dependencies

- **Depends on:** [bob-cli-ni.3](bob-cli-ni.3.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-ni.6](bob-cli-ni.6.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ni.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ni.5.md) | [bob-cli-ni.5](bob-cli-ni.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ccc0f72`](https://github.com/bobs-org/bob-plugins/commit/ccc0f724a1a9f0c41f411eca96f898243ca5a845) | feat(bob-copy-chips): add make-or-edit card and Alt+Click edit | [bob-cli-ni.5](bob-cli-ni.5.md) | 2026-11-19 13:57:28 EST |
