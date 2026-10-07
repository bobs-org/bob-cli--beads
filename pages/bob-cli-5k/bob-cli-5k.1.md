# Bead: bob-cli-5k.1 — Fix the deterministic red tests

[Bead Pages](../README.md) / [bob-cli-5k](README.md) / bob-cli-5k.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0y2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y2.md) · **Assignee:** `bob-cli-5k.1` · **Size:** small
**Created:** 2026-10-07 14:38:40 EDT · **Closed:** 2026-10-07 15:00:26 EDT
**Plan:** [202610/close\_top\_ten\_impact\_beads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/close_top_ten_impact_beads.md)

## Description

red-tests: give `ref create --audio` a completion decision (bob-cli-4j), confirm the stale `clip` help snapshot is fixed (bob-cli-5i), and make the listen-card test accept both Pandoc ampersand escapings without losing URI coverage (bob-cli-4u); close all three.

## Notes

[2026-10-07T19:00:18Z · bob-cli-5k.1] Sibling-phase failure, not mine: cargo test --no-fail-fast on athena atop 6244ddd shows 1 lib failure in native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes, which passes in isolation -- the known BOB_DAY_FILE env race owned by the env-isolation phase (bob-cli-2e). All 1159 CLI tests pass. Change left uncommitted (2 files, +14) for landing.

[2026-10-07T19:00:26Z · bob-cli-5k.1] red-tests done on athena atop 6244ddd, pandoc 3.1.11.1: 4j fixed (FilePath hint + !files protocol proof), 5i verified already-fixed at HEAD (snapshot green, hidden alias works), 4u fixed (both ampersand forms accepted, URI coverage kept, hyperref equivalence proven by compile). Full gate: lib 1875/1876 (sole failure is bob-cli-2e's known env race, passes solo), cli 1159/1159, all other binaries green, clippy no errors, fmt clean. No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-5k.3](bob-cli-5k.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.1/README.md) | [bob-cli-5k.1](bob-cli-5k.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a5bb9ae`](https://github.com/bobs-org/bob-cli/commit/a5bb9aeb350d0de12299580f151cee122318257d) | fix(red-tests): resolve owned check failures for 4j, 5i, 4u | [bob-cli-5k.1](bob-cli-5k.1.md) | 2026-10-07 15:01:58 EDT |
