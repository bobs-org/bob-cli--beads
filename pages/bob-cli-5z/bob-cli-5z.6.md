# Bead: bob-cli-5z.6 — Bob Mac Capture \`==#\` picker status and row hints

[Bead Pages](../README.md) / [bob-cli-5z](README.md) / bob-cli-5z.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.61.w1.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.61.w1.w0.md) · **Assignee:** `bob-cli-5z.6` · **Size:** small
**Created:** 2026-10-09 13:24:49 EDT · **Closed:** 2026-10-09 15:09:55 EDT
**Plan:** [202610/pomodoro\_override.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_override.md)

## Description

mac-override-picker: decode the capture-complete `override` object and use it for the `==#` picker status line and the running/open row hints, fix the `=#` running-row hint to teach `==`, with fixtures and tests.

## Notes

[2026-10-09T19:09:55Z · bob-cli-5z.6] mac-override-picker done in bob-mac-capture checkout (uncommitted working tree for land-agent stitch): decoded capture-complete override object (keepsLedger + running) in CaptureModels; ==# rows show Takes-over ledger + swap/restart hints, plain =# running hint now teaches ==; override-aware picker status wired through applyNonActiveTaskCompletion; 4 real-bob fixtures (==#, ==3#, idle, ==3# parse) + fake-bob routes; 5 row tests + 4 decode tests + 5 status tests + 3 live panel-model probes added; README updated. Verified: bash -n + live fake-bob probes for all routes, independent Python simulation reproducing every new string exactly from real-bob JSON, full re-reads of touched files, zero new brace/paren imbalance (remaining deltas pre-exist on base), epic-symbols clean. Swift build/test pending macOS CI (no toolchain on host).

## Dependencies

- **Depends on:** [bob-cli-5z.4](bob-cli-5z.4.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5z.5](bob-cli-5z.5.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5z.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5z.6/README.md) | [bob-cli-5z.6](bob-cli-5z.6.md) | 0 |
