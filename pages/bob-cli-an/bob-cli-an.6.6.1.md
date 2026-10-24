# Bead: bob-cli-an.6.6.1 — Stop rfserver trusting X-Forwarded-For for token suspension

[Bead Pages](../README.md) / [bob-cli-an.6.6](bob-cli-an.6.6.md) / bob-cli-an.6.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md) · **Assignee:** `bob-cli-an.6.6.1` · **Size:** small
**Created:** 2026-10-23 17:27:15 EDT · **Closed:** 2026-10-23 17:32:45 EDT
**Plan:** [202610/backlog\_batch3\_rfserver\_backups\_day\_zone\_webclip\_fonts\_ref\_paths.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch3_rfserver_backups_day_zone_webclip_fonts_ref_paths.md)

## Description

rfserver-suspension: resolve bob-cli-b3 by keying rfserver auth suspension on REMOTE_ADDR only, with a regression, a durable tailnet record, and a single-program restart.

## Notes

[2026-10-23T21:32:45Z · bob-cli-an.6.6.1] bob-cli-b3 fixed: _get_client_address returns REMOTE_ADDR only (XFF branch deleted). Verified: scratch probe showed varying XFF never SUSPENDED pre-fix; 3 live regressions pass (loopback bind + 2 suspension tests); tailnet hosts/athena/rfserver updated (server-suspension.patch reverse-applies clean, test copy identical, README verify/rollback/residual-risk updated); tools:rfserver restarted via user Supervisor (RUNNING); ss shows 127.0.0.1:23401 only; single loopback bad-token form POST returned 401. No epic symbols remain. Task bead bob-cli-b3 left open for lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.1/README.md) | [bob-cli-an.6.6.1](bob-cli-an.6.6.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-an.6.6.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.land/README.md

<!-- sase:referenced-by:end -->
