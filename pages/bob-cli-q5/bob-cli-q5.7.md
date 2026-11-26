# Bead: bob-cli-q5.7 — Mac Later-today band, woken accents, and exact-minute waker

[Bead Pages](../README.md) / [bob-cli-q5](README.md) / bob-cli-q5.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fx.md) · **Assignee:** `bob-cli-q5.7` · **Size:** large
**Created:** 2026-11-25 10:22:53 EST · **Closed:** 2026-11-26 12:44:22 EST
**Plan:** [202611/snoozed\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md)

## Description

mac-agenda: decode the additive snoozed/woke_at agenda fields, add a dim Later-today band that folds first, woken-row accents, a snoozed count on the budget row, z: span styling, and an always-on scheduler that runs bob snooze wake at next_wake_at.

## Notes

[2026-11-26T17:45:14Z · bob-cli-q5.7.1.land--4] Parent-phase closeout: child epic bob-cli-q5.7.1 landed the full mac-agenda scope on Mac 46c5202b == origin/master (bob-cli clean). Verified: additive snoozed/woke_at decoding, snooze-span tint, dim Later-today band after strip with first-fold persistent summary, separate budget alarm N, 60-min fresh-woke accents, hidden-panel +5s non-cancelling snooze-wake lane with bounded 60s retries and day/clock/lifecycle invalidation. Evidence: portable-check 2846/1-skip PASS, scratch bundle+typecheck PASS, precommit gate 9ntrn9ejrj7d exit 0 snapshot 40f15ef41c85c63cd7eeb6c4b8e0bd8ceff252ac run https://github.com/bobs-org/bob-mac-capture/actions/runs/45865004175. epic-symbols clean. Outer bob-cli-q5 left open for its land agent; snoozed_tasks plan stays open.

## Dependencies

- **Depends on:** [bob-cli-q5.2](bob-cli-q5.2.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q5.3](bob-cli-q5.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.8](bob-cli-q5.8.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.md) | [bob-cli-q5.7](bob-cli-q5.7.md) | 0 |
