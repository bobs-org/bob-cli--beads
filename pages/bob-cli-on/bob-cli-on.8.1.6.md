# Bead: bob-cli-on.8.1.6 — Published contract and cross-feature regression evidence

[Bead Pages](../README.md) / [bob-cli-on.8.1](bob-cli-on.8.1.md) / bob-cli-on.8.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.md) · **Assignee:** `bob-cli-on.8.1.6` · **Size:** medium
**Created:** 2026-11-22 07:22:30 EST · **Closed:** 2026-11-22 13:57:46 EST
**Plan:** [202611/requirement\_close\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/requirement_close_engine.md)

## Description

contract: finish task-dependencies sections 12.25 and 12.26 and the JSON reference, complete RV and compatibility coverage, run the canonical code and docs gates, and prepare completion evidence for bob-cli-on.8's land agent.

## Notes

[2026-11-22T18:57:46Z · bob-cli-on.8.1.6] Contract phase done: added 12.25 normative requirement-close contract (eligibility, snapshot-bound key formula, owner order/numbering, full wire-shape field table, req_outcomes omissions, verdicts/conflicts/refusals, frozen receipt table, one-commit/placement/jump rules, mixed-card JSON example) and 12.26 RV inventory (RV1-43 by family); updated 12.13 with picker v6, 12.14 with -k/--carry + hidden --req-choice + row-kind flag table + stale/overlap refusals, 12.5 reporting model with 12.25 pointer + requirements glyph/group entries; finished json-outputs (discriminator, omissions, links to 12.25/12.26) and linked task-requirements 7 + roster to 12.25/12.26. Verified: just check exit 0 (12709 passed, 0 failed, 43 binaries ok), cargo fmt clean, just docs-gen no diff, just docs-check 447 passed (new anchors validated), focused task_complete lib 262 passed + capture req_close CLI 21 passed. No code changes; RV/RQ/RL/RW/SP fixtures untouched. epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-on.8.1.5](bob-cli-on.8.1.5.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.8.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.6/README.md) | [bob-cli-on.8.1.6](bob-cli-on.8.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`96a23f5`](https://github.com/bobs-org/bob-cli/commit/96a23f506f072ec577b6891b605937c47d4d82a6) | docs(task-dependencies): publish requirement close contract and RV inventory | [bob-cli-on.8.1.6](bob-cli-on.8.1.6.md) | 2026-11-22 13:58:46 EST |
