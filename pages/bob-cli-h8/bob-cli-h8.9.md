# Bead: bob-cli-h8.9 — Brief truncation counts, Bryan's words, and Markdown glitches

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.9` · **Size:** medium
**Created:** 2026-11-04 16:39:10 EST · **Closed:** 2026-11-04 18:05:17 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

brief-polish: in the same brief.rs, report totals and +N more behind the Finished/Dropped caps (bob-cli-gv). Make Bryan's words deduplicated, date-ordered, fair across days, and link-safe (bob-cli-gw). Drop empty Part date segments and raw block ids in Still open aliases (bob-cli-gx).

## Notes

[2026-11-04T23:01:05Z · bob-cli-h8.9] PROPOSED FOLLOW-UP: just check clippy gate fails on clean base tree with 8 pre-existing denies in src/native/capture_language/editor_pomodoro.rs (needless_return x3, collapsible_if x3, question_mark) and src/native/capture_language/past.rs (overly_complex_bool_expr) — needs an owner lane, not brief-polish. -r Recording pre-existing clippy gate failure per phase instructions

[2026-11-04T23:05:17Z · bob-cli-h8.9] Verified: 3 new regression tests in tests/cli/periods.rs failed pre-fix exactly as gv/gw/gx describe and pass post-fix; full periods module 27/27 green; cargo test --workspace --no-fail-fast green (8527 passed, 0 failed, 27 targets); cargo fmt clean; just docs-check green (447 passed). Finished/Dropped carry finished_total/finished_more and dropped_total/dropped_more with - +N more tails (additive, arrays unchanged). Bryan words deduped by (date,text) preferring daily-note links, date-only stable order, 10/day + 40 overall round-robin, exact checkbox trim, link-only children skipped, wikilink aliases flattened. Part lines skip empty dates; Still open aliases strip inline fields and ^block ids. docs/periods.md contract updated. just check clippy gate has 8 pre-existing denies in capture_language (reproduced identically on clean base, recorded as PROPOSED FOLLOW-UP, not this phase).

## Dependencies

- **Blocks:** [bob-cli-h8.10](bob-cli-h8.10.md) ◐ · ⧖ 2026-11-04
- **Depends on:** [bob-cli-h8.3](bob-cli-h8.3.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.9.md) | [bob-cli-h8.9](bob-cli-h8.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`75bb6c6`](https://github.com/bobs-org/bob-cli/commit/75bb6c62e82526445576872e5542de2ad53bd914) | feat(periods): report brief truncation totals and clean words and aliases | [bob-cli-h8.9](bob-cli-h8.9.md) | 2026-11-04 18:39:00 EST |
