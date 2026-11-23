# Bead: bob-cli-pf.4.1.7.2 — Row identity, overlays, diagnostics, and value fidelity

[Bead Pages](../README.md) / [bob-cli-pf.4.1.7](bob-cli-pf.4.1.7.md) / bob-cli-pf.4.1.7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.land.md) · **Assignee:** `bob-cli-pf.4.1.7.2` · **Size:** medium
**Created:** 2026-11-23 03:09:55 EST · **Closed:** 2026-11-23 03:51:29 EST
**Plan:** [202611/property\_editor\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_landing_repairs.md)

## Description

row-fidelity: keep requested keys across reconciliation, publish confirmed overlays to cards and drawers, show recovery diagnostics, preserve datetime/tag/null spelling, and fix add-flow completion and draft loss.

## Notes

[2026-11-23T08:51:29Z · bob-cli-pf.4.1.7.2] row-fidelity done in bob-plugins: nearest-row identity (298o helpers wired into 298f constructor/reconcile, 298m Done-reopen, keyed mode=edit open); confirmed overlays merged into foot/record-sheet frontmatter (240r, 242k), editor repaint via store subscription plus publish-triggered drawer refresh (298d/298f), null/deletion semantics kept; hook presence added to foot digests (240r, 242kc); verbatim bob recovery message/line with duplicate-line YAML targets and row/ownership diagnostics (298e/298f/298m); datetime wall-time-without-offset plus seconds precision for naive/new values with explicit-offset retention (298h); tags normalize only typed items and null text no-op (298h); exact-name-wins plus add-refuses-open-stage (298k/298l). Verified: new row-fidelity suite plus all 6 property suites pass 108/108; adjacent foot/record/intention/bank/album suites 192/192; build:check and validate (12/12) exit 0; bob plugins sync ok; full unit 9011/9018 with only the tracked bob-cli-io frees-marks perf flakes, green 17/17 in isolation.

## Dependencies

- **Depends on:** [bob-cli-pf.4.1.7.1](bob-cli-pf.4.1.7.1.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pf.4.1.7.3](bob-cli-pf.4.1.7.3.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.4.1.7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.4.1.7.2/README.md) | [bob-cli-pf.4.1.7.2](bob-cli-pf.4.1.7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3141cf6`](https://github.com/bobs-org/bob-plugins/commit/3141cf64ff40a7ac23967cdf27432b44149f3b21) | feat(property-editor): row identity, overlays, diagnostics, and value fidelity | [bob-cli-pf.4.1.7.2](bob-cli-pf.4.1.7.2.md) | 2026-11-23 03:52:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.4.1.7.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.4.1.7.2/README.md

<!-- sase:referenced-by:end -->
