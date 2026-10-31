# Bead: bob-cli-ez.1 — Keep adapter hardening

[Bead Pages](../README.md) / [bob-cli-ez](README.md) / bob-cli-ez.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2y.linker.w0.md) · **Assignee:** `bob-cli-ez.1` · **Size:** small
**Created:** 2026-10-31 13:32:41 EDT · **Closed:** 2026-10-31 13:45:37 EDT
**Plan:** [202610/gkeep\_footer\_indicator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gkeep_footer_indicator.md)

## Description

keep-adapter-hardening: bound gkeepapi's endless 429 retry, classify rate-limit 403s as rate_limit, stop network blips from forcing a full resync, and drop the redundant state save in the Python adapter, with self-tests.

## Notes

[2026-10-31T17:45:19Z · bob-cli-ez.1] PROPOSED FOLLOW-UP: consider a decisions-web record that bob owns the Keep count, its cache, and its check budget (epic auto-decision was no; revisit in keep-indicator-actions land agent if check-budget disputes arise)

[2026-10-31T17:45:37Z · bob-cli-ez.1] keep-adapter-hardening done in 5eade952: bounded gkeepapi 429 retry (3 attempts, sleeps 2s/4s, version-guarded on 0.17.1), 403 rateLimitExceeded/userRateLimitExceeded mapped to rate_limit in classify_error and _auth_error, connect() stateless retry narrowed to non-auth/network/rate_limit, op_snapshot redundant save dropped, docs note added. Verified: just check-adapter ok, cargo test gkeep 142 passed 0 failed, no Rust touch needed (adapter.rs already maps rate_limit).

## Dependencies

- **Blocks:** [bob-cli-ez.3](bob-cli-ez.3.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ez.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ez.1/README.md) | [bob-cli-ez.1](bob-cli-ez.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bb3a2f4`](https://github.com/bobs-org/bob-cli/commit/bb3a2f4166d0366232cbe0b05b6916de6f4afc00) | fix(gkeep): bound adapter 429 retries and classify rate-limit 403s | [bob-cli-ez.1](bob-cli-ez.1.md) | 2026-10-31 13:46:52 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ez.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ez.1/README.md

<!-- sase:referenced-by:end -->
