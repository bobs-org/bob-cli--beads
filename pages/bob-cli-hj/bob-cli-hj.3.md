# Bead: bob-cli-hj.3 — Record pinned runs end to end and ship grammar 14

[Bead Pages](../README.md) / [bob-cli-hj](README.md) / bob-cli-hj.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18s.md) · **Assignee:** `bob-cli-hj.3` · **Size:** medium
**Created:** 2026-11-05 14:25:24 EST · **Closed:** 2026-11-05 17:41:19 EST
**Plan:** [202611/past\_pomodoro\_segment\_suffix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/past_pomodoro_segment_suffix.md)

## Description

record: wire the timeline and layout into plan.rs for pinned runs (snapshot first, unpinned runs untouched), add guard hints and the same-capture trim rule, report segment and cut in capture JSON and human output, document the feature, and bump the grammar to 14.

## Notes

[2026-11-05T22:41:08Z · bob-cli-hj.3] PROPOSED FOLLOW-UP: just check clippy gate fails on pre-existing src/native/gmail/body/mime.rs derivable_impls (untouched by this phase; same bytes as base)

[2026-11-05T22:41:19Z · bob-cli-hj.3] Pinned x= segments record end to end at grammar 14: timeline+layout wiring with snapshot-first pinned path, guard fit/carve hints and same-capture refusal, segment/pin/cut JSON and human clauses, docs updated, 9 new segment tests green with existing past/parse suites and docs-check/docs-reference green

## Dependencies

- **Depends on:** [bob-cli-hj.1](bob-cli-hj.1.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hj.2](bob-cli-hj.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hj.4](bob-cli-hj.4.md) ◐ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hj.5](bob-cli-hj.5.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.3/README.md) | [bob-cli-hj.3](bob-cli-hj.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`86554bf`](https://github.com/bobs-org/bob-cli/commit/86554bf66551e6f44dd269295cfca19eba570a65) | feat(capture): record pinned past-Pomodoro segments and ship grammar 14 | [bob-cli-hj.3](bob-cli-hj.3.md) | 2026-11-05 17:42:43 EST |
