# Bead: bob-cli-rc.2 — Section Map card painter, placement, and styles

[Bead Pages](../README.md) / [bob-cli-rc](README.md) / bob-cli-rc.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hg](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hg.md) · **Assignee:** `bob-cli-rc.2` · **Size:** medium
**Created:** 2026-11-27 15:06:05 EST · **Closed:** 2026-11-27 16:19:17 EST
**Plan:** [202611/ctrl\_jk\_section\_map.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ctrl_jk_section_map.md)

## Description

card: build the pure DOM painter with keyed in-place reconciliation, the margin/overlay/compact placement function, the .bob-section-map styles, and a headless-Chromium preview whose screenshots are reviewed against the visual spec.

## Notes

[2026-11-27T21:19:08Z · bob-cli-rc.2] PROPOSED FOLLOW-UP: test-snooze-model-vectors "snooze-add-resnooze-replaces-history daily postimage" fails (extra woke 15:32 row); reproduces identically on the clean base tree, unrelated to the Section Map card — needs its own bug bead

[2026-11-27T21:19:17Z · bob-cli-rc.2] Card phase done: 474-section-map-view.js painter (keyed reconcile, pill slide/crossfade, entrance-once, compact strip, textContent-only, aria-hidden rows + role=status live region), computeSectionMapPlacement (margin/overlay/compact + Notice nudge), .bob-section-map styles, 8 fake-DOM tests green, preview-section-map.cjs 18 PNGs all layout checks pass, gate green except pre-existing snooze-model-vectors fail (reproduces on clean base, recorded as follow-up), version 2.107.15, vault byte-identical

## Dependencies

- **Depends on:** [bob-cli-rc.1](bob-cli-rc.1.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-rc.3](bob-cli-rc.3.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rc.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rc.2/README.md) | [bob-cli-rc.2](bob-cli-rc.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c3729cf`](https://github.com/bobs-org/bob-plugins/commit/c3729cf1c922035293769732fea81c2e970936f7) | feat(navigation): add Section Map card painter, placement, and styles | [bob-cli-rc.2](bob-cli-rc.2.md) | 2026-11-27 16:20:19 EST |
