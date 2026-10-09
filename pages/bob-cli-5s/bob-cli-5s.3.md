# Bead: bob-cli-5s.3 — RefsCore target — decoding, item model, fetcher, and stores

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.5z` · **Assignee:** `bob-cli-5s.3` · **Size:** medium
**Created:** 2026-10-08 19:32:40 EDT · **Closed:** 2026-10-08 21:54:19 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

refs-core-model: add the Foundation-only RefsCore target with lossy decoding of `bob ref list` and `bob plan` JSON, the RefItem/RefKind/RefState/RefScope model, the BobRefsFetcher over BobProcessClient, the snapshot cache and open log stores, fake-bob ref/plan branches, synthetic fixtures, and tests.

## Notes

[2026-10-09T01:38:19Z · bob-cli-5s.3] RefsCore committed as e3f918d to bob-mac-capture master; CI run https://github.com/bobs-org/bob-mac-capture/actions/runs/37870523795

[2026-10-09T01:38:34Z · bob-cli-5s.3] PROPOSED FOLLOW-UP: Write the refs-panel-is-a-thin-client decision strand (Bob Refs ranks bob's reference index and never mutates the vault), linking mac-capture-is-a-thin-client and task-lanes-are-sticky — skipped per refs_decision_memory=no

[2026-10-09T01:54:19Z · bob-cli-5s.3--1] RefsCore done and CI green: run https://github.com/bobs-org/bob-mac-capture/actions/runs/37871610495 at SHA 3937b0f4ce496e216b1abf1f30ec4699781a4156; macOS CI passed lint, build, and all 1368 swift tests (fixed testOpenLogAppendsLoadsAndResets clock-prune failure from run 37870523795 by pinning now). No --epic-symbol leftovers; RefsCore sources and tests verified present.

## Dependencies

- **Depends on:** [bob-cli-5s.1](bob-cli-5s.1.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.4](bob-cli-5s.4.md) ✓ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.3/README.md) | [bob-cli-5s.3](bob-cli-5s.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e3f918d`](https://github.com/bobs-org/bob-mac-capture/commit/e3f918d757f39133a1e31781f153219615ee37d0) | feat(refs): add RefsCore decoding, model, fetcher, and stores | [bob-cli-5s.3](bob-cli-5s.3.md) | 2026-10-08 21:35:34 EDT |
| bob-mac-capture | [`bob-mac-capture@3937b0f`](https://github.com/bobs-org/bob-mac-capture/commit/3937b0f4ce496e216b1abf1f30ec4699781a4156) | fix(refs): pin open-log append test clock so prune keeps fixtures | [bob-cli-5s.3](bob-cli-5s.3.md) | 2026-10-08 21:49:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.3][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-5s.3--1][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5s.3.md

<!-- sase:referenced-by:end -->
