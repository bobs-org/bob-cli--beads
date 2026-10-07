# Bead: bob-cli-4w.5 — bob ref list

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.5` · **Size:** medium
**Created:** 2026-10-06 20:15:53 EDT · **Closed:** 2026-10-06 22:50:29 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

list: the reading queue by default and filtered library views (reading state, status, type, origin, parent, since), with a consistent cap, opt-in Git dates, and grouped human output.

## Notes

[2026-10-07T02:49:25Z · bob-cli-4w.5] PROPOSED FOLLOW-UP: lib test every_value_arg_has_a_decision fails on clean base for ref create:audio (tracked by bob-cli-4j); left alone per plan

[2026-10-07T02:49:29Z · bob-cli-4w.5] PROPOSED FOLLOW-UP: lib test listen_filter_renders_card_and_encoded_play_link fails identically on clean base (create.rs LaTeX card assertion); unrelated to ref list

[2026-10-07T02:50:17Z · bob-cli-4w.5] PROPOSED FOLLOW-UP: lib test capture_pomodoros missing_note_and_missing_section_are_warning_successes flaked once in full-lib run, passes alone; unrelated area, needs a re-run to confirm

[2026-10-07T02:50:29Z · bob-cli-4w.5] bob ref list ships: queue default, all filters, ordering, limit/-A, legacy collapse, git dates; 37 CLI + 35 lib ref_library tests green, fmt/clippy clean; 2 lib failures repro on base (bob-cli-4j, listen_filter) recorded as follow-ups

## Dependencies

- **Depends on:** [bob-cli-4w.4](bob-cli-4w.4.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.6](bob-cli-4w.6.md) ◐ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.5/README.md) | [bob-cli-4w.5](bob-cli-4w.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3642b4a`](https://github.com/bobs-org/bob-cli/commit/3642b4a5c10753bd2013e12eb804a6bd4b74b36d) | feat(ref): add bob ref list reading-queue and filtered library views | [bob-cli-4w.5](bob-cli-4w.5.md) | 2026-10-06 22:56:16 EDT |
