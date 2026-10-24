# Bead: bob-cli-bc.6 — Global theme rename transaction

[Bead Pages](../README.md) / [bob-cli-bc](README.md) / bob-cli-bc.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2c.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2c.linker.w1.md) · **Assignee:** `bob-cli-bc.6` · **Size:** medium
**Created:** 2026-10-24 07:52:22 EDT · **Closed:** 2026-10-24 10:20:28 EDT
**Plan:** [202610/pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_themes.md)

## Description

rename: implement the previewed, verified, single-commit rename modeled on `bob ref rename`, with refusals and reappearance detection.

## Notes

[2026-10-24T14:20:16Z · bob-cli-bc.6] PROPOSED FOLLOW-UP: highlights continuations scan tests fail on clean base (continuation_scan_reports_dangling_marker, continuation_scan_tucks_two_pages_and_is_idempotent) — pre-existing, unrelated to themes rename

[2026-10-24T14:20:28Z · bob-cli-bc.6] Implemented bob themes rename (PT10): previewed dry-run, verified single-commit transaction with journal append, cache invalidate, and renamed_reappeared in list. Verified: 20 themes tests pass (5 rename incl. collapse/template/fenced/future, refusals, lock, dirty, not_a_worktree, config_reference, revert restores bytes, one commit); cargo fmt clean, clippy clean, just docs-check passes. Pre-existing highlights continuations failures recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-bc.11](bob-cli-bc.11.md) ◐ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bc.3](bob-cli-bc.3.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bc.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.6/README.md) | [bob-cli-bc.6](bob-cli-bc.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4a6f449`](https://github.com/bobs-org/bob-cli/commit/4a6f4494fdfb8a40c2d7c0e002040b52f37b2014) | feat(themes): add global theme rename transaction | [bob-cli-bc.6](bob-cli-bc.6.md) | 2026-10-24 10:21:49 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.2][1] | Identify the existing owner and task evidence for clean-base just check failures | 1 |
| read-by | [agent:bob-cli-bc.6][2] | Verify phase scope before closing rename work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-an.6.6.6.5.6.5.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.6/README.md

<!-- sase:referenced-by:end -->
