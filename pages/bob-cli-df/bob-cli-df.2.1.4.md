# Bead: bob-cli-df.2.1.4 — Repair artifact-link durability ordering and quarantine replay

[Bead Pages](../README.md) / [bob-cli-df.2.1](bob-cli-df.2.1.md) / bob-cli-df.2.1.4

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.land.md) · **Assignee:** `bob-cli-df.2.1.4.land`
**Created:** 2026-10-28 02:07:52 EDT
**Plan:** [202610/artifact\_link\_quarantine\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_quarantine_landing_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/artifact_link_quarantine_landing_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_quarantine_landing_repairs.md

<!-- sase:links:end -->

## Description

Preserve the earliest provable durable payload and make quarantined replays settle idempotently without weakening corruption checks.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.4.land/README.md) | [bob-cli-df.2.1.4](bob-cli-df.2.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.4.1--5][1] | Need parent epic decisions that govern the artifact-link collision ordering phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.1.md

<!-- sase:referenced-by:end -->
