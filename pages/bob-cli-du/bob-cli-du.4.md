# Bead: bob-cli-du.4 — bob relations rename --reverse moves each edge to its other end

[Bead Pages](../README.md) / [bob-cli-du](README.md) / bob-cli-du.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.aw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.aw.md) · **Assignee:** `bob-cli-du.4` · **Size:** large
**Created:** 2026-10-28 14:49:53 EDT · **Closed:** 2026-10-28 21:26:47 EDT
**Plan:** [202610/relation\_complete\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_complete_labels.md)

## Description

reverse-rename: add -r/--reverse to bob relations rename so S OLD T becomes T NEW S in one previewed transaction and one revertable commit, with mirrors, minting, merge, refusals, JSON, and beautiful human preview.

## Notes

[2026-10-29T01:26:47Z · bob-cli-du.4] Implemented reverse rename per 202610/relations_reverse_rename.md: new relation_labels/reverse.rs planner (immutable snapshot, archive-aware resolution, writable minting, simultaneous collision checks, LINKS via plan_links_edit, mirrors via plan_linked_from_line, reversal-aware verify), -r/--reverse flag after -o with help/completion flow, vault_rewrite journal rollback guard, commit subject '... (reversed)', additive JSON (reversed/moves/minted_block_ids) + human grouping/mint/merge/mirror/stay-open/undo. Docs: marked RV10 shipped, removed planned markers, clarified task-status-hooks archive exception, documented JSON fields, ran just docs-gen (relations.md diff only reverse). Tests: new tests/cli/relations_reverse.rs (12 tests: dry-run/apply/revert/unknown_label, 14-edge migration counts, same-note/cross-note, mint/refusal, merge/conflict/same-key, unresolved/self, closing-label never closes, CRLF/no-newline, help ordering/completion, mirrors-disabled, previous-daily, reconcile no-op) + existing rename/relations suites green. Gates: cargo test --lib relation_labels (11 ok), cargo test --lib vault_rewrite (8 ok), cargo test --test cli relations (136 ok), just check exit 0, just docs-check exit 0.

## Dependencies

- **Depends on:** [bob-cli-du.3](bob-cli-du.3.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-du.9](bob-cli-du.9.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.4.md) | [bob-cli-du.4](bob-cli-du.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cba7c47`](https://github.com/bobs-org/bob-cli/commit/cba7c47dada6b0f409fc2b9c6ad72ecf05e97bb2) | feat(relations): reverse relation-label renames with previewed edge reversal | [bob-cli-du.4](bob-cli-du.4.md) | 2026-10-28 21:28:05 EDT |
