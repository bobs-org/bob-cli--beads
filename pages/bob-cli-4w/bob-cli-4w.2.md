# Bead: bob-cli-4w.2 — Managed-region and note-anatomy parser

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.2` · **Size:** small
**Created:** 2026-10-06 20:15:52 EDT · **Closed:** 2026-10-06 20:46:05 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

region: a read-only parser for rendered ref-note bodies (annotation blocks with quote and comment kept apart, tombstones, mirror and preamble detection, the user's own notes, and the Tasks section), round-tripped against the renderer.

## Notes

[2026-10-07T00:45:46Z · bob-cli-4w.2] PROPOSED FOLLOW-UP: just-all listen-card test failure is pre-existing on clean base, already tracked by bob-cli-4u

[2026-10-07T00:45:50Z · bob-cli-4w.2] PROPOSED FOLLOW-UP: just-all every_value_arg_has_a_decision failure (highlights create --audio) is pre-existing on clean base, already tracked by bob-cli-4j

[2026-10-07T00:46:05Z · bob-cli-4w.2] region.rs parser done: parse_managed_region + split_note_body + is_marker_mirror_text, 10 round-trip tests pass, real-vault probe 595 notes/0 unparsed; just fmt+clippy clean, lib tests 1770 pass with only the 2 pre-existing base failures (tracked by bob-cli-4u, bob-cli-4j)

## Dependencies

- **Blocks:** [bob-cli-4w.3](bob-cli-4w.3.md) ◐ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.8](bob-cli-4w.8.md) ◐ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.2/README.md) | [bob-cli-4w.2](bob-cli-4w.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ecabc33`](https://github.com/bobs-org/bob-cli/commit/ecabc336ac35611458ce98004a6ece415d7314f2) | feat(highlights\_ref): add read-only managed region parser | [bob-cli-4w.2](bob-cli-4w.2.md) | 2026-10-06 20:48:52 EDT |
