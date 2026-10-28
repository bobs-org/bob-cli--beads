# Bead: bob-cli-df.4.1.2 — Protect reset-and-replay operations

[Bead Pages](../README.md) / [bob-cli-df.4.1](bob-cli-df.4.1.md) / bob-cli-df.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.md) · **Assignee:** `bob-cli-df.4.1.2` · **Size:** medium
**Created:** 2026-10-27 21:39:19 EDT · **Closed:** 2026-10-27 22:58:05 EDT
**Plan:** [202610/preserve\_failed\_close\_worktrees.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/preserve_failed_close_worktrees.md)

## Description

reset-replay: snapshot before abort/reset, preserve recovery locations through success and every failure exit, and prove tracked plus untracked recovery with real Git repositories.

## Notes

[2026-10-28T02:57:51Z · bob-cli-df.4.1.2--1] PROPOSED FOLLOW-UP: Remove stale Symvision epic-symbol entries for sase-1p1(other_id) and sase-1p1(custom_id) — required check failed on these entries, and the exact lint command reproduced both failures on clean SASE HEAD 42512dc116; monitor triage reported no owner.

[2026-10-28T02:58:05Z · bob-cli-df.4.1.2--1] Verified focused reset-replay and archive-recovery tests: 36 passed. Required sase tool run check passed all prior stages but failed Symvision on stale sase-1p1 epic-symbol entries for other_id and custom_id; exact lint command reproduced both on clean SASE HEAD 42512dc116. Recorded the unrelated lint follow-up; epic-symbol check is clear.

## Dependencies

- **Depends on:** [bob-cli-df.4.1.1](bob-cli-df.4.1.1.md) ✓ · ⧖ 2026-10-27
- **Blocks:** [bob-cli-df.4.1.4](bob-cli-df.4.1.4.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.2.md) | [bob-cli-df.4.1.2](bob-cli-df.4.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.2][1] | Cite existing stale epic-symbol follow-up | 1 |
| read-by | [agent:bob-cli-df.4.1.2--1][2] | Need the phase scope, design file, and recorded remaining work | 2 |
| read-by | [agent:bob-cli-df.4.1.3][3] | Check sibling phase status to avoid duplicating reset-replay work | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.2.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md

<!-- sase:referenced-by:end -->
