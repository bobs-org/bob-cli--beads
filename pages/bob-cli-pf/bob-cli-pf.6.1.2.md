# Bead: bob-cli-pf.6.1.2 — Add cached capability gating and native property entry routing

[Bead Pages](../README.md) / [bob-cli-pf.6.1](bob-cli-pf.6.1.md) / bob-cli-pf.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.6.md) · **Assignee:** `bob-cli-pf.6.1.2` · **Size:** medium
**Created:** 2026-11-23 20:38:15 EST · **Closed:** 2026-11-23 22:38:04 EST
**Plan:** [202611/frontmatter\_takeover.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/frontmatter_takeover.md)

## Description

capability-routing: add the session-and-bob-path capability cache, shared actual-ownership query, reversible Add file property command wrapper, and owned-scope focus-helper routing. Test lifecycle and stale-result behavior before enabling adapters.

## Notes

[2026-11-24T03:37:18Z · bob-cli-pf.6.1.2] capability-routing landed in bob-plugins: 298v session-and-bob-path cache (confirmed/absent/unconfirmed per resolved bob path, in-flight dedupe, bounded retry of 3, stale/path-changed/teardown discards, no repaint retry), 240q actual-ownership query (live field generation for Live Preview, scope tag for Reading, denied scopes unowned) plus per-scope release, S1 command wrapper on markdown:add-metadata-property (owned scopes openPropertyEditor filePath+mode:add, untouched scopes delegate with receiver/args/check intact, opener failure releases then native fallback, teardown restores only own wrapper), focus-helper routing (owned views openPropertyEditor key:summary, sidebar keeps native even when main note owned). Verified: 20 new unit tests green; neighbors (property-update, entrypoints, frontmatter-ownership, notebook-catalog) 92 green; build:check green; full unit 9202 with only the 2 known perf-budget flakes (pass isolated, same as clean tree). Adapters unwired (no production propertyCardOwnFrontmatter callers). Root-cause found and fixed in-phase: the probe initially walked the vault via getMarkdownFiles during onload, breaking vault-walk-counting tests; eligible-note resolution is now walk-free (open note or pend). bob plugins sync deployed from workspace build. -r capability-routing phase completion evidence

[2026-11-24T03:37:52Z · bob-cli-pf.6.1.2] PROPOSED FOLLOW-UP: 25ms perf budgets in test-ledger-tools-event-link-times.cjs (one build over a 200-link ledger, took 50-120ms) and test-ledger-tools-frees-marks.cjs (200-link/2000-task build, took ~480ms) fail under full-suite parallel load on apollo but pass in isolation (40/40); identical failures on the clean base tree (9202-test run: only these 2 fail); same known pattern already recorded on pf.6.1.1 and earlier beads. -r pre-existing perf flake triage

[2026-11-24T03:38:04Z · bob-cli-pf.6.1.2] capability-routing done and verified: session-and-bob-path capability cache, 240q actual-ownership query plus per-scope release, S1 Add-file-property wrapper (markdown:add-metadata-property), owned-scope focus routing with sidebar-native preservation. 20 new tests green; 92 neighbor tests green; build:check green; full unit 9202/9195 with only the 2 known pre-existing perf flakes (isolated-green, clean-tree-identical); walk-free probe (fixed onload vault-walk regression in-phase); adapters stay unwired; bob plugins sync deployed.

## Dependencies

- **Depends on:** [bob-cli-pf.6.1.1](bob-cli-pf.6.1.1.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pf.6.1.3](bob-cli-pf.6.1.3.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.2/README.md) | [bob-cli-pf.6.1.2](bob-cli-pf.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ede33f2`](https://github.com/bobs-org/bob-plugins/commit/ede33f2fc10c858615b1ab76eaaebf46e6ba4cd6) | feat(property-card): add cached capability routing and native entry points | [bob-cli-pf.6.1.2](bob-cli-pf.6.1.2.md) | 2026-11-23 22:39:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.6.1.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.2/README.md

<!-- sase:referenced-by:end -->
