# Bead: bob-cli-fl.6.1.2 — Add the persistent Stats clock control and fetch routing

[Bead Pages](../README.md) / [bob-cli-fl.6.1](bob-cli-fl.6.1.md) / bob-cli-fl.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.6.md) · **Assignee:** `bob-cli-fl.6.1.2` · **Size:** medium
**Created:** 2026-11-02 05:03:38 EST · **Closed:** 2026-11-02 06:35:36 EST
**Plan:** [202611/stats\_clock\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock_ui.md)

## Description

clock-control: add defensive clock presentation helpers, report-driven accessible radios, device persistence, clock-specific fetch keys, capability fallback, and bounded idle prefetch while preserving the Day strip default cache key.

## Notes

[2026-11-02T11:33:44Z · bob-cli-fl.6.1.2] PROPOSED FOLLOW-UP: Resolve four pre-existing bob-plugins suite failures reproduced unchanged on clean base 71ae1cb: freshness-namespace reload emits no event, note-ready startup counts 1 scan instead of 2, relation-index replay misses its 1s completion deadline, and schedule-work-log leaves a future Pending task In Progress.

[2026-11-02T11:35:36Z · bob-cli-fl.6.1.2] Implemented the persistent three-clock Stats control, fetch routing, compatible fallback, low-priority prefetching, fixtures, tests, and preview. Focused tests, browser preview, build validation, plugin validation, and bob-cli docs checks pass. Full npm test has four failures reproduced identically on clean base 71ae1cb; recorded as a proposed follow-up. Synced bob-ledger-tools from this linked checkout and verified dry-run reports it up to date.

## Dependencies

- **Depends on:** [bob-cli-fl.6.1.1](bob-cli-fl.6.1.1.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fl.6.1.3](bob-cli-fl.6.1.3.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.2/README.md) | [bob-cli-fl.6.1.2](bob-cli-fl.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3a2b03b`](https://github.com/bobs-org/bob-plugins/commit/3a2b03b635a3e81b343f482e502257d00e2fa4b7) | feat(stats): add persistent clock controls and fetch routing | [bob-cli-fl.6.1.2](bob-cli-fl.6.1.2.md) | 2026-11-02 06:45:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.6.1.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.2/README.md

<!-- sase:referenced-by:end -->
