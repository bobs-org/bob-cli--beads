# Bead: bob-cli-34.3 — Navigation Hotkeys: recommended roll for counted N\<Ctrl+Shift+P\> sessions

[Bead Pages](../README.md) / [bob-cli-34](README.md) / bob-cli-34.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0um](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0um.md) · **Assignee:** `bob-cli-34.3` · **Size:** medium
**Created:** 2026-09-30 23:56:48 EDT · **Closed:** 2026-10-01 00:56:07 EDT
**Plan:** [202609/priority\_roll\_decay.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/priority_roll_decay.md)

## Description

picker-counted: plan a recommendation for each target, show a batch preview line, and compose the cancel and set-priority plans into one undoable editor transaction. Also adds the priorityValueByLine and reasonByLine planner extensions, the batch notice card, and a manifest bump.

## Notes

[2026-10-01T04:56:07Z · bob-cli-34.3] picker-counted done in bob-plugins: per-target recommendations, batch preview/notice, composed cancel+set-priority planner with priorityValueByLine/reasonByLine, one-transaction counted write, Ctrl+Enter/Ctrl+R in both stages, manifest 1.46.0. Verified: npm test 982 pass, validate 6/6, plugins sync ok, mixed roll/decay/cancel exact lines, recurring refusal, stale refusal, byte-identity

## Dependencies

- **Depends on:** [bob-cli-34.2](bob-cli-34.2.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-34.4](bob-cli-34.4.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-34.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-34.3/README.md) | [bob-cli-34.3](bob-cli-34.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d97f005`](https://github.com/bobs-org/bob-plugins/commit/d97f005f8c1aeaeec68bbce8dc9cbb1ba803b44c) | feat(nav): recommended roll for counted N\<Ctrl+Shift+P\> sessions | [bob-cli-34.3](bob-cli-34.3.md) | 2026-10-01 00:57:32 EDT |
