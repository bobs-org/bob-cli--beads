# Bead: bob-cli-on.15.1.1 — Decode requirement cards and encode gated verdict arguments

[Bead Pages](../README.md) / [bob-cli-on.15.1](bob-cli-on.15.1.md) / bob-cli-on.15.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) · **Assignee:** `bob-cli-on.15.1.1` · **Size:** medium
**Created:** 2026-11-22 14:56:48 EST · **Closed:** 2026-11-22 15:50:08 EST
**Plan:** [202611/mac\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md)

## Description

protocol: add typed requirement capability, group, row, consequence, and receipt models in bob-mac-capture, canonical collection helpers, and capability-gated BobProcessClient arguments. Generate synthetic fixtures from current bob and cover old payloads and requirement-only responses. Follow the protocol section and shared verification rules below; do not activate the card yet.

## Notes

[2026-11-22T20:50:08Z · bob-cli-on.15.1.1] Implemented typed requirement-card capabilities/groups/rows/consequences/receipts, canonical batch collection and stale recovery, and BobProcessClient capability-proof-gated verdict argv. Generated current Bob 0.6.0 synthetic preview, mixed, write, stale, and legacy fixtures; copied req_close vectors byte-for-byte. Verified bash syntax, vector cmp, focused requirement/client suites, and just portable-check (2,685 tests, 1 skipped, 0 failures). epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-on.15.1.2](bob-cli-on.15.1.2.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.15.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.1/README.md) | [bob-cli-on.15.1.1](bob-cli-on.15.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.2][1] | Need to know if the running workspace-11 agent is also deploying cycler or nav before resolving the sync refusal | 1 |
| read-by | [agent:bob-cli-on.15.1.1][2] | Need the phase scope, design file, and prior work notes before implementation | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.1/README.md

<!-- sase:referenced-by:end -->
