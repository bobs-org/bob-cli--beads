# Bead: bob-cli-7b.1 — Contract, dependency-drop writer, and the solo link gesture

[Bead Pages](../README.md) / [bob-cli-7b](README.md) / bob-cli-7b.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7c.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7c.w0.md) · **Assignee:** `bob-cli-7b.1` · **Size:** medium
**Created:** 2026-10-13 08:12:08 EDT · **Closed:** 2026-10-13 09:23:19 EDT
**Plan:** [202610/capture\_link\_drops\_blocking\_deps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_link_drops_blocking_deps.md)

## Description

cli-core: write the §13.5 dependency-drop contract and PDG18–PDG27 vectors first, then add the drop verdict, the staged drop writer, the shared guard helper, JSON/human output, and wire `@route:id` / `^route:id` (with `#name` and `=<X>`).

## Notes

[2026-10-13T13:01:46Z · bob-cli-7b.1--1] PROPOSED FOLLOW-UP: clean-base `just check` reproduces the two percent-listen CLI failures (`capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio`, `capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance`), already tracked by bob-cli-6m; the parallel library listen stub ETXTBSY is tracked by bob-cli-5l and passes when isolated.

[2026-10-13T13:23:19Z · bob-cli-7b.1--3] Implemented the dependency-drop contract, staged writer and shared guard, and capture link wiring. The fresh-target just check passed all dependency-drop unit and CLI tests; its only failures were the two known percent-listen CLI tests tracked by bob-cli-6m and already recorded on this bead as reproduced on clean base. sase bead epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-7b.2](bob-cli-7b.2.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7b.3](bob-cli-7b.3.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7b.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7b.1.md) | [bob-cli-7b.1](bob-cli-7b.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`92515f1`](https://github.com/bobs-org/bob-cli/commit/92515f1bb8565fa7d6116e4581911b9f45e880bb) | feat(capture): support dependency-drop link gestures | [bob-cli-7b.1](bob-cli-7b.1.md) | 2026-10-13 09:24:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7b.1--3][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-7b.4][2] | Need cli-core commit for decision evidence | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7b.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.4/README.md

<!-- sase:referenced-by:end -->
