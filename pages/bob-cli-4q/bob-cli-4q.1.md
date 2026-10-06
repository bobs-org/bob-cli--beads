# Bead: bob-cli-4q.1 — Inbox routing core in bob-navigation-hotkeys

[Bead Pages](../README.md) / [bob-cli-4q](README.md) / bob-cli-4q.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0xh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0xh.md) · **Assignee:** `bob-cli-4q.1` · **Size:** medium
**Created:** 2026-10-06 14:57:17 EDT · **Closed:** 2026-10-06 15:17:15 EDT
**Plan:** [202610/inbox\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inbox_routing.md)

## Description

route-core: add the inbox-note classifier, the route picker modal, the preflight, the routed move commit (no focus, no park), the walk's new `route` outcome kind, and the nav api `inboxRoute` v1 namespace, with unit and runtime tests; nav 2.9.0.

## Notes

[2026-10-06T19:17:15Z · bob-cli-4q.1] route-core done in bob-navigation-hotkeys 2.9.0: classifier, route picker modal, preflight, routed move commit (no focus/park), route walk outcome, inboxRoute v1 api. Verified: new test-navigation-inbox-route.cjs 15/15, targeted move+review suites 69/69, full npm test 1925/1925, build:check clean, bob plugins sync deployed. epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-4q.2](bob-cli-4q.2.md) ◐ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4q.3](bob-cli-4q.3.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4q.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4q.1/README.md) | [bob-cli-4q.1](bob-cli-4q.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@bff5585`](https://github.com/bobs-org/bob-plugins/commit/bff5585014d5ea090d1485406840d7beb681d427) | feat(inbox-route): add inbox routing core with picker modal and move commit | [bob-cli-4q.1](bob-cli-4q.1.md) | 2026-10-06 15:18:33 EDT |
