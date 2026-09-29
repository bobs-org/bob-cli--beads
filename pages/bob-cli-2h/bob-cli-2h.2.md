# Bead: bob-cli-2h.2 — Mac: generalize the Active Task Picker into a source-agnostic capture picker

[Bead Pages](../README.md) / [bob-cli-2h](README.md) / bob-cli-2h.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.31](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.31.md) · **Assignee:** `bob-cli-2h.2` · **Size:** medium
**Created:** 2026-09-29 09:43:07 EDT · **Closed:** 2026-09-29 10:00:55 EDT
**Plan:** [202609/mac\_block\_id\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/mac_block_id_picker.md)

## Description

picker-generalize: refactor the `^` picker's presentation types, model state machine, routing, controller focus repair, filter field, and card into source-agnostic `CapturePicker*` building blocks with zero user-visible change to `^`.

## Notes

[2026-09-29T14:00:31Z · bob-cli-2h.2] PROPOSED FOLLOW-UP: macOS verification for picker-generalize still needed — build, swift test, and BOB_MAC_CAPTURE_RENDER_DIR before/after image comparison (Linux host has no Swift/Xcode toolchain)

[2026-09-29T14:00:55Z · bob-cli-2h.2] picker-generalize done in bob-mac-capture checkout (staged, uncommitted): new CapturePickerPresentation.swift generic types (source/status/glyph/section/row/presentation/navigation), ActiveTaskPickerIndex now emits CapturePickerPresentation, TaskDisplayText rename, CapturePickerState/ChipState+source with CapturePickerIndex enum, generic model ops (presentPicker/acceptPickerRow/escapePicker/cancelPicker/removePickerTrigger/openPickerFromChip), picker router commands/context, pickerFilter focus target + repairPickerFilterFocusIfNeeded, CapturePickerFilterField with per-source strings and substitution/spelling disabled, CapturePickerCard/Chip/KeyHints/HeightPolicy/RichText renames, taskStatus palette extended per UX spec. Verified: no stale ActiveTask* refs; normalized diff shows ranking/grouping/count/budget logic byte-identical; non-ASCII census matches HEAD (extra em dash is the relocated quiet-status string); user strings/a11y/UD key/counts unchanged; caught and fixed 4 guard-let shadowing defects by diff review; added CapturePickerTaskStatus mapping tests and adapted all picker tests to new names. NOT verifiable on this Linux host: no Swift/Xcode toolchain (xcode-swift.sh fails fast), so swift build/test and the BOB_MAC_CAPTURE_RENDER_DIR before/after image comparison are recorded as a PROPOSED FOLLOW-UP for macOS verification.

## Dependencies

- **Blocks:** [bob-cli-2h.3](bob-cli-2h.3.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2h.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2h.2/README.md) | [bob-cli-2h.2](bob-cli-2h.2.md) | 0 |
