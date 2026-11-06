# Bead: bob-cli-hl.3.1.2 — Carry merge payload origins into final task previews

[Bead Pages](../README.md) / [bob-cli-hl.3.1](bob-cli-hl.3.1.md) / bob-cli-hl.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.md) · **Assignee:** `bob-cli-hl.3.1.2` · **Size:** medium
**Created:** 2026-11-05 19:49:42 EST · **Closed:** 2026-11-05 21:13:40 EST
**Plan:** [202611/capture\_merge\_in\_execution.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_execution.md)

## Description

origins: carry internal source identity and insertion ranges from the merge engine through capture tracking to task_blocks lines, including > and label merges, without text matching or new serialized engine fields.

## Notes

[2026-11-06T02:13:08Z · bob-cli-hl.3.1.2] PROPOSED FOLLOW-UP: just check fails on clean base 8eecf0c4 and on this branch identically: error constant TODAY is never used at tests/cli/capture/merge_in.rs:8 (dead_code denied); already recorded by bob-cli-hl.3.1.1 note #1, no new tracking bead

[2026-11-06T02:13:12Z · bob-cli-hl.3.1.2] PROPOSED FOLLOW-UP: just docs-check fails identically on clean base HEAD 4282e712 (pre-existing generated drift, not from this phase): docs/reference/cli/capture-parse.md says grammar 14 while src/native/capture_language/mod.rs GRAMMAR_REVISION=15, plus glossary/capture-complete drift from the grammar phase; this phase touches no docs per plan, so leaving for the acceptance phase docs pass

[2026-11-06T02:13:40Z · bob-cli-hl.3.1.2] Origins implemented end-to-end: engine captures per-payload insertion ranges (repaired fragments) and forwards them through retirement/mirror/dependency/offer edits via Myers Replace-pairing into MergePlan.merge_line_origins (serde-skipped); adapters carry them through explicit > and label merges (section targets excluded) with cross-group forwarding; TaskBlockTracker stores per-line origins, forwards through same-note edits, and emits BlockLineJson.origin (<relative>#^<block>) only on merged rows. Verified: 4 new transfer origins tests (basic/typed-order, duplicates+identical-text, same-note+later-edit, rename+drawer+section-omission) + 1 new label-merge origins test pass; all 30 transfer, 4 relations_merge, 51 task_merge lib, 185 capture lib, 3 merge_in CLI tests green. just check fails only on pre-existing TODAY dead_code (recorded follow-up, reproduces on clean base); just docs-check fails only on pre-existing grammar-14-vs-15 generated drift (recorded follow-up, untouched per plan). epic-symbols clean. Changes uncommitted in workspace for land-agent review.

## Dependencies

- **Depends on:** [bob-cli-hl.3.1.1](bob-cli-hl.3.1.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hl.3.1.3](bob-cli-hl.3.1.3.md) ◐ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hl.3.1.4](bob-cli-hl.3.1.4.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.2/README.md) | [bob-cli-hl.3.1.2](bob-cli-hl.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fd26fb2`](https://github.com/bobs-org/bob-cli/commit/fd26fb29655d1efba1639db2c5883d98302e3d59) | feat(capture): carry merge payload origins into task block previews | [bob-cli-hl.3.1.2](bob-cli-hl.3.1.2.md) | 2026-11-05 21:14:58 EST |
