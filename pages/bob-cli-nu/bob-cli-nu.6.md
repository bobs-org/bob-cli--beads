# Bead: bob-cli-nu.6 — ⌘↵ runs the command chip at the cursor, with an armed chip and keycap hint

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.6` · **Size:** medium
**Created:** 2026-11-20 05:59:33 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

keymap: compose a command-chip step into the existing Meta+Enter dispatcher in bob-navigation-hotkeys, add targetAt/runAtCursor and a palette command, and paint the armed chip and a muted ⌘↵ Run keycap from the live binding. The Gmail and Highlights hints yield, and every old ⌘↵ target is regression-tested.

## Notes

[2026-11-20T15:58:37Z · bob-cli-nu.4.1.land] Heads-up from the bob-cli-nu.4.1 land agent: bob-plugins docs/develop/plugin-apis.md is at 7,980/8,000 words (develop/ warning cap). Adding the keymap contract there will cross it; trim or plan a split of the command-chip sections (see the DISCOVERED ISSUE note on bob-cli-nu).

[2026-11-20T16:41:48Z · bob-cli-nu.5] Heads-up from bob-cli-nu.5 (fence): bob-run cards mount through commandChipMount with the chipAt block identity { form: "block", fence: { open, close }, line: open } plus the render sourcePath, so store.setArmed({ ...chipAtResult.chip, sourcePath, key }) arms the card (accent border + header rule) with no extra wiring; ⌘↵ on a fence should call commandChipActivate with that chip so card Run and ⌘↵ share one path (covered by test-command-chips-fence.cjs "armed card" case).

## Dependencies

- **Depends on:** [bob-cli-nu.4](bob-cli-nu.4.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.8](bob-cli-nu.8.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.6/README.md) | [bob-cli-nu.6](bob-cli-nu.6.md) | 0 |
