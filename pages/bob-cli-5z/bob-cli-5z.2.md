# Bead: bob-cli-5z.2 — Execute restarts and the idle fallback, with the override JSON contract

[Bead Pages](../README.md) / [bob-cli-5z](README.md) / bob-cli-5z.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.61.w1.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.61.w1.w0.md) · **Assignee:** `bob-cli-5z.2` · **Size:** medium
**Created:** 2026-10-09 13:24:48 EDT · **Closed:** 2026-10-09 14:13:49 EDT
**Plan:** [202610/pomodoro\_override.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_override.md)

## Description

override-restart: route override starts in the executor, run the idle fallback, restart the running session in place with fresh `se<X>` timing, introduce the full `pomodoro_start.override` JSON object and `restarted` human output, and start the new docs section.

## Notes

[2026-10-09T18:12:47Z · bob-cli-5z.2] PROPOSED FOLLOW-UP: 9 pre-existing lib failures in highlights_ref::return_links reproduce identically on the clean base tree (verified via stash); unrelated to override-restart

[2026-10-09T18:13:49Z · bob-cli-5z.2] override-restart done: unnamed == restarts running session in place with fresh se<X> timing (drops, byte-safe ledger splice, current-slot move), idle fallback acts exactly like = twin, pomodoro_start.override JSON (restart/fresh+previous, start/fresh), restarted/would-restart human output plus idle note, ==<X> teaching hint on unnamed still-running error, docs section plus lifecycle row and mnemonic. Verified: 9 new pomodoro_override tests pass, 48 neighboring start tests pass, 117 chain/reset/close/parse tests pass, fmt clean, clippy has no new warnings; 9 highlights_ref lib failures reproduce identically on clean base (recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-5z.1](bob-cli-5z.1.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5z.3](bob-cli-5z.3.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5z.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5z.2/README.md) | [bob-cli-5z.2](bob-cli-5z.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`36df8b8`](https://github.com/bobs-org/bob-cli/commit/36df8b8afed540db39962472d83a153e5c3dbfb9) | feat(capture): execute == restarts with idle fallback and override JSON contract | [bob-cli-5z.2](bob-cli-5z.2.md) | 2026-10-09 14:15:02 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5z.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5z.2/README.md

<!-- sase:referenced-by:end -->
