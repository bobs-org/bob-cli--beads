# Bead: bob-cli-4w.9 — Capture URLs that only a legacy note records

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.9` · **Size:** small
**Created:** 2026-10-06 20:15:53 EDT · **Closed:** 2026-10-06 21:26:43 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

legacy-capture: shared dedupe refuses only PDF-backed note hits, so a URL recorded only by a legacy note captures with a warning instead of hitting the dead end introduced by the bob-cli-4s legacy `url:` dedupe.

## Notes

[2026-10-07T01:26:32Z · bob-cli-4w.9] PROPOSED FOLLOW-UP: full-suite runs show 2 pre-existing lib failures that reproduce identically on the clean base tree: completion kinds every_value_arg_has_a_decision (ref create:audio, the known bob-cli-4j failure named in the epic plan) and create listen_filter_renders_card_and_encoded_play_link; plus 2 flakes that pass in isolation (capture_pomodoros missing_note warning test, completion bash readline PTY test).

[2026-10-07T01:26:43Z · bob-cli-4w.9] legacy-capture done: shared dedupe refuses only PDF-backed ref-note hits; legacy-only URLs warn (already in the library as <path>, capturing a fresh copy) and capture on every URL route, with legacy: <path> (superseded by this capture) in dry runs and no --listen attach. Verified: 4 sources unit tests, 14 clip + 3 arxiv-create + 22 listen CLI tests green; fmt clean; clippy has only the pre-existing unused-import warning; full lib/cli suites show only clean-tree-identical failures (recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-4w.1](bob-cli-4w.1.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.10](bob-cli-4w.10.md) ◐ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.9/README.md) | [bob-cli-4w.9](bob-cli-4w.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a34dc02`](https://github.com/bobs-org/bob-cli/commit/a34dc026c04ed47ae0119e6100bad774c5b2dc7d) | feat(ref): capture URLs recorded only by legacy notes with a warning | [bob-cli-4w.9](bob-cli-4w.9.md) | 2026-10-06 21:27:49 EDT |
