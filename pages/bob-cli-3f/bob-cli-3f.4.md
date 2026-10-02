# Bead: bob-cli-3f.4 — CROWDED chip, bob-ready-notes block, and Tasks heading chip

[Bead Pages](../README.md) / [bob-cli-3f](README.md) / bob-cli-3f.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0v5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0v5.md) · **Assignee:** `bob-cli-3f.4` · **Size:** medium
**Created:** 2026-10-01 17:55:47 EDT · **Closed:** 2026-10-01 19:18:51 EDT
**Plan:** [202610/per\_note\_ready\_cap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/per_note_ready_cap.md)

## Description

ledger-views: add the live renderCrowdedChip, the bob-ready-notes ranked-bar code block, and the `## Tasks` heading chip (CM6 widget plus Reading view). Adds theme-safe CSS, the bob-cli-3d anchor-class fix, and one consolidated live-refresh fan-out. Deploys the plugin.

## Notes

[2026-10-01T23:18:51Z · bob-cli-3f.4] ledger-views shipped in bob-ledger-tools 1.16.0: live renderCrowdedChip api, bob-ready-notes ranked-bar block, Tasks heading chip (CM6 Live Preview + Reading view), theme-safe CSS, bob-cli-3d anchor fix, consolidated scheduleLiveWidgetRefresh fan-out. Verified: npm test 1155/1155 green (incl. 17 new note-ready-views tests), npm run validate 6/6 valid, deployed via bob plugins sync (vault at 1.16.0). No epic-symbol entries remain.

## Dependencies

- **Depends on:** [bob-cli-3f.3](bob-cli-3f.3.md) ✓ · ⧖ 2026-10-01
- **Blocks:** [bob-cli-3f.5](bob-cli-3f.5.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3f.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.4/README.md) | [bob-cli-3f.4](bob-cli-3f.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@91b8e40`](https://github.com/bobs-org/bob-plugins/commit/91b8e405adb9bb1a2b76475d90e80748c17963c2) | feat(ledger-tools): CROWDED chip, bob-ready-notes block, and Tasks heading chip (1.16.0) | [bob-cli-3f.4](bob-cli-3f.4.md) | 2026-10-01 19:19:48 EDT |
