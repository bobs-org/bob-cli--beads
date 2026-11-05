# Bead: bob-cli-hc.3 — bob types rename and split cover offclock\_types lists

[Bead Pages](../README.md) / [bob-cli-hc](README.md) / bob-cli-hc.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3c.linker.w0.md) · **Assignee:** `bob-cli-hc.3` · **Size:** medium
**Created:** 2026-11-05 10:03:54 EST · **Closed:** 2026-11-05 12:30:13 EST
**Plan:** [202611/offclock\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/offclock_types.md)

## Description

type-rename-coverage: `bob types rename` rewrites matching `offclock_types` items in flow, block, and scalar form inside its existing previewed transaction, removing duplicates when two types merge; `split` leaves the lists alone and counts them in its leftover warning; update docs/task-types.md.

## Notes

[2026-11-05T17:30:05Z · bob-cli-hc.3] PROPOSED FOLLOW-UP: just check flake capture::related::draft_related_stays_under_the_debug_perf_gate failed once on timing (604ms vs baseline) then passed on retry; unrelated to offclock rename work

[2026-11-05T17:30:13Z · bob-cli-hc.3] type-rename-coverage done: rename rewrites offclock_types scalar/flow/block with merge dedupe (block drops line), split counts offclock lists in leftover warning, docs/task-types.md updated. Verified: 16 coverage unit tests, 27 themes_rename/split CLI tests, just lint/fmt clean, just docs-check green, full workspace tests green except one unrelated perf-gate flake that passed on retry.

## Dependencies

- **Depends on:** [bob-cli-hc.1](bob-cli-hc.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hc.5](bob-cli-hc.5.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hc.3/README.md) | [bob-cli-hc.3](bob-cli-hc.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`832e124`](https://github.com/bobs-org/bob-cli/commit/832e124645585118f9c7e42633e05814f70ec59c) | feat(types): cover offclock lists in rename and split | [bob-cli-hc.3](bob-cli-hc.3.md) | 2026-11-05 12:31:33 EST |
