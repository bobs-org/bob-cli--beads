# Bead: bob-cli-4l.1 — Nav review-advance core, shared advance tail, and nav api v3

[Bead Pages](../README.md) / [bob-cli-4l](README.md) / bob-cli-4l.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0d.linker.w0.md) · **Assignee:** `bob-cli-4l.1` · **Size:** medium
**Created:** 2026-10-06 07:01:40 EDT · **Closed:** 2026-10-06 07:20:04 EDT
**Plan:** [202610/review\_walk\_answer\_auto\_advance.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/review_walk_answer_auto_advance.md)

## Description

nav-core: add the landing-scoped capture/continue helper and its gesture lock, settle window, landing epoch and lifetime, and the pure outcome predicate. Add one shared advance tail that plans from the anchor, records a Vim jump, and composes one toast. Move Ctrl+Alt+F, the decay card, and the checklist claim onto that tail, and expose `reviewWalk` on nav api v3 (nav 2.5.0).

## Notes

[2026-10-06T11:20:04Z · bob-cli-4l.1] nav-core done in workspace clone: 536 review-advance fragment (capture/continue, gesture lock 3000ms, settle 350ms, epoch/lifetime, reviewOutcomeResolves, shared anchor-only tail with Vim jump + one composed toast), Ctrl+Alt+F/decay/checklist on the tail, landOnReviewQueueEntry+jumpToDueTask moved 520->536 (both under 1000 lines), nav api v3 + manifest 2.5.0. Verified: npm run build clean, full npm test 1829 pass/0 fail incl. new test-navigation-review-advance.cjs (20 tests) and updated v2->v3 + settle-window ticks in 4 existing files. epic-symbols clean. Vault deploy pending: bob plugins sync deploys from the canonical checkout, so land agent must carry the workspace diff over and sync.

## Dependencies

- **Blocks:** [bob-cli-4l.2](bob-cli-4l.2.md) ◐ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4l.3](bob-cli-4l.3.md) ◐ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4l.4](bob-cli-4l.4.md) ◐ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4l.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4l.1/README.md) | [bob-cli-4l.1](bob-cli-4l.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@824ad2a`](https://github.com/bobs-org/bob-plugins/commit/824ad2a5bd514c710244319c75f0e46bda7c2463) | feat(review-walk): nav-core auto-advance, shared tail, nav api v3 (nav 2.5.0) | [bob-cli-4l.1](bob-cli-4l.1.md) | 2026-10-06 07:23:00 EDT |
