# Bead: bob-cli-k3.4 — Records, capture, and completion read schemas from albums

[Bead Pages](../README.md) / [bob-cli-k3](README.md) / bob-cli-k3.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.43.linker.w0` · **Assignee:** `bob-cli-k3.4` · **Size:** large
**Created:** 2026-11-11 04:56:44 EST · **Closed:** 2026-11-11 13:33:32 EST
**Plan:** [202611/album\_and\_record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md)

## Description

album-records: route all eight config call sites through the registry so record kinds follow `--bob-dir`, write album records as `type: "[[record]]"` under their album, teach `bob records check` the album membership rules, enrich capture, capture-targets, and JSON additively with album identity, and make a bare album route (`Blaze @eat`) a teaching refusal.

## Notes

[2026-11-11T16:57:18Z · bob-cli-k3.4.1.land] Child landing audit found epic-owned routing/diagnostic boundary defects plus unfinished consumer docs/acceptance. See the detailed LANDING AUDIT on bob-cli-k3.4.1. No child PROPOSED FOLLOW-UP entries or independent task proposals require triage. A validated medium repair tale will finish the code, docs, checks, and normal closure of both bob-cli-k3.4.1 and this phase in its own implementation turn; bob-cli-k3 remains open. No fresh test pass is claimed by this audit.

[2026-11-11T18:33:49Z · bob-cli-k3.4.1.land] Phase landing (recorded after epic close cascaded): child epic bob-cli-k3.4.1 delivered the full album-records scope - shared resolved record identity with source/album metadata, album-aware records CLI (noun/stem, membership/checkbox/orphan checks, legacy-type warnings, config deprecation), per-route capture planning with album task-home refusals and owner guidance, and album-aware targets/completion honoring the effective vault. Docs landed (records/capture/capture-syntax/json-outputs/configuration) with transition accurately described and index/catalog rebuild correctly unclaimed. Acceptance: just check fully green (lib 6486, cli 3546, all suites), docs-gen clean, isolated two-album plus unclaimed-config walkthrough verified (noun/stem create, staged multi-item, dry-run/write byte equality, zero dry-run writes, -b precedence, failure isolation, writeless refusals, record-only writes). No leftover epic-symbols on bob-cli-k3.4. Parent epic bob-cli-k3 and plan 202611/album_and_record_notes.md deliberately left open for its land agent. -n

## Dependencies

- **Depends on:** [bob-cli-k3.2](bob-cli-k3.2.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k3.5](bob-cli-k3.5.md) ◐ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k3.8](bob-cli-k3.8.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.4.md) | [bob-cli-k3.4](bob-cli-k3.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.4.1.1][1] | Need the outer epic's binding decisions for this assigned child phase | 1 |
| read-by | [agent:bob-cli-k3.4.1.3][2] | Need assigned phase scope and final decisions | 1 |
| read-by | [agent:bob-cli-k3.4.1.4][3] | Need the parent epic's final decisions before completing album-completion | 1 |
| read-by | [agent:research.47.mus][4] | Need records capture schema details for bank album research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.4.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.4.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.4.1.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.mus/README.md

<!-- sase:referenced-by:end -->
