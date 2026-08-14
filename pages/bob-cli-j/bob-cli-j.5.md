# Bead: bob-cli-j.5 — Highlighting, completion, and live preview

[Bead Pages](../README.md) / [bob-cli-j](README.md) / bob-cli-j.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.005](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.005.md) · **Assignee:** `bob-cli-j.5` · **Size:** medium
**Created:** 2026-08-13 20:32:35 EDT · **Closed:** 2026-08-13 21:58:46 EDT
**Plan:** [202608/bob\_mac\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/bob_mac_capture.md)

## Description

intelligence: connect macOS 26 attributed editing to capture-parse spans, add an inline keyboard completion popover backed by capture-complete, and add debounced cancellable exact preview through bob capture --dry-run --no-clip with cached targets and explicit stale-response handling.

## Notes

[2026-08-14T01:58:46Z · bob-cli-j.5] Implemented macOS capture intelligence in bobs-org/bob-mac-capture: parse-span highlighting, cursor completion, cached route hints, no-clip live preview with fixed priority seed, FSEvents target refresh, updated JSON models, fixture tests, and README contract. Verified git diff --check, bash -n for fixture/scripts, and fake-bob capture-targets/capture-complete/capture --dry-run --no-clip smoke outputs. Swift build/test could not be run on this Linux host because swift is not installed; macOS CI remains the required compiler validation.

[2026-08-14T01:59:46Z · bob-cli-j.5] Verified git diff --check, fixture shell syntax, and fake-bob smoke checks for capture-targets, capture-complete, and no-clip preview; swift build/test not available on this Linux host.

## Dependencies

- **Depends on:** [bob-cli-j.2](bob-cli-j.2.md) ✓ · ⧖ 2026-08-13
- **Depends on:** [bob-cli-j.3](bob-cli-j.3.md) ✓ · ⧖ 2026-08-13
- **Blocks:** [bob-cli-j.6](bob-cli-j.6.md) ✓ · ⧖ 2026-08-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j.5/README.md) | [bob-cli-j.5](bob-cli-j.5.md) | 0 |
