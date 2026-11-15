# Bead: bob-cli-ls — Subscriptions album: records that know how they show up on the statement

[Bead Pages](../README.md) / bob-cli-ls

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cp.md) · **Assignee:** `bob-cli-ls.land`
**Created:** 2026-11-15 13:11:21 EST
**Plan:** [202611/bank\_subscriptions\_album.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_subscriptions_album.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md

<!-- sase:links:end -->

## Description

A 🔁 Subscriptions album under bank holds every discretionary recurring charge, seeded from a reviewed bank history. bob bank import links each new matching row to its record, and the link renders as a quiet 🔁 chip. bob bank check and bob bank subscriptions keep the album honest: they flag price changes, charges after a cancel, and possible new subscriptions. The old Zorg recurring table retires without losing a link, and bob-cli-kt closes.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ls.1](bob-cli-ls.1.md) | Seed the album from a reviewed bank history | ✓ closed | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.10](bob-cli-ls.10.md) | Vault acceptance, memory, and closing bob-cli-kt | ◐ in_progress | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.2](bob-cli-ls.2.md) | Subscription registry, match resolver, and ledger | ✓ closed | large | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.3](bob-cli-ls.3.md) | Retire old\_recur.md into a legacy\_recur notebook | ✓ closed | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.4](bob-cli-ls.4.md) | Import links new rows to their subscription | ✓ closed | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.5](bob-cli-ls.5.md) | Subscription findings in bob bank check | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-ls.6](bob-cli-ls.6.md) | The bob bank subscriptions command | ◐ in_progress | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.7](bob-cli-ls.7.md) | 🔁 chips on bank rows | ✓ closed | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.8](bob-cli-ls.8.md) | Category card subscription linker | ◐ in_progress | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.9](bob-cli-ls.9.md) | Record header strip and album summary card | ◐ in_progress | medium | 2026-11-15 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ls: Subscriptions album: records that know how they show up on the statement [in_progress]"]
    n1["bob-cli-ls.1: Seed the album from a reviewed bank history [closed]"]
    n2["bob-cli-ls.10: Vault acceptance, memory, and closing bob-cli-kt [in_progress]"]
    n3["bob-cli-ls.2: Subscription registry, match resolver, and ledger [closed]"]
    n4["bob-cli-ls.2.1: Subscription registry, attribution, and ledger core [closed]"]
    n5["bob-cli-ls.2.1.1: Typed subscription registry and deterministic matching [closed]"]
    n6["bob-cli-ls.2.1.2: Shared charge attribution and subscription ledger [closed]"]
    n7["bob-cli-ls.2.1.3: Guarded loaders, row JSON, suggestions, and documentation [closed]"]
    n8["bob-cli-ls.3: Retire old_recur.md into a legacy_recur notebook [closed]"]
    n9["bob-cli-ls.4: Import links new rows to their subscription [closed]"]
    n10["bob-cli-ls.5: Subscription findings in bob bank check [closed]"]
    n11["bob-cli-ls.6: The bob bank subscriptions command [in_progress]"]
    n12["bob-cli-ls.7: 🔁 chips on bank rows [closed]"]
    n13["bob-cli-ls.8: Category card subscription linker [in_progress]"]
    n14["bob-cli-ls.9: Record header strip and album summary card [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n3 --> n4
    n4 --> n5
    n4 --> n6
    n4 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n0 --> n14
    n1 -.-> n8
    n3 -.-> n9
    n3 -.-> n10
    n3 -.-> n11
    n3 -.-> n12
    n5 -.-> n6
    n5 -.-> n7
    n6 -.-> n7
    n8 -.-> n2
    n9 -.-> n2
    n10 -.-> n11
    n11 -.-> n13
    n11 -.-> n14
    n12 -.-> n13
    n13 -.-> n14
    n14 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.1.md) | [bob-cli-ls.1](bob-cli-ls.1.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.10/README.md) | [bob-cli-ls.10](bob-cli-ls.10.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.md) | [bob-cli-ls.2](bob-cli-ls.2.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.1.1.md) | [bob-cli-ls.2.1.1](bob-cli-ls.2.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.1.2.md) | [bob-cli-ls.2.1.2](bob-cli-ls.2.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.2.1.3/README.md) | [bob-cli-ls.2.1.3](bob-cli-ls.2.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.1.land.md) | [bob-cli-ls.2.1](bob-cli-ls.2.1.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.3/README.md) | [bob-cli-ls.3](bob-cli-ls.3.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.4/README.md) | [bob-cli-ls.4](bob-cli-ls.4.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.5.md) | [bob-cli-ls.5](bob-cli-ls.5.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.6/README.md) | [bob-cli-ls.6](bob-cli-ls.6.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.7/README.md) | [bob-cli-ls.7](bob-cli-ls.7.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.8/README.md) | [bob-cli-ls.8](bob-cli-ls.8.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.9/README.md) | [bob-cli-ls.9](bob-cli-ls.9.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.land/README.md) | [bob-cli-ls](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`96b35f4`](https://github.com/bobs-org/bob-cli/commit/96b35f41c4d20cecc065e85e2fe5ac1d8d191c2c) | feat(bank): add subscription attribution and ledger | [bob-cli-ls.2.1.2](bob-cli-ls.2.1.2.md) | 2026-11-15 16:08:32 EST |
| bob-cli | [`055f9b6`](https://github.com/bobs-org/bob-cli/commit/055f9b6e0558c8458ac37a20d0533f22ac4d5d77) | feat(bank): integrate subscription core into rows, suggestions, and docs | [bob-cli-ls.2.1.3](bob-cli-ls.2.1.3.md) | 2026-11-15 16:51:38 EST |
| bob-cli | [`b8aed5a`](https://github.com/bobs-org/bob-cli/commit/b8aed5a943242a5517a6f536de9914432193ed90) | fix(bank): repair subscription core ledger, import after-state, and guards | [bob-cli-ls.2.1](bob-cli-ls.2.1.md) | 2026-11-15 17:58:47 EST |
| bob-cli | [`cfd4548`](https://github.com/bobs-org/bob-cli/commit/cfd4548a2cd60a165fdbdc67bd0472e2d6968343) | feat(bank): add native bank checks and subscription registry | [bob-cli-ls.5](bob-cli-ls.5.md) | 2026-11-15 18:48:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lr.land][1] | Check whether bank subscription registry dead code breaking just check on master is tracked in-flight work | 1 |
| read-by | [agent:bob-cli-ls.7][2] | Need parent epic DECISIONS and overall design | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lr.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.7/README.md

<!-- sase:referenced-by:end -->
