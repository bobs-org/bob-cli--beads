# Bead: bob-cli-ly.2 — bob-cli \`//\` grammar claim, note\_goto completion, Tasks continuation, docs

[Bead Pages](../README.md) / [bob-cli-ly](README.md) / bob-cli-ly.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cr](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cr.md) · **Assignee:** `bob-cli-ly.2` · **Size:** medium
**Created:** 2026-11-15 16:47:01 EST · **Closed:** 2026-11-15 21:04:22 EST
**Plan:** [202611/note\_goto\_double\_slash.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_goto_double_slash.md)

## Description

cli-note-goto: claim whole-draft `//query` as `note_goto` across parse, refusal, and completion; serve catalog rows; advertise `/` as the bare Go To continuation key; bump the grammar; update help, docs, and CLI tests.

## Notes

[2026-11-16T02:04:12Z · bob-cli-ly.2] PROPOSED FOLLOW-UP: just docs-check still fails the mounted bob-ledger-tools page at 6146/6000 — already tracked by bob-cli-il; this phase did not edit that sibling page and capture-syntax is 5997/6000.

[2026-11-16T02:04:22Z · bob-cli-ly.2] Verified contract §§1–4: grammar 28 claims whole-draft //query as note_goto; just all passed after bumping grammar-27 goldens. capture-syntax trimmed to 5997/6000. just docs-check fails only the pre-existing mounted bob-ledger-tools page at 6146/6000 (bob-cli-il). Live vault with CARGO_TARGET_DIR/release/bob (not installed): capture-complete -c 2 -f json -- '//' → grammar 28, schema_version 1, context note_goto, listed=3645, 3645 rows, 761081 bytes, warm 0.101s, first row today's daily 2026/20261115.md group today, picker trigger_removal_range {start:1,end:2}; capture --dry-run -- '//x' exits 2 with T4. epic-symbols none.

## Dependencies

- **Depends on:** [bob-cli-ly.1](bob-cli-ly.1.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ly.4](bob-cli-ly.4.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ly.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ly.2/README.md) | [bob-cli-ly.2](bob-cli-ly.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fc3d6eb`](https://github.com/bobs-org/bob-cli/commit/fc3d6eb47c9d85e7f5622196faf688016fa800f3) | feat(capture)!: claim whole-draft //query as Go To Notes | [bob-cli-ly.2](bob-cli-ly.2.md) | 2026-11-15 21:06:37 EST |
