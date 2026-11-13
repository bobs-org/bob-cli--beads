# Bead: bob-cli-l5.3.1 — Complete the Google Calendar ack command

[Bead Pages](../README.md) / [bob-cli-l5.3](bob-cli-l5.3.md) / bob-cli-l5.3.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-l5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-l5.3.md) · **Assignee:** `bob-cli-l5.3.1.land`
**Created:** 2026-11-12 20:43:26 EST
**Plan:** [202611/gcal\_ack\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_ack_cli.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gcal_ack_cli.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_ack_cli.md

<!-- sase:links:end -->

## Description

Complete bob-cli-l5.3 with a tested one-key external-event review queue, shared private-note editing, noninteractive ack management, and stale/doctor diagnostics, then close only that containing phase through this child's land agent.

## Notes

[2026-11-13T04:45:14Z · bob-cli-kx.2.1.land] DISCOVERED ISSUE: (from bob-cli-kx.2.1.land) Commit 1863b39b (bob-cli-l5.3.1.2, 'add external event ack CLI') added a catalog entry and bumped src/native/catalog/tests.rs to 98, but left tests/cli/catalog.rs:42 at 97. On master 1863b39b, cargo test --test cli catalog::protocol_1_parses_with_schema_version_one fails deterministically (left 98, right 97), both alone and in the full just check. Fix: update the CLI catalog count (and any entry assertions for gcal-ack) alongside the lib test. Phase bob-cli-l5.3.1.4 (CLI verification) is the natural owner.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-l5.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.land/README.md) | [bob-cli-l5.3.1](bob-cli-l5.3.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-l5.3.1.1][1] | Need parent epic scope and DECISIONS | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.1/README.md

<!-- sase:referenced-by:end -->
