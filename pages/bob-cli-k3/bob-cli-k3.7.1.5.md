# Bead: bob-cli-k3.7.1.5 — Album and record kinds in navigation

[Bead Pages](../README.md) / [bob-cli-k3.7.1](bob-cli-k3.7.1.md) / bob-cli-k3.7.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.7.md) · **Assignee:** `bob-cli-k3.7.1.5` · **Size:** medium
**Created:** 2026-11-11 23:10:18 EST · **Closed:** 2026-11-12 10:08:06 EST
**Plan:** [202611/album\_plugin\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_plugin_ui.md)

## Description

album-navigation: implement accessible album/record icons, album and record parent-picker rules with commit-time checks, task-home exclusions, and focused navigation regressions.

## Notes

[2026-11-12T15:07:46Z · bob-cli-k3.7.1.5] PROPOSED FOLLOW-UP: test-ledger-tools-task-tag-marks.cjs "session toggle and onload wiring" fails (2 !== 1) on clean base c2f6834 too — pre-existing, unrelated to album-navigation; needs triage

[2026-11-12T15:07:52Z · bob-cli-k3.7.1.5] PROPOSED FOLLOW-UP: docs-check strict Zensical build fails on pre-existing broken anchor develop/plugins/validation.md:55 -> ../bob-vim-yank-flash.md#verification; lint and generated-drift pass — needs triage

[2026-11-12T15:08:06Z · bob-cli-k3.7.1.5] album-navigation done in linked bob-plugins checkout (uncommitted): explicit album kind before record fallback in parentRuleKindOf with [[record]] direct + legacy-noun compat; album parents = area/project any status, record parents = album only, notebook rules unchanged, commit-time live re-check via existing parentChangeLiveIndex; Lucide album/file-text icons with Album/Record labels, summary + search-text coverage, is-status-album/record CSS; delete-guard labels. Tests: new test-navigation-parent-album-record.cjs (16 tests) registered in test:unit; notebook-gestures expectations updated for new rules. Verified: linked-repo build+validate+inventory-check pass, focused navigation suites 76/76, full test:unit 6280/6281 (1 pre-existing task-tag-marks failure reproduced on clean base, noted as follow-up), test:perf 5/5, docs lint+drift pass (strict-build failure is a pre-existing broken anchor, noted as follow-up). bob plugins sync NOT run to completion: vault holds an uncommitted WS-10 deploy (ed5e648-based) whose author agent is still RUNNING, so per deployment.md no force/clean-sync; land agent to sync after that lands. Docs: bob-navigation-hotkeys.md parent rules + task-home exclusion updated.

## Dependencies

- **Depends on:** [bob-cli-k3.7.1.4](bob-cli-k3.7.1.4.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.7.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.7.1.5/README.md) | [bob-cli-k3.7.1.5](bob-cli-k3.7.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2d10fca`](https://github.com/bobs-org/bob-plugins/commit/2d10fca3ce8b6333af0fa41c82847d65083282cc) | feat(navigation-hotkeys): album and record kinds in parent pickers | [bob-cli-k3.7.1.5](bob-cli-k3.7.1.5.md) | 2026-11-12 10:09:25 EST |
