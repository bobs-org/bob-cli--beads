# Bead: bob-cli-4l.2 — Alt+N, Task Card, and Ctrl+Shift+M advance from a landing

[Bead Pages](../README.md) / [bob-cli-4l](README.md) / bob-cli-4l.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0d.linker.w0.md) · **Assignee:** `bob-cli-4l.2` · **Size:** medium
**Created:** 2026-10-06 07:01:40 EDT · **Closed:** 2026-10-06 07:40:10 EDT
**Plan:** [202610/review\_walk\_answer\_auto\_advance.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/review_walk_answer_auto_advance.md)

## Description

nav-gestures: wire nav's own answering gestures through the core. This covers Alt+N commit/release (single, counted, and the Pending Work Log prompt), every committing Task Card stage (decided from the line after the write, with the cancel route's late notice handled), and Ctrl+Shift+M move, which advances instead of focusing the destination (nav 2.6.0).

## Notes

[2026-10-06T11:40:10Z · bob-cli-4l.2] nav-gestures wired through the nav-core capture/continue API (nav 2.6.0): Alt+N commit/release settles lane outcomes incl. counted batches and cancelled-prompt stay; Task Card captures on the plain task-line path with idempotent onClose settle and deferred cancel-route settle (cancel card precedes landing toast); Ctrl+Shift+M advances instead of focusing from lane landings and keeps focus on checklist/off-landing. Verified: new scripts/test-navigation-review-advance-gestures.cjs (16 tests) green, full bob-plugins suite 1845/1845 green, build:check clean, bob plugins sync done.

## Dependencies

- **Depends on:** [bob-cli-4l.1](bob-cli-4l.1.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4l.5](bob-cli-4l.5.md) ◐ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4l.2/README.md) | [bob-cli-4l.2](bob-cli-4l.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f100300`](https://github.com/bobs-org/bob-plugins/commit/f100300baac583b00b69516c8a1d073834f75519) | feat(nav): advance review walk from Alt+N, Task Card, and Ctrl+Shift+M landings | [bob-cli-4l.2](bob-cli-4l.2.md) | 2026-10-06 07:42:50 EDT |
