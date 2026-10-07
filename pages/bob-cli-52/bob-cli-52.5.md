# Bead: bob-cli-52.5 — Ref job spool, background worker, and bob ref jobs

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.5` · **Size:** medium
**Created:** 2026-10-07 08:11:17 EDT · **Closed:** 2026-10-07 10:02:23 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

jobs: the durable job spool under the bob-cli state directory; a single-flight worker that is crash-safe and has no lost wakeups; its fully detached kick; the lossless inbox-task fallback writer; `bob ref jobs` (bare = list) and `bob ref jobs run`; doctor rows; and `docs/ref-jobs.md`.

## Notes

[2026-10-07T14:01:54Z · bob-cli-52.5] PROPOSED FOLLOW-UP: completion kinds lacks a decision for ref create --audio (every_value_arg_has_a_decision fails identically on the clean base tree)

[2026-10-07T14:01:59Z · bob-cli-52.5] PROPOSED FOLLOW-UP: create listen_filter unit test fails identically on the clean base tree (BobListenCard LaTeX mismatch)

[2026-10-07T14:02:03Z · bob-cli-52.5] PROPOSED FOLLOW-UP: ingest_characterizes missing-uv case fails identically on the clean base tree (fetch 404 before uv check on machines with ~/.local/bin/uv)

[2026-10-07T14:02:07Z · bob-cli-52.5] PROPOSED FOLLOW-UP: capture_pomodoros missing_note and note_ready r3/r7 tests flake under parallel load on the clean base tree too, pass solo (same class as known parallel flake bob-cli-40)

[2026-10-07T14:02:23Z · bob-cli-52.5] Ref job spool, single-flight worker, detached kick, fallback writer, bob ref jobs (bare=list) + run, doctor row, docs/ref-jobs.md all land per phase jobs. Verified: 15 new unit tests + 11 new CLI tests pass; cargo fmt/clippy clean; full cargo test green except 3 failures reproduced identically on the clean base tree (filed as PROPOSED FOLLOW-UP notes). No epic-symbol leftovers. One deliberate plan deviation: kick uses pre_exec setsid WITHOUT process_group(0) (combined form makes the child a group leader so setsid fails; unit test proves the new session).

## Dependencies

- **Depends on:** [bob-cli-52.1](bob-cli-52.1.md) ✓ · ⧖ 2026-10-07
- **Depends on:** [bob-cli-52.3](bob-cli-52.3.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.7](bob-cli-52.7.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.5/README.md) | [bob-cli-52.5](bob-cli-52.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f4fb812`](https://github.com/bobs-org/bob-cli/commit/f4fb812ad58cb8748f7bfe73036f9ddbf6461e79) | feat(ref-jobs): background clip queue for reading-queue links | [bob-cli-52.5](bob-cli-52.5.md) | 2026-10-07 10:08:25 EDT |
