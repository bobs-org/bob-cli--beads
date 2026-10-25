# Bead: bob-cli-an.1 — Secure Athena supervisor control and its executable chain

[Bead Pages](../README.md) / [bob-cli-an](README.md) / bob-cli-an.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12v.md) · **Assignee:** `bob-cli-an.1` · **Size:** medium
**Created:** 2026-10-21 12:58:23 EDT · **Closed:** 2026-10-21 18:16:17 EDT
**Plan:** [202610/backlog\_security\_and\_durability.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_security_and_durability.md)

## Description

supervisor: resolve bob-cli-8u with restricted authenticated control, protected credentials, root-owned dependencies, and live verification.

## Notes

[2026-10-21T22:16:06Z · bob-cli-an.1--3] Baseline: bob-cli-8u tracked the pre-change 2026-10-17 exposure: unauthenticated root multivisor-rpc on 0.0.0.0:8051, root execution from Bryan-owned pipx code, and a world-readable root config with HTTP credentials. Fix deployed through reviewed gates: removed TCP 8051; runs multivisor-rpc as bryan on IPC; retains root administration via /tmp/supervisor.sock (root:bryan 0770); keeps authenticated HTTP on 127.0.0.1:8001 with rotated credentials; root config is root:root 0600; local Multivisor configs are bryan:bryan 0600; IPC bridge socket is bryan:bryan 0700. Verification: final install/restart passed and approved credential-safe verifier rerun passed (exit 0, output suppressed), including HTTP rejection, nobody denial, authenticated Multivisor, root@athena status, and supervised health. Direct checks as bryan succeeded: supervisorctl via the Unix socket reported both supervised programs RUNNING; ss showed only 127.0.0.1:8001 and no 8051; multivisor-rpc ran as bryan; stat confirmed config/socket modes. Constraints: Bryan retains intended admin access through the protected group socket, the authenticated HTTP endpoint remains loopback-only, and the Bryan-owned venv is used by the unprivileged RPC process. Earlier install/verifier attempts failed; later approved install/restart and verifier rerun passed. Their suppressed output does not identify the earlier causes. Credentials were not recorded.

[2026-10-21T22:16:17Z · bob-cli-an.1--3] Done: approved Athena install and restart passed; credential-safe verifier rerun passed. As bryan, authenticated supervisorctl over /tmp/supervisor.sock reports both managed programs RUNNING; no 8051 listener remains, 8001 is loopback-only, multivisor-rpc runs as bryan, and root/local configs plus IPC sockets have the verified protected ownership and modes. Baseline, fix, verification, and remaining constraints were recorded on this phase and bob-cli-8u. No credentials recorded.

## Dependencies

- **Blocks:** [bob-cli-an.2](bob-cli-an.2.md) ✓ · ⧖ 2026-10-21

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.1--3][1] | Need the phase scope, design file, prior work, and accepted decisions before continuing verification | 2 |
| read-by | [agent:bob-cli-an.4][2] | Need prior phase pattern for host work | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.land--2][3] | Review every ancestor phase note for unresolved follow-ups and completion | 1 |
| read-by | [agent:bob-cli-an.land][4] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md

<!-- sase:referenced-by:end -->
