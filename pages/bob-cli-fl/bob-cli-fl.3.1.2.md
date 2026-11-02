# Bead: bob-cli-fl.3.1.2 — Report clock-aware sessions and clock diagnostics

[Bead Pages](../README.md) / [bob-cli-fl.3.1](bob-cli-fl.3.1.md) / bob-cli-fl.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.3.md) · **Assignee:** `bob-cli-fl.3.1.2` · **Size:** medium
**Created:** 2026-11-02 01:23:57 EST · **Closed:** 2026-11-02 03:11:48 EST
**Plan:** [202611/stats\_clock.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock.md)

## Description

session_diagnostics: filter session drill-downs by clock, attribute real off-clock minutes, and report unstamped rows, conflicts, drift, and overlaps.

## Notes

[2026-11-02T08:11:48Z · bob-cli-fl.3.1.2] Session diagnostics land: clock-filtered sessions with real minutes and off_clock flags, window-scoped unstamped/conflict/drift/overlap diagnostics with warnings, compat untracked markers kept. Verified: cargo fmt --check, just lint, cargo test --workspace (7538 passed, 0 failed), just docs-check pass; epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-fl.3.1.1](bob-cli-fl.3.1.1.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fl.3.1.3](bob-cli-fl.3.1.3.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.3.1.2/README.md) | [bob-cli-fl.3.1.2](bob-cli-fl.3.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.3.1.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.3.1.2/README.md

<!-- sase:referenced-by:end -->
