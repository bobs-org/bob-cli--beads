# Bead: bob-cli-2h.4 — Mac app: Block ID Picker flow, type-through, quiet states, and routing

[Bead Pages](../README.md) / [bob-cli-2h](README.md) / bob-cli-2h.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.31](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.31.md) · **Assignee:** `bob-cli-2h.4` · **Size:** medium
**Created:** 2026-09-29 09:43:07 EDT · **Closed:** 2026-09-29 10:51:33 EDT
**Plan:** [202609/mac\_block\_id\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/mac_block_id_picker.md)

## Description

block-id-flow: route `pomodoro_block_id`/`task_block_id` completions into the generic picker with intent-aware opening rules, accept, type-through commits, trigger removal, chip, quiet incomplete states, fake-bob fixtures, model and router tests, and README behavior docs.

## Notes

[2026-09-29T14:51:33Z · bob-cli-2h.4] block-id-flow done in bob-mac-capture: CapturePickerSource.blockID + BlockIDPickerContext, CapturePickerIndex.blockID, handleBlockIDCompletion with link/new opening rules + refetch, generic accept with @route:id announcements and spoken no-op reasons, New-ID type-through commits, marker-aware trigger removal, quiet pomodoro_id/block_id needs with precedence, task_block_id/block_id request gating. fake-bob parse/complete/dry-run fixtures for @file:/@file:rea/@file:ready/@old:/Follow-up new+colon/child-line/batch/type-through + cursor-aware Do-work/Follow-up branches; 19 new model tests + 1 router test; README behavior + keyboard table + Requirements. Verified: fake-bob bash -n clean, all new fixture branches emit valid JSON with expected contexts/ranges/needs, old-draft outputs byte-identical to base, no epic-symbols left. NOT run: swift build/test (no Xcode toolchain on this Linux host) — needs macOS just test before landing.

## Dependencies

- **Depends on:** [bob-cli-2h.3](bob-cli-2h.3.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2h.5](bob-cli-2h.5.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2h.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2h.4/README.md) | [bob-cli-2h.4](bob-cli-2h.4.md) | 0 |
