# Bead: bob-cli-31.3 — bob capture stamps the existing tasks it rewrites

[Bead Pages](../README.md) / [bob-cli-31](README.md) / bob-cli-31.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.v.linker.w0.md) · **Assignee:** `bob-cli-31.3` · **Size:** medium
**Created:** 2026-09-30 19:32:05 EDT · **Closed:** 2026-09-30 20:22:03 EDT
**Plan:** [202609/task\_freshness\_review.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_freshness_review.md)

## Description

capture-stamps: plan_task_link and the =x in-progress close stamp fresh in the same write; creation never stamps; hooks preserve the field; docs and tests updated.

## Notes

[2026-10-01T00:21:35Z · bob-cli-31.3] PROPOSED FOLLOW-UP: Pre-existing clippy deny (overly_complex_bool_expr) at tests/cli/capture/pomodoro_name.rs:808 (`|| true`) reproduces on clean HEAD; unrelated to capture-stamps, needs cleanup

[2026-10-01T00:21:42Z · bob-cli-31.3] PROPOSED FOLLOW-UP: Verify Bob Mac Capture rendering of capture JSON task_line/previous_task_line now carrying [fresh:: ...]; if it shows the raw line, strip or clean the stamp for display (capture-stamps left the Mac app unchanged per plan)

[2026-10-01T00:22:03Z · bob-cli-31.3] plan_task_link stamps rewritten lines via freshness::stamp_fresh (byte-identical Next/In-Progress leaves note untouched; recurring/closed refusals leave line as-is); ClosePlanner::apply_startable stamps [/] with close date after normalize_task_metadata_spacing. Verified: 405 capture CLI tests pass incl new freshness_stamps (7 tests: Ready/Blocked link stamps, Next/In-Progress no-op vs retire-schedule, recurring refusal, same-day idempotent, =x [/] stamps vs [x] no stamp, creation never stamps); task_status_hooks 81 pass (checkbox-byte swap preserves fresh); other capture paths audited (creation/sub-bullet/start/work-log/randomize untouched). Docs: one sentence each in capture.md toggle, Ensure Next, =x sections. No epic symbols.

## Dependencies

- **Depends on:** [bob-cli-31.1](bob-cli-31.1.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.10](bob-cli-31.10.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-31.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-31.3/README.md) | [bob-cli-31.3](bob-cli-31.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3cd4d44`](https://github.com/bobs-org/bob-cli/commit/3cd4d44290857815d6d6596ed307a54eca2456e7) | feat(capture): stamp freshness on rewritten tasks | [bob-cli-31.3](bob-cli-31.3.md) | 2026-09-30 20:23:52 EDT |
