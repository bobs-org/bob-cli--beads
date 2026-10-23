# Bead: bob-cli-an.6.3 — Restrict Bryan's user Supervisor bridge and the Multivisor web UI

[Bead Pages](../README.md) / [bob-cli-an.6](bob-cli-an.6.md) / bob-cli-an.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md) · **Assignee:** `bob-cli-an.6.3` · **Size:** medium
**Created:** 2026-10-23 12:41:09 EDT · **Closed:** 2026-10-23 13:45:32 EDT
**Plan:** [202610/backlog\_batch2\_athena\_hardening\_and\_ref\_ids.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md)

## Description

user-supervisor: resolve bob-cli-av by moving the unauthenticated user multivisor-rpc bridge off the network and applying the chosen Multivisor web audience.

## Notes

[2026-10-23T16:55:33Z · bob-cli-an.6.3] Baseline 2026-10-23 as bryan: ss shows 0.0.0.0:8052 (multivisor-rpc) and 0.0.0.0:8100 (multivisor). Apollo TCP to 100.87.31.114:8052 and :8100 both open. Live files are ~/.config/supervisor -> ~/db/home/.config/supervisor; chezmoi does not track them. Only consumer of 8052 is local Multivisor (url=localhost:8052). Remote consumer of 8100 is chezmoi alias multivisor-cli --url athena:8100. hera:8051/8052 kept: hera is absent from tailnet inventory, DNS, and tailscale status, with no retirement evidence. Decision: 8100 loopback+tailnet via dedicated nftables table matching iifname lo and tailscale0.

[2026-10-23T16:58:19Z · bob-cli-an.6.3] Unprivileged install done as bryan: install_user_supervisor.py patched ~/.config/supervisor/supervisord.conf and multivisor.conf (password preserved, hera URLs kept). Backups supervisord.conf.bob-cli-av.20261023T165548Z.pre and matching multivisor.conf. Restarted only user multivisor-rpc and supervisor:multivisor; root supervisor PIDs unchanged. verify_user_supervisor.py passed (user IPC bryan:bryan 0700, no TCP 8052, local 8100 401, authenticated login shows root@athena and bryan@athena running). Apollo 100.87.31.114:8052 connection refused; :8100 still open pending nftables boundary.

[2026-10-23T17:45:32Z · bob-cli-an.6.3--1] User multivisor-rpc moved from TCP :8052 to ipc:///tmp/supervisor-user-multivisor.sock (bryan:bryan 0700, umask 077); bryan@athena URL rewritten to that IPC; hera:8051/8052 kept. ss: no :8052 listener; 0.0.0.0:8100 still listens. User programs clipster, dunst, pycron, rfserver, xbindkeys, multivisor-rpc, supervisor:multivisor RUNNING; root multivisor-rpc and supervisor:bryan@athena RUNNING. nftables inet athena_multivisor accepts TCP 8100 on lo and tailscale0 and drops it elsewhere (no hardcoded tailnet address); athena-multivisor-boundary.service active/enabled. Apollo 100.87.31.114:8052 connection refused; :8100 HTTP 401. sudo verify_multivisor_boundary.py foreign-veth probe dropped. bob-cli-av stays open for the lander.

## Dependencies

- **Blocks:** [bob-cli-an.6.4](bob-cli-an.6.4.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.3.md) | [bob-cli-an.6.3](bob-cli-an.6.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.3--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.3.md

<!-- sase:referenced-by:end -->
