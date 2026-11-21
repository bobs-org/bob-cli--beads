# Bead: bob-cli-on.7 — Carry a requirement branch into its own task

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.7` · **Size:** medium
**Created:** 2026-11-21 11:13:26 EST · **Closed:** 2026-11-21 14:24:07 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

req-split: extend Task Split to select requirements at any depth, move the whole branch with depth rebasing and the NOTES rule, leave a [>] stub, refuse overlaps and excluded rows, and expose a library entry with a move map.

## Notes

[2026-11-21T19:22:50Z · bob-cli-on.7] PROPOSED FOLLOW-UP: just docs-check fails identically on the clean base (reference/ word budgets: bob-navigation-hotkeys.md 6302, vault-format.md 6037) — already tracked by bob-cli-oc and bob-cli-ob; no new bead needed.

[2026-11-21T19:22:54Z · bob-cli-on.7] PROPOSED FOLLOW-UP: plain (non-req) Task Split still writes the LINKED FROM mention after the children at a fixed two-space indent (SP2, SP17, SP18), outside the task_block_layout managed-link zone that req carries now use — align plain splits with insertion_offset(ManagedLink) and the note indent unit; changes SP1–SP31 bytes and the bob-plugins JS twin, so bob-cli first then copy.

[2026-11-21T19:22:59Z · bob-cli-on.7] PROPOSED FOLLOW-UP: bob-plugins split twin must port req-split (for obsidian-close-card / bob-cli-on.11): copy tests/fixtures/task_split/vectors.json (SP32–SP51), the innermost-candidate rule for cursor/lines, parent-scoped count, [>] stubs, carried-block layout through the RL twin (back-link in managed zone + first-req NOTES scoop), the moves map, split_req_excluded/split_overlap, and the SP51 fix (Rust inserted below the wrong line when a split owner with moved child rows was followed by more content; the JS twin may share it).

[2026-11-21T19:23:55Z · bob-cli-on.7] PROPOSED FOLLOW-UP: just docs-check now also flags docs/reference/plugins/bob-ledger-tools.md at 6042 words (cap 6000) — a mounted bob-plugins page this phase never touched, likely grown by the concurrent ledger-marks phase (bob-cli-on.9); trim it in bob-plugins or extend bob-cli-ob.

[2026-11-21T19:24:07Z · bob-cli-on.7] req-split shipped: Task Split now lists reqs at any depth (task_reqs forest, root-owner context, innermost-candidate rule for cursor/lines, parent-scoped count), refuses dropped/carried/[x] reqs (split_not_splittable, state copy), excluded reqs (split_req_excluded), and ancestor+descendant picks (split_overlap); carries write a [>] stub, the branch rebased below the owner's block (daily-note rules kept), the new block laid out via task_block_layout (back-link in managed zone, NOTES rule with with_first_note), anchor reuse, and a per-task move map. New task_split/carry.rs exposes carry_req(snapshot, owner, RowKey|LineDigest) -> CarryOutcome{plan, path, line, block_id, moves}. Fixed a pre-existing split bug placing new tasks too low when moved rows preceded later content (SP51). Added SP32–SP51 vectors (harness now also pins req_depth, moves, stubs), unit tests for carry_req/listing, updated docs/task-split.md §§1–3,5,6, docs/task-requirements.md §6/§10, fixture README. Verified: just check passes (fmt, clippy gate, full workspace tests); just docs-gen clean; just docs-check fails only on pre-existing reference budgets (tracked bob-cli-oc/bob-cli-ob) plus a mounted bob-plugins page this phase did not touch; CLI smoke test of listing, dry run, JSON, and refusals on a temp vault.

## Dependencies

- **Depends on:** [bob-cli-on.3](bob-cli-on.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.8](bob-cli-on.8.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.7/README.md) | [bob-cli-on.7](bob-cli-on.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2239120`](https://github.com/bobs-org/bob-cli/commit/2239120810ed5867eefc66a468cee04972aa6b45) | feat(task-split)!: carry a requirement branch into its own task | [bob-cli-on.7](bob-cli-on.7.md) | 2026-11-21 14:25:11 EST |
