# Bead: bob-cli-4w.3 — Read-only ref index, reading state, and identity

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.3` · **Size:** medium
**Created:** 2026-10-06 20:15:52 EDT · **Closed:** 2026-10-06 21:19:35 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

index: a new `ref_library` module that builds one read-only row per ref note (status precedence, derived reading state, identity keys, dates, origin, supersession, diagnostics, coverage) plus query resolution and title scoring, over a mixed-corpus fixture vault.

## Notes

[2026-10-07T00:56:12Z · bob-cli-4w.3] PROPOSED FOLLOW-UP: placeholder to verify tool

[2026-10-07T00:56:25Z · bob-cli-4w.3] Retract note #1 placeholder: not a follow-up, ignore it during triage

[2026-10-07T01:19:16Z · bob-cli-4w.3] PROPOSED FOLLOW-UP: every_value_arg_has_a_decision (create:audio) fails identically on clean base — tracked by bob-cli-4j

[2026-10-07T01:19:20Z · bob-cli-4w.3] PROPOSED FOLLOW-UP: listen-card render test fails identically on clean base — tracked by bob-cli-4u

[2026-10-07T01:19:24Z · bob-cli-4w.3] PROPOSED FOLLOW-UP: capture_pomodoros warning test (and note_ready scan_excludes) flake under parallel cargo test on clean base too — tracked by bob-cli-40

[2026-10-07T01:19:35Z · bob-cli-4w.3] ref_library module done: build_index over 32-row fixture vault (3 skips), 25 index tests + 2 seam tests pass; fmt clean, clippy exit 0, full suite green except 2 deterministic + intermittent parallel flakes that reproduce identically on clean base (tracked by bob-cli-4j, bob-cli-4u, bob-cli-40, recorded as follow-ups)

## Dependencies

- **Depends on:** [bob-cli-4w.2](bob-cli-4w.2.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.4](bob-cli-4w.4.md) ◐ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.7](bob-cli-4w.7.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.3/README.md) | [bob-cli-4w.3](bob-cli-4w.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7b60ded`](https://github.com/bobs-org/bob-cli/commit/7b60ded9f056f240f7e0d3db1ae4707a4ab9aab3) | feat(ref-library): add read-only RefRow index module with fixture vault | [bob-cli-4w.3](bob-cli-4w.3.md) | 2026-10-06 21:21:22 EDT |
