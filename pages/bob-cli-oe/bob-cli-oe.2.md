# Bead: bob-cli-oe.2 — Obsidian successor card pin (picker API v5)

[Bead Pages](../README.md) / [bob-cli-oe](README.md) / bob-cli-oe.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5m.linker.w0.md) · **Assignee:** `bob-cli-oe.2` · **Size:** medium
**Created:** 2026-11-20 17:03:14 EST · **Closed:** 2026-11-20 17:35:01 EST
**Plan:** [202611/successor\_jump\_pin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_pin.md)

## Description

nav-pin-card: in bob-navigation-hotkeys, extract code from fragment 206 to make room, then add the Ctrl+J pin: radio toggle by key, a solid accent `↗ Jump` capsule, hover button, footer chip, summary, and status copy. Enter's highlight fallback is suppressed while a pin is staged, and a jump-only commit returns `{picks, closes, jump}`. Picker API goes to v5.

## Notes

[2026-11-20T22:34:42Z · bob-cli-oe.2] PROPOSED FOLLOW-UP: docs-check budget docs/reference/vault-format.md over cap at 6016 words (cap 6000) fails on the clean base tree too — pre-existing, needs a maintainer trim or cap bump

[2026-11-20T22:34:49Z · bob-cli-oe.2] PROPOSED FOLLOW-UP: reference budget docs/reference/plugins/bob-navigation-hotkeys.md has ~3 words of headroom under its 6000-word cap after this phase, so the next nav-docs edit needs a cap bump or trims elsewhere

[2026-11-20T22:35:01Z · bob-cli-oe.2] nav-pin-card done in bob-plugins: extracted 206 mixin+API to 206f (206 now 815 lines), added 206e Ctrl+J jump pin with capsule/hover-button/footer-chip/summary/status copy, picker API v5 with jump-only commits; 75/75 successor tests pass, build:check/inventory/perf green, docs:check clean except pre-existing vault-format budget, manifest 2.93.0, bob plugins sync deployed

## Dependencies

- **Blocks:** [bob-cli-oe.3](bob-cli-oe.3.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.2/README.md) | [bob-cli-oe.2](bob-cli-oe.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oe.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.2/README.md

<!-- sase:referenced-by:end -->
