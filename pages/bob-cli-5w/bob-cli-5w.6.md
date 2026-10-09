# Bead: bob-cli-5w.6 — The Unblocked notice card and nav \`api.notice\`

[Bead Pages](../README.md) / [bob-cli-5w](README.md) / bob-cli-5w.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0p.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0p.linker.w0.md) · **Assignee:** `bob-cli-5w.6` · **Size:** medium
**Created:** 2026-10-09 11:54:15 EDT · **Closed:** 2026-10-09 12:32:40 EDT
**Plan:** [202610/successor\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_links.md)

## Description

nav_card: in bob-navigation-hotkeys, add the Unblocked notice card in a new fragment: `is-unblock` styles on existing tokens, clickable rows, chips, and breaker and failure variants. Expose it as the additive `api.notice` v1. Ships tests, a version bump, a README update, and a sync.

## Notes

[2026-10-09T16:32:24Z · bob-cli-5w.6] PROPOSED FOLLOW-UP: record decisions strand closed-task-hands-slot-to-successors (claim, rejected alternatives, cost, reopens-when) per epic closeout memory decision

[2026-10-09T16:32:29Z · bob-cli-5w.6] PROPOSED FOLLOW-UP: add glossary strand successor-link cross-linked to task-link and task-dependency-link per epic closeout memory decision

[2026-10-09T16:32:33Z · bob-cli-5w.6] PROPOSED FOLLOW-UP: fix 2 date-sensitive test-navigation-roll-decay.cjs failures (picker-single P2 roll expects [?] but gets [ ]) that reproduce identically on the clean base tree

[2026-10-09T16:32:40Z · bob-cli-5w.6] nav_card landed in bob-plugins: new src/285-unblocked-notice.js (buildUnblockedNoticeModel/renderUnblockedNoticeFragment/showUnblockedNotice/createNoticeApi), is-unblock CSS on task-status tokens, additive api.notice v1 (api stays v3), manifest 2.15.0, README row, 16/16 new tests green, npm run build + build:check green, full suite 2248/2251 with only 2 pre-existing roll-decay failures identical on clean base, bob plugins sync deployed

## Dependencies

- **Depends on:** [bob-cli-5w.2](bob-cli-5w.2.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5w.8](bob-cli-5w.8.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5w.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.6/README.md) | [bob-cli-5w.6](bob-cli-5w.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@aff37aa`](https://github.com/bobs-org/bob-plugins/commit/aff37aabe48815166905723b9739a495aa4e1bb9) | feat(bob-navigation-hotkeys): add unblocked-notice fragment with api.notice v1 | [bob-cli-5w.6](bob-cli-5w.6.md) | 2026-10-09 12:34:26 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5w.6][1] | Need full phase notes and fields | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.6/README.md

<!-- sase:referenced-by:end -->
