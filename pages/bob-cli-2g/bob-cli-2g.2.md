# Bead: bob-cli-2g.2 — Picker state machine, keyboard routing, focus, and a functional picker view

[Bead Pages](../README.md) / [bob-cli-2g](README.md) / bob-cli-2g.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-2f.3.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.3.w1.md) · **Assignee:** `bob-cli-2g.2` · **Size:** medium
**Created:** 2026-09-28 18:28:11 EDT · **Closed:** 2026-09-28 18:58:43 EDT
**Plan:** [202609/mac\_active\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/mac_active_task_picker.md)

## Description

picker-flow: route `active_task` completion into a modal picker state. This covers open, suppress, and reopen rules, full-snapshot fetch, accept and accept-and-submit, the two-stage Escape, trigger removal on Backspace, and the reopen chip. Add picker key routing, an AppKit-owned filter field, and live-preview suppression for an incomplete `^`. Ship a plain but fully working picker view, fake-bob fixtures, tests, and README behavior docs.

## Notes

[2026-09-28T22:58:10Z · bob-cli-2g.2] PROPOSED FOLLOW-UP: run mac verification (just format-lint build test) or confirm green macOS 26 SwiftPM CI for the stitched picker-flow commit — this Linux host has no Swift toolchain and mac was unreachable (ssh timeout), so only fixture-level verification ran here (fake-bob bash -n plus executed JSON assertions for the new cursor-aware ^dee/^zzz branches and 3-candidate ^ list)

[2026-09-28T22:58:43Z · bob-cli-2g.2] picker-flow implemented in bob-mac-capture: picker/chip state machine with trigger kinds, full-snapshot fetch with partial fallback, accept/accept-and-submit, two-stage Escape, Backspace trigger removal, quiet incomplete-^ preview suppression, key routing with picker precedence and chip reopen, AppKit filter field with focus repair, functional picker view plus chip, fake-bob cursor-aware fixtures with 3rd unqueued-Next candidate, 12 model tests plus 4 router tests, README behavior docs. Verified on Linux: fake-bob bash -n and executed JSON assertions for all new fixture branches; Swift-level checks by API review only — mac build/test/format not run here (no Swift toolchain, mac unreachable); see PROPOSED FOLLOW-UP note for the land agent.

## Dependencies

- **Depends on:** [bob-cli-2g.1](bob-cli-2g.1.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2g.3](bob-cli-2g.3.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2g.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2g.2/README.md) | [bob-cli-2g.2](bob-cli-2g.2.md) | 0 |
