# Bead: bob-cli-g9.6 — Real-Obsidian decay ladder end-to-end check

[Bead Pages](../README.md) / [bob-cli-g9](README.md) / bob-cli-g9.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.32.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.32.linker.w0.md) · **Assignee:** `bob-cli-g9.6` · **Size:** medium
**Created:** 2026-11-02 15:55:43 EST · **Closed:** 2026-11-02 21:33:41 EST
**Plan:** [202611/task\_decay\_ladder.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_decay_ladder.md)

## Description

live-e2e: add an isolated real-Obsidian e2e that walks a scratch vault through every rung (keeps, card, step, stay, drop, undo, batch skip), asserts the exact task lines and Rotten Log entries, captures the card in light and dark themes, and records the result in a live-verification doc.

## Notes

[2026-11-03T02:33:24Z · bob-cli-g9.6] PROPOSED FOLLOW-UP: Live Obsidian decay-ladder e2e pass — this host has no /snap/bin/obsidian and no xvfb-run (driver exit 2 unrun). Rerun `xvfb-run -a node scripts/obsidian-decay-ladder-e2e.cjs` on a Linux host with Obsidian, capture WIP/Ready/P4 light+dark screenshots into docs/decay-ladder.md, and smoke Alt+F / card Enter-Stay-Drop / Ctrl+Z on the Mac.

[2026-11-03T02:33:41Z · bob-cli-g9.6] Verified offline --self-test (fixture 2-keeps/enter P1/rolls 2, Rotten Log keep/stay/step/drop bodies, card probe, skip notice, P1/P4 windows, Alt+F/undo/batch-skip driver coverage) via node scripts/obsidian-decay-ladder-e2e.cjs --self-test and scripts/test-obsidian-decay-ladder-e2e.cjs. Live driver exits 2 unrun (no Obsidian/xvfb on this host). docs/decay-ladder.md registered; contract tests 8/8; epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-g9.5](bob-cli-g9.5.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-g9.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-g9.6/README.md) | [bob-cli-g9.6](bob-cli-g9.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0346d82`](https://github.com/bobs-org/bob-cli/commit/0346d828011a5f5a0c4ef4d526fa80583dab7ee6) | docs(decay-ladder): add live-verification page for the task-decay e2e | [bob-cli-g9.6](bob-cli-g9.6.md) | 2026-11-02 21:36:14 EST |
