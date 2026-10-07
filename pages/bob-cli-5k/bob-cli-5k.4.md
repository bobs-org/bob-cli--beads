# Bead: bob-cli-5k.4 — Repair the artifact-link event store

[Bead Pages](../README.md) / [bob-cli-5k](README.md) / bob-cli-5k.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0y2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y2.md) · **Assignee:** `bob-cli-5k.4` · **Size:** large
**Created:** 2026-10-07 14:38:41 EDT · **Closed:** 2026-10-07 15:36:44 EDT
**Plan:** [202610/close\_top\_ten\_impact\_beads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/close_top_ten_impact_beads.md)

## Description

link-store: plan and run a backed-up data repair of the colliding operation_id events in the plans sidecar so `sase artifact doctor` is healthy and typed links write again, backfill the relations kept as free text, propose the sase hardening as follow-ups, and close bob-cli-21.

## Notes

[2026-10-07T19:35:51Z · bob-cli-5k.4] PROPOSED FOLLOW-UP: one bad historical artifact-link event pair must not block every future write — whole-store validation fails every link add while one operation id has two canonical payloads; quarantine that pair instead of rejecting the store.

[2026-10-07T19:35:55Z · bob-cli-5k.4] PROPOSED FOLLOW-UP: sase plan propose must validate or publish the links: inlet before consuming the scratch plan, or roll the archive back on failure — a links: inlet currently archives the plan and crashes before the approval gate.

[2026-10-07T19:35:59Z · bob-cli-5k.4] PROPOSED FOLLOW-UP: drain or compact the bob-cli artifact-link outbox — on 2026-10-07 it held 12918 lines and 511 unpublished operation ids because publication refused while the store was invalid; this repair does not drain them.

[2026-10-07T19:36:44Z · bob-cli-5k.4] Repair complete. Event validation/reduction clean (duplicate ids none), artifact-link errors none, cutover imported; link list bead:bob-cli-5i shows related 4j/3c/52; all 14 backfill pairs written or skipped as already listed; epic-symbols clean (no entries, nothing to re-key); three hardening follow-ups noted; epic bob-cli-5k left open. Residual doctor exit 1 is pre-existing research dangling/orphaned plus undrained outbox backlog, out of scope.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.4.md) | [bob-cli-5k.4](bob-cli-5k.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@81b3f88`](https://github.com/bobs-org/bob-cli--plans/commit/81b3f880841807b1d5a00d54de05888ca2c12813) | fix(artifact-links): drop replayed derived link events that reused operation ids | [bob-cli-5k.4](bob-cli-5k.4.md) | 2026-10-07 15:12:14 EDT |
