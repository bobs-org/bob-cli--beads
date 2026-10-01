# Bead: bob-cli-34.2 — Navigation Hotkeys: Ctrl+Enter recommended roll for single and ^prj tasks

[Bead Pages](../README.md) / [bob-cli-34](README.md) / bob-cli-34.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0um](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0um.md) · **Assignee:** `bob-cli-34.2` · **Size:** medium
**Created:** 2026-09-30 23:56:47 EDT · **Closed:** 2026-10-01 00:34:14 EDT
**Plan:** [202609/priority\_roll\_decay.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/priority_roll_decay.md)

## Description

picker-single: add the roll preview line on the `scheduled` row, Ctrl+Enter in both picker stages, and Ctrl+R re-roll in stage one. The value stage's pinned row shares the previewed date. Writes are guarded and re-verified for roll, decay and cancel, with decay-aware notice cards, CSS, a manifest bump and a vault deploy.

## Notes

[2026-10-01T04:34:14Z · bob-cli-34.2] picker-single verified: npm test 964 pass (19 roll-decay incl 6 new picker-single), manifests valid, vault files identical, no epic symbols

## Dependencies

- **Depends on:** [bob-cli-34.1](bob-cli-34.1.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-34.3](bob-cli-34.3.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-34.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-34.2/README.md) | [bob-cli-34.2](bob-cli-34.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b56bb9d`](https://github.com/bobs-org/bob-plugins/commit/b56bb9d00088557f5f30c76160457e69331bf772) | feat(nav): Ctrl+Enter recommended roll for single and ^prj tasks | [bob-cli-34.2](bob-cli-34.2.md) | 2026-10-01 00:35:30 EDT |
