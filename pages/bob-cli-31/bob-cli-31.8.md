# Bead: bob-cli-31.8 — Status cycling and Task Link gestures stamp freshness

[Bead Pages](../README.md) / [bob-cli-31](README.md) / bob-cli-31.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.v.linker.w0.md) · **Assignee:** `bob-cli-31.8` · **Size:** medium
**Created:** 2026-09-30 19:32:06 EDT · **Closed:** 2026-09-30 22:37:30 EDT
**Plan:** [202609/task\_freshness\_review.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_freshness_review.md)

## Description

cycler-link-stamps: task-status-cycler (Alt+[ / Alt+] to an open status, leaving Blocked, reopening) and block-id-prompt (Ctrl+Shift+Enter and ^^ when they rewrite the task line) stamp through api.freshness.stampLine.

## Notes

[2026-10-01T02:37:19Z · bob-cli-31.8] PROPOSED FOLLOW-UP: cycler Tasks-command path stamps in a follow-up editor edit rather than the same write (undo granularity); consider a single-transaction stamp if Tasks exposes a hook

[2026-10-01T02:37:30Z · bob-cli-31.8] cycler-link-stamps landed: task-status-cycler 1.18.0 and block-id-prompt 1.16.0 stamp via api.freshness.stampLine (ledger-tools v3, injected stamper with identity default); 12 new tests, full npm test 906 pass, validate 6/6 valid, both plugins synced to vault, docs/freshness.md Surfaces rows marked landed; new tests fail 9/12 on base (3 pin unchanged defaults)

## Dependencies

- **Blocks:** [bob-cli-31.10](bob-cli-31.10.md) ◐ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-31.5](bob-cli-31.5.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-31.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-31.8/README.md) | [bob-cli-31.8](bob-cli-31.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`779cc0c`](https://github.com/bobs-org/bob-cli/commit/779cc0caa8169f3d2799d5d6cb30f2e475d50c85) | docs(freshness): mark cycler-link-stamps surfaces landed | [bob-cli-31.8](bob-cli-31.8.md) | 2026-09-30 22:40:31 EDT |
