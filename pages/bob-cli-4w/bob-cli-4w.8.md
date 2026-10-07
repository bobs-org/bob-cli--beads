# Bead: bob-cli-4w.8 — Remove leaked marker mirrors and stamp completion dates

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.8` · **Size:** medium
**Created:** 2026-10-06 20:15:53 EDT · **Closed:** 2026-10-06 21:38:38 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

sync-fixes: fix bob-cli-4r so neither sidecar preambles nor marker mirrors render as annotations, drop previously leaked blocks without tombstones while keeping every genuine block ID stable, and stamp completion or cancellation dates when sync closes a `^ref` task.

## Notes

[2026-10-07T01:38:14Z · bob-cli-4w.8] PROPOSED FOLLOW-UP: lib test listen_filter_renders_card_and_encoded_play_link fails identically on clean base (verified via git stash); pre-existing, unrelated to sync-fixes

[2026-10-07T01:38:18Z · bob-cli-4w.8] PROPOSED FOLLOW-UP: lib test completion::kinds every_value_arg_has_a_decision fails identically on clean base (verified via git stash); pre-existing, unrelated to sync-fixes

[2026-10-07T01:38:38Z · bob-cli-4w.8] sync-fixes done. Mirror/preamble: sidecar preamble skipped at parse, content-based mirror skip in render+intake (region::is_marker_mirror_text), leaked mirror/preamble blocks drop without tombstones while genuine losses still tombstone and genuine IDs render byte-identical with/without preamble (unit: setext_preamble_*, leaked_mirror_and_preamble_blocks_drop_silently_*, region_round_trip update; CLI: highlights_ref_sync_drops_leaked_mirror_without_tombstone incl. dry-run/update/no-tombstone/settle). Dates: generated [x]/[-] lines stamped [completion::]/[cancelled::] before ^ref from BOB_NOW clock, existing/emoji dates preserved, user closes untouched, reopens keep dates, dirty guard compares stamp-free (unit: close_date_stamp_* + rewrite updates; CLI: stamps_completion/cancellation + reopen-test updates); docs/highlights-ref-sync.md updated. Gate: cargo fmt clean, clippy no errors, CLI 1047/1047 green, lib green except 2 failures verified pre-existing on clean base (recorded as PROPOSED FOLLOW-UP). Closed bob-cli-4r as resolved. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-4w.1](bob-cli-4w.1.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.11](bob-cli-4w.11.md) ◐ · ⧖ 2026-10-06
- **Depends on:** [bob-cli-4w.2](bob-cli-4w.2.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.8/README.md) | [bob-cli-4w.8](bob-cli-4w.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`eaca8b1`](https://github.com/bobs-org/bob-cli/commit/eaca8b14ef506bcc48a282218eb6944561a13efd) | feat(highlights-ref): sync fixes — discard leaked marker mirrors, stamp close dates | [bob-cli-4w.8](bob-cli-4w.8.md) | 2026-10-06 21:39:57 EDT |
