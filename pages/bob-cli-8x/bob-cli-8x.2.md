# Bead: bob-cli-8x.2 — Reverse dependency writer with forward-parity tests

[Bead Pages](../README.md) / [bob-cli-8x](README.md) / bob-cli-8x.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.117](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.117.md) · **Assignee:** `bob-cli-8x.2` · **Size:** medium
**Created:** 2026-10-17 17:11:59 EDT · **Closed:** 2026-10-17 18:18:07 EDT
**Plan:** [202610/ctrl\_shift\_alt\_b\_blocks\_stage.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_alt_b_blocks_stage.md)

## Description

writer: add a nav writer that puts sources N onto many dependents T across notes, built on planDependencyEdit and the §6.6 prepare → commit → mirror order. Prepare N once (id plus the strongest lane), plan its BLOCKS edit once from the T writes that committed, and aggregate Pomodoro consumption. Prove byte parity with the forward writer on the RBP/RBW vectors.

## Notes

[2026-10-17T22:17:52Z · bob-cli-8x.2] PROPOSED FOLLOW-UP: npm test still fails 6 cases on the clean base tree — ledger-tools unblocked-glyph Live Preview/Reading (bob-cli-6v), decision-card Keep counts (bob-cli-6w), and forward-promotion reverse BLOCKS pointer (bob-cli-7i).

[2026-10-17T22:18:07Z · bob-cli-8x.2] planBlocksEdit/applyBlocksEdit in nav 084+592; mergeTargetPreparations fixes RBW6 in the counted path; optional blocksLinesEnabled on applyDependencyEdit. npm run validate green. scripts/test-navigation-blocks-edit.cjs covers RBP1–RBP10, RBW1–RBW4, RBW6 with forward byte parity. npm test: 2938 pass, 6 fail identically on clean base (bob-cli-6v, bob-cli-6w, bob-cli-7i). bob plugins sync --repo linked checkout. epic-symbols: none leftover.

## Dependencies

- **Depends on:** [bob-cli-8x.1](bob-cli-8x.1.md) ✓ · ⧖ 2026-10-17
- **Blocks:** [bob-cli-8x.3](bob-cli-8x.3.md) ◐ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8x.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.2/README.md) | [bob-cli-8x.2](bob-cli-8x.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8ca6a65`](https://github.com/bobs-org/bob-plugins/commit/8ca6a65eeca6b6f34403ae2e9840896e42a8cf1a) | feat(nav): add reverse Blocks writer with forward-parity tests | [bob-cli-8x.2](bob-cli-8x.2.md) | 2026-10-17 18:22:11 EDT |
