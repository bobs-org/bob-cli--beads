# Bead: bob-cli-mc.5 — Docs, visual acceptance, and polish

[Bead Pages](../README.md) / [bob-cli-mc](README.md) / bob-cli-mc.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4y.linker.w0.md) · **Assignee:** `bob-cli-mc.5` · **Size:** medium
**Created:** 2026-11-16 11:01:02 EST · **Closed:** 2026-11-16 14:04:48 EST
**Plan:** [202611/obsidian\_ctrl\_w\_numbered\_tab\_jump.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_numbered_tab_jump.md)

## Description

finish: document digits and numerals on the Window keys page, run real-Obsidian visual acceptance in light and dark, fix every polish issue, and sync.

## Notes

[2026-11-16T18:50:26Z · bob-cli-mc.5--1] PROPOSED FOLLOW-UP: Repair the block-marks e2e self-test hardcoded-date guard (tracked by bob-cli-m8); scripts/test-obsidian-block-marks-e2e.cjs fails identically in this suite and a clean git-archive HEAD run with “fixture must use relative dates, not hardcoded contract dates”.

[2026-11-16T19:04:19Z · bob-cli-mc.5--2] ACCEPTANCE: PASS — Phase-scope real-Obsidian acceptance is complete; no phase-scoped polish defect was found and no code change was needed.

Reports (copied evidence under /tmp/bob-cli-mc5-evidence.XBEt37/athena-evidence):
- Visual: /tmp/bob-cli-mc5-evidence.XBEt37/athena-evidence/visual.json and visual.log — 56/56 cases passed, zero skipped, 52 screenshots. Reviewed all 52 PNGs in /tmp/bob-cli-mc5-evidence.XBEt37/athena-evidence/visual-shots (contact sheet: /tmp/bob-cli-mc5-visual-contact-sheet.png): light/dark idle, lit, and flash across one, two, and three splits; overflow; stacked tabs; both range-card cases; and Linux hidden numerals. No polish issue found.
- Tabs: /tmp/bob-cli-mc5-evidence.XBEt37/athena-evidence/tabs.json and tabs.log — 31/31 passed, zero skipped.
- Prefix: /tmp/bob-cli-mc5-evidence.XBEt37/athena-evidence/prefix.json and prefix.log — 17/17 passed, zero skipped.
- Actions: /tmp/bob-cli-mc5-evidence.XBEt37/athena-evidence/actions.json and actions.log — 18/18 passed, zero skipped.
- Full plugin suite: /tmp/bob-cli-mc5-evidence.XBEt37/npm-test.log — failed with 13 test failures, including the block-marks hardcoded-date guard. The archived clean-base run at /tmp/bob-cli-mc5-evidence.XBEt37/clean-base-npm-test.log failed earlier in docs:inventory:check at 688-plugin-window-prefix-commands.js:14:42 (command-table entries must be object literals), before unit/performance tests. Retain the existing PROPOSED FOLLOW-UP for the block-marks guard citing bob-cli-m8, based on the earlier clean git-archive HEAD comparison; this monitor’s clean-base run did not reach that test.

Sync: bob plugins sync exited 0; all plugins up to date, 0 copied, 0 skipped, 31 unchanged. It also reported the existing bob-emoji vault Git tracking warning.

[2026-11-16T19:04:48Z · bob-cli-mc.5--2] Closed after recording acceptance: all four real-Obsidian groups passed, 52 visual screenshots were reviewed, sync completed, and suite failures/follow-up evidence were documented.

## Dependencies

- **Depends on:** [bob-cli-mc.4](bob-cli-mc.4.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mc.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mc.5.md) | [bob-cli-mc.5](bob-cli-mc.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@cf25d60`](https://github.com/bobs-org/bob-plugins/commit/cf25d6027c57f3d68065c79de245f99afd751129) | feat(navigation): add numbered tab focus hints | [bob-cli-mc.5](bob-cli-mc.5.md) | 2026-11-16 14:06:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mc.5--2][1] | Verify appended acceptance evidence before closing this completed phase | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mc.5.md

<!-- sase:referenced-by:end -->
