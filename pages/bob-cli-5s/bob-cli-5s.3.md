# Bead: bob-cli-5s.3 — RefsCore target — decoding, item model, fetcher, and stores

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5z.md) · **Assignee:** `bob-cli-5s.3` · **Size:** medium
**Created:** 2026-10-08 19:32:40 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

refs-core-model: add the Foundation-only RefsCore target with lossy decoding of `bob ref list` and `bob plan` JSON, the RefItem/RefKind/RefState/RefScope model, the BobRefsFetcher over BobProcessClient, the snapshot cache and open log stores, fake-bob ref/plan branches, synthetic fixtures, and tests.

## Notes

[2026-10-09T01:38:19Z · bob-cli-5s.3] RefsCore committed as e3f918d to bob-mac-capture master; CI run https://github.com/bobs-org/bob-mac-capture/actions/runs/37870523795

[2026-10-09T01:38:34Z · bob-cli-5s.3] PROPOSED FOLLOW-UP: Write the refs-panel-is-a-thin-client decision strand (Bob Refs ranks bob's reference index and never mutates the vault), linking mac-capture-is-a-thin-client and task-lanes-are-sticky — skipped per refs_decision_memory=no

## Dependencies

- **Depends on:** [bob-cli-5s.1](bob-cli-5s.1.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.4](bob-cli-5s.4.md) ◐ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.3.md) | [bob-cli-5s.3](bob-cli-5s.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.3.md

<!-- sase:referenced-by:end -->
