# Bead: bob-cli-h2.4 — Whole-stack overlap guard and ! edge repair

[Bead Pages](../README.md) / [bob-cli-h2](README.md) / bob-cli-h2.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.38.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.38.linker.w0.md) · **Assignee:** `bob-cli-h2.4` · **Size:** medium
**Created:** 2026-11-04 11:11:57 EST · **Closed:** 2026-11-04 15:30:06 EST
**Plan:** [202611/past\_pomodoro\_recording.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/past_pomodoro_recording.md)

## Description

guard: replace the strict guard with the full per-token `!` rules. Running sessions are protected, the whole stack is validated at once, erase and split are refused, and closed-row edges are trimmed with warnings. Pin the user's five examples end to end.

## Notes

[2026-11-04T20:29:56Z · bob-cli-h2.4] PROPOSED FOLLOW-UP: just lint gate fails on clean-tree files untouched by h2.4 (editor_pomodoro.rs needless_return/collapsible_if/question_mark, past.rs bool logic) under clippy 1.95; h2.4 files pass the gate

[2026-11-04T20:30:06Z · bob-cli-h2.4] Whole-stack guard with per-token !, edge trims staged atomically, JSON trims/warnings/trimmed blocks, human trim lines, five examples pinned; verified 20 pomodoro_past CLI tests + trimmed-MEET gcal regression pass, cargo check clean; just lint blocked by pre-existing gate errors in untouched grammar files (recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-h2.3](bob-cli-h2.3.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h2.5](bob-cli-h2.5.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-h2.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h2.4/README.md) | [bob-cli-h2.4](bob-cli-h2.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`399b522`](https://github.com/bobs-org/bob-cli/commit/399b52221409f4c37536530d7d56067f1d4f4f4f) | feat(capture)!: whole-stack overlap guard and past edge repair | [bob-cli-h2.4](bob-cli-h2.4.md) | 2026-11-04 15:31:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h2.4][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-h2.5][2] | Check existing follow-up ownership of the clean-base clippy failure | 1 |
| read-by | [agent:bob-cli-h3.land--1][3] | Determine which active Pomodoro epic phases own the Rust files flagged by canonical formatting verification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h2.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h2.5/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-h3.land.md

<!-- sase:referenced-by:end -->
