# Bead: bob-cli-du.5 — task-status-cycler API v3 exposes its Done line rewrite and post-Done pass

[Bead Pages](../README.md) / [bob-cli-du](README.md) / bob-cli-du.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.aw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.aw.md) · **Assignee:** `bob-cli-du.5` · **Size:** medium
**Created:** 2026-10-28 14:49:53 EDT · **Closed:** 2026-10-28 15:36:09 EDT
**Plan:** [202610/relation\_complete\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_complete_labels.md)

## Description

cycler-done-api: expose completeTaskLineText and finalizeClosedTasks on the cycler api (version 3), refactor Ctrl+Enter onto them byte-identically, and pin the done vectors in bob-plugins.

## Notes

[2026-10-28T19:36:09Z · bob-cli-du.5] Cycler api v3: added completeTaskLineText + finalizeClosedTasks (version 3), refactored Ctrl+Enter local-fallback Done write onto completeTaskLineText, copied relation_complete vectors byte-for-byte with README. Verified: new vector test 3/3, cycler+relation suites 528/528, full npm test 3953/3953 on re-run (one unrelated ledger-tools timing flake passed in isolation and on re-run), npm run build:check and docs:check passed, task-status-cycler deployed via bob plugins sync. Uncommitted in linked bob-plugins checkout for land flow (no commit authorization this turn); bob-cli checkout untouched.

## Dependencies

- **Depends on:** [bob-cli-du.1](bob-cli-du.1.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-du.6](bob-cli-du.6.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.5/README.md) | [bob-cli-du.5](bob-cli-du.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-du.5][1] | need assignee name for commit trailer | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.5/README.md

<!-- sase:referenced-by:end -->
