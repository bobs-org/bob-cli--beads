# Bead: bob-cli-mf.5 — Album arrangement editing and one-envelope save

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.5` · **Size:** medium
**Created:** 2026-11-16 15:38:38 EST · **Closed:** 2026-11-16 18:16:15 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

## Description

album-arrange: wire the engine into the album card. Alt+J/K, ends, counts, and m move-to change a local projection with FLIP, deltas, and a pending bar. A latched quiet/loud Enter saves one envelope in the background, and u steps back or stages Undo. The save survives closing the card.

## Notes

[2026-11-16T23:15:58Z · bob-cli-mf.5] PROPOSED FOLLOW-UP: Full test:unit shows 16 pre-existing failures on clean base (setup-card x2, perf budgets, walkMode x4, chip/toggle/priority/related, block-marks date fixture); identical count on modified tree after album-header fixes, so unrelated to album-arrange

[2026-11-16T23:16:15Z · bob-cli-mf.5] Album-arrange wired: local projection with Alt+J/K/ends/counts/m gaps, FLIP/deltas/pending bar, quiet_once Enter latch, background save with follow-on marker, refusal-kept pending, esc/u ladders, close-during-save Notice + per-stem undo seed. Verified: 5 new arrange-card tests pass, 34 album-header pass, 80-file focused set green; build:check and docs:check pass; bob plugins sync deployed 3 files from workspace checkout

## Dependencies

- **Depends on:** [bob-cli-mf.4](bob-cli-mf.4.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mf.6](bob-cli-mf.6.md) ◐ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.5/README.md) | [bob-cli-mf.5](bob-cli-mf.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@866bb77`](https://github.com/bobs-org/bob-plugins/commit/866bb77c859d19046784324c58fd4e97ec86b00d) | feat(bob-ledger-tools): wire album arrangement editing and one-envelope save | [bob-cli-mf.5](bob-cli-mf.5.md) | 2026-11-16 18:18:09 EST |
