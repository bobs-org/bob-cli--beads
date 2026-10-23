# Bead: bob-cli-an.6.4 — Decide and enforce rfserver's function-port boundary

[Bead Pages](../README.md) / [bob-cli-an.6](bob-cli-an.6.md) / bob-cli-an.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md) · **Assignee:** `bob-cli-an.6.4` · **Size:** medium
**Created:** 2026-10-23 12:41:09 EDT · **Closed:** 2026-10-23 14:26:40 EDT
**Plan:** [202610/backlog\_batch2\_athena\_hardening\_and\_ref\_ids.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md)

## Description

rfserver-port: resolve bob-cli-aw by inventorying port 23401 clients, choosing the narrowest boundary that keeps them working, and verifying allowed and denied access.

## Notes

[2026-10-23T18:20:00Z · bob-cli-an.6.4] Baseline 2026-10-23 as bryan: rfserver (tools:rfserver, PID 3181265) on 0.0.0.0:23401 with token-authed /sendmail; metrics already 127.0.0.1:9101. Apollo probes: tailnet 100.87.31.114:23401 OPEN, public 72.76.171.141:23401 CLOSED (router no longer forwards; WAN scanners reached it in 2021-2023 per rfserver.log: Censys 162.142.125.x/167.248.133.x plus others, latest Jul 2023). Client matrix: local pymail CLI (rfuncs client.post to $RFSERVER_HOSTNAME) incl. root send2en wrapper; server-side routes.py imports pymail module directly (no HTTP, unaffected); NO remote/tailnet/LAN callers (apollo grep clean, no cron/pycron callers, no 2024-2025 pymail use in shell history, hera 2020 use retired with host). Local clients currently broken: RFSERVER_HOSTNAME=bbugyi.ddns.net=public IP, no NAT loopback (self-connect refused). Decision: narrowest boundary is loopback-only; no trade-off found so no questions asked. Fix applied unprivileged in live-host source ~/db/bin/main/rfuncs/server.py (bbugyi200/scripts, unregistered local checkout, edited directly like prior host phases; batch-1 metrics-loopback precedent left uncommitted there too): make_server("",port) -> make_server("127.0.0.1",port). Test kept: db/bin/tests/test_rfserver.py asserts loopback bind + loopback TCP reachability; FAILS on HEAD version (host ""), PASSES on fixed. Restarted tools:rfserver via user supervisorctl (PID 969679); ss shows 127.0.0.1:23401 only. Verified allowed without sending mail: bad-token POST -> 401 Bad Access Token, no-token -> 401, dispatcher logged New Client Request. Verified denied: apollo tailnet probe refused, apollo WAN probe refused; LAN covered by ss (no non-lo listener). Remaining: persistent client endpoint RFSERVER_HOSTNAME=bbugyi.ddns.net lives in root-owned /etc/environment (PAM source for all logins); changing it needs a reviewed sudo gate, requested next. Residual (not fixed, out of scope): PathDispatcher trusts X-Forwarded-For for suspension bucketing; static-token brute force is suspension-only. PROPOSED FOLLOW-UP: consider dropping XFF trust in _get_client_address since no proxy fronts rfserver.

[2026-10-23T18:26:40Z · bob-cli-an.6.4--1] Verified loopback boundary: fresh ssh login RFSERVER_HOSTNAME=127.0.0.1 and /etc/environment line; ss shows 127.0.0.1:23401 only (0.0.0.0:23401 count 0); bad-token POST to 127.0.0.1:23401/sendmail returns 401; apollo tailnet probe to 100.87.31.114:23401 refused (curl 7/nc refused) and public 72.76.171.141:23401 filtered (curl 28/nc timeout 124, ddns same IP); rfserver PID 969679 running; epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-an.6.3](bob-cli-an.6.3.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.4.md) | [bob-cli-an.6.4](bob-cli-an.6.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md

<!-- sase:referenced-by:end -->
