# Bead: bob-cli-5k.3 — Add the canonical just check gate

[Bead Pages](../README.md) / [bob-cli-5k](README.md) / bob-cli-5k.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0y2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y2.md) · **Assignee:** `bob-cli-5k.3` · **Size:** small
**Created:** 2026-10-07 14:38:41 EDT · **Closed:** 2026-10-07 15:51:40 EDT
**Plan:** [202610/close\_top\_ten\_impact\_beads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/close_top_ten_impact_beads.md)

## Description

check-gate: add `just check` (fmt, clippy, and every test binary with --no-fail-fast), make `just test` stop masking binaries, clear any remaining clippy deny or environment-dependent CLI test, document the gate, prove it green twice, and close bob-cli-3c.

## Notes

[2026-10-07T19:51:40Z · bob-cli-5k.3] check-gate done on 3cbef27: just check (fmt+clippy+test --no-fail-fast) green twice, 3190 tests each run (1876 lib, 1159 cli); just test unmasked; masking demo proved CLI binary runs under broken lib; dependsOn tautology now asserts the real reconcile warning; DISPLAY/WAYLAND_DISPLAY/TMUX scrubbed + stub clipboard (DISPLAY=:99 run passes); README documents gate; bob-cli-3c closed; no epic-symbol leftovers

## Dependencies

- **Depends on:** [bob-cli-5k.1](bob-cli-5k.1.md) ✓ · ⧖ 2026-10-07
- **Depends on:** [bob-cli-5k.2](bob-cli-5k.2.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-5k.5](bob-cli-5k.5.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-5k.6](bob-cli-5k.6.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-5k.7](bob-cli-5k.7.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.3/README.md) | [bob-cli-5k.3](bob-cli-5k.3.md) | 0 |
