# Bead: bob-cli-3n.5 — task-status-cycler and block-id-prompt compatibility

[Bead Pages](../README.md) / [bob-cli-3n](README.md) / bob-cli-3n.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vl.md) · **Assignee:** `bob-cli-3n.5` · **Size:** medium
**Created:** 2026-10-02 16:54:35 EDT · **Closed:** 2026-10-02 19:12:53 EDT
**Plan:** [202610/task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links.md)

## Description

compat: the cycler skips strike, restore, and tree close on Depends-On lines; Ctrl+Enter closes or reopens the target only; Alt+] and Alt+[ cycle the link under the cursor; the normalizer never edits the line. block-id-prompt's Ctrl+Shift+Enter refuses the line. Tests, bumps, and deploy.

## Notes

[2026-10-02T23:12:53Z · bob-cli-3n.5] compat done in bob-plugins: isTaskDependencyLine recogniser (DP vectors) copied into task-status-cycler and block-id-prompt; cycler skips retire/restore/tree-close on Depends-On lines, Ctrl+Enter closes/reopens target root-only with finalizeClosedTasks recovery and no strike/unstrike, Alt+]/[ (single+counted) cycle link under cursor with notice otherwise, getPlainBulletFormatToggle never applies; block-id-prompt Ctrl+Shift+Enter refuses with new notice, never deletes; isDedicated* helpers reject the line (isDedicatedLinkBullet newly exported). Tests: 175/175 cycler, 167/167 bid, 1210/1210 full suite, manifests validate. Bumped cycler 1.20.0 + bid 1.18.0, README rows updated, both deployed to vault via bob plugins sync (scoped -p to avoid sibling agents' files). No epic-symbol leftovers; bob-cli tree untouched.

## Dependencies

- **Depends on:** [bob-cli-3n.1](bob-cli-3n.1.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.6](bob-cli-3n.6.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.9](bob-cli-3n.9.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.5/README.md) | [bob-cli-3n.5](bob-cli-3n.5.md) | 0 |
