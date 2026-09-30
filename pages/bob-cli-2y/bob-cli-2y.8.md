# Bead: bob-cli-2y.8 — Ctrl+Shift+Enter toggles on link presence and never changes the lane

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.8` · **Size:** medium
**Created:** 2026-09-30 16:42:00 EDT · **Closed:** 2026-09-30 17:29:16 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

link-toggle: block-id-prompt links or unlinks by link presence, never writes the checkbox on unlink, offers the Work Log prompt for In Progress, and never lowers In Progress when linking.

## Notes

[2026-09-30T21:29:16Z · bob-cli-2y.8] link-toggle done in bob-plugins block-id-prompt 1.15.0: toggle decides on link presence, unlink never writes checkbox, Work Log prompt retitled Unlink task, forceNext never lowers In Progress, link-mode keeps all lanes with target re-read guard. Verified: node --test block-id-prompt 158/158, npm test 854/854, npm run validate 6/6, bob plugins sync deployed, Work Log strand updated.

## Dependencies

- **Blocks:** [bob-cli-2y.10](bob-cli-2y.10.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.2](bob-cli-2y.2.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2y.9](bob-cli-2y.9.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.8/README.md) | [bob-cli-2y.8](bob-cli-2y.8.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`85f7901`](https://github.com/bobs-org/bob-cli/commit/85f79018ab2e47075c9123c3a03c8ef2f9805f85) | docs(memory): unlinking an In Progress task keeps its lane in the Work Log strand | [bob-cli-2y.8](bob-cli-2y.8.md) | 2026-09-30 17:32:20 EDT |
| bob-plugins | [`bob-plugins@b9d9828`](https://github.com/bobs-org/bob-plugins/commit/b9d98284f658666a0e11d82d42de612666b6ef72) | feat(block-id-prompt): lane-preserving Ctrl+Shift+Enter link toggle | [bob-cli-2y.8](bob-cli-2y.8.md) | 2026-09-30 17:32:54 EDT |
