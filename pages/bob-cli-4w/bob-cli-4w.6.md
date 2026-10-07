# Bead: bob-cli-4w.6 — bob ref show

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.6` · **Size:** medium
**Created:** 2026-10-06 20:15:53 EDT · **Closed:** 2026-10-06 23:24:02 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

show: exact resolution of one or more references and their metadata, annotations (quote and comment kept apart), the user's own notes, and tasks, as human, Markdown digest, or JSON.

## Notes

[2026-10-07T03:23:41Z · bob-cli-4w.6] PROPOSED FOLLOW-UP: Pre-existing lib failures reproduce identically on clean base (3642b4a): every_value_arg_has_a_decision on ref create:audio (tracked by bob-cli-4j) and listen_filter_renders_card_and_encoded_play_link (tracked by bob-cli-4u); leave both to their beads

[2026-10-07T03:23:45Z · bob-cli-4w.6] PROPOSED FOLLOW-UP: Parallel-run flakes vary between runs and pass isolated with --exact: capture_pomodoros missing_note_and_missing_section_are_warning_successes failed on show tree while note_ready scan_excludes_r3_and_r7_paths failed on clean base; consider flake task beads if they recur

[2026-10-07T03:24:02Z · bob-cli-4w.6] bob ref show implemented per plan: exact REF resolution (path/stem/id/URL/arXiv/DOI/title_exact, superseded collapse to live note with also, ambiguous/multi-match and miss errors with candidates, all REFs resolved before output), JSON row extensions (annotations_status/raw_region/annotations/excluded/own_notes/tasks/also), human/Markdown/JSON output, -c/-N flags, help group + example, VaultNote completion, docs/ref.md show section. Verified: cargo fmt clean, clippy exit 0 (no new warnings), cargo test --test cli 1107/1107 pass (incl 17 new show tests + 3 new unit tests); lib has only pre-existing failures also failing on clean base (bob-cli-4j audio, bob-cli-4u listen, recorded as follow-ups). No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-4w.10](bob-cli-4w.10.md) ◐ · ⧖ 2026-10-06
- **Depends on:** [bob-cli-4w.5](bob-cli-4w.5.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.6/README.md) | [bob-cli-4w.6](bob-cli-4w.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e3e69df`](https://github.com/bobs-org/bob-cli/commit/e3e69dfd24c714ad8840ebcc3b806a3b10257848) | feat(ref): add bob ref show with exact resolution and rich row output | [bob-cli-4w.6](bob-cli-4w.6.md) | 2026-10-06 23:26:16 EDT |
