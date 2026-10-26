# Bead: bob-cli-an — Backlog batch 1: Athena security and vault durability

[Bead Pages](../README.md) / bob-cli-an

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12v.md) · **Assignee:** `bob-cli-an.land`
**Created:** 2026-10-21 12:58:23 EDT · **Closed:** 2026-10-23 12:32:01 EDT
**Plan:** [202610/backlog\_security\_and\_durability.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_security_and_durability.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_security_and_durability.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 9 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_security_and_durability.md

<!-- sase:links:end -->

## Description

Close five prioritized task beads by removing Athena privilege-boundary exposures, restricting monitoring access, preserving ignored vault content, and stabilizing annotation identities. The lander continues the backlog through further epics of at most five phases and five task beads until every project task bead is closed.

## Notes

[2026-10-23T16:31:50Z · bob-cli-an.land] LANDER FOLLOW-UP TRIAGE (bob-cli-an.land): (1) an.2 #3, daily/weekly/monthly root cron bryan-writable chains: created bob-cli-au (medium). (2) an.2 #6, rsync exit-24 discards rotations: semantic duplicate of canceled bob-cli-1a. Recorded a +1 with post-close evidence (hourly rotations land only every third run; latest 04:24 at 12:25; daily, weekly, and monthly also stale), which reopened it as READY. (3) an.3 #2, dead clipster_server scrape: created bob-cli-ax (small). (4) an.3 #3, rfserver 0.0.0.0:23401 boundary: created bob-cli-aw (large); 23401 is reachable from apollo. (5) an.4 #4, apollo .bob/gkeep/migrate-tasks/*.json: declined as a task, because docs/gkeep.md defines these as bob gkeep migrate-tasks crash-recovery and commit-retry receipts (machine-local state). The lander recorded that exclusion justification in docs/vault-git-sync.md, as the proposal's own alternative asked. (6) Lander discovery: Bryan's user supervisord serves unauthenticated multivisor-rpc on 0.0.0.0:8052 (reachable from apollo), and Multivisor web binds 0.0.0.0:8100. Created bob-cli-av (medium). Epic-caused remainder fixed by the lander: phase an.3 never committed its tailnet install source. It was recovered from the workspace-11 SASE rescue patch, verified byte-identical to all seven installed files, and staged in tailnet hosts/athena/monitoring with README install, verify, and rollback steps plus tailnet README index rows.

[2026-10-23T16:32:01Z · bob-cli-an.land] Verified all five phases (an.1-an.5 closed) and closed their tasks with live evidence: 8u, 96, 97, 1g, and 9o. Supervisor: no 8051 listener, 8001 loopback-only, root config 0600, bridge running as bryan over IPC; source in tailnet 6af6375. Root cron: hourly entries are root-owned regular files, byte-identical to tailnet dbb7368, and rotations still land. Monitoring: 9090, 9091, 9100, 9101, and 9093 are loopback-only; remote probes from apollo are denied; the nft boundary service is enabled. The phase's uncommitted tailnet source was recovered from the SASE rescue patch, verified byte-identical to the installed files, and staged for commit. Vault: 4b62d0ac's 80 paths are on origin/master, and no authored-class path remains ignored. Highlight IDs: 51ad4f4c stable planner with regression tests; later epic bob-cli-ap's tucked groups build on the same plan; highlights_ref 596/596 pass; just check exits 0 on c07a65cc; just docs-check passes. Integration: post-start commits reviewed; only bob-cli-ap touched epic code, and it already uses the ID plan. Follow-ups: created bob-cli-au, av, aw, and ax; reopened bob-cli-1a by +1; declined the migrate-tasks receipts task and recorded the exclusion in docs/vault-git-sync.md (see the epic triage note). No epic symbols.

[2026-10-23T16:37:30Z · bob-cli-an.land] CONTINUATION (bob-cli-an.land, 2026-10-23): fresh enumeration after this landing found 155 unresolved tasks (151 ready, 4 snoozed: 3o, 6q, aa, ah; none claimed or in progress). Successor epic 'Backlog batch 2: Athena root, listener, and backup hardening plus reference ID allocation' was authored and submitted through sase plan propose (scratch sase_plan_backlog_batch2_athena_hardening_and_ref_ids.md). It owns exactly bob-cli-au (periodic-cron), bob-cli-1a (backup-rotation, after periodic-cron), bob-cli-av (user-supervisor), bob-cli-aw (rfserver-port, after user-supervisor), and bob-cli-8o (ref-id-allocation), with one reviewer decision (multivisor_web_access, default tailnet) and the verbatim continuation contract. Ranking: security first (au, av, aw), backup content loss next (1a), then the top silent identity defect (8o, chosen over 9a on age and live-vault impact). Next candidates: 9a, 8a, 79, al, 2q, ax; heavily corroborated 6m, 6v, 6w, 7i; detection 8r, 9x. The backlog campaign is not complete.

[2026-10-24T11:29:39Z · bob-cli-an.6.6.6.land] RECHECK after descendant bob-cli-an.6.6.6 closed (2026-10-24). Chain an.6 -> an.6.6 -> an.6.6.6 is closed; epic-symbols empty; linked plan 202610/backlog_security_and_durability.md already status: done. No unfinished descendants. Parent stays closed. Backlog campaign continues.

[2026-10-24T11:29:50Z · bob-cli-an.6.6.6.land] Rechecked after descendant an.6.6.6 closed; already done.

[2026-10-24T16:28:13Z · bob-cli-an.6.6.6.5.6.land--2] POST-BATCH-6 READINESS RECHECK (2026-10-24): 33 descendants; prior security, vault restore, and stable-highlight identity evidence plus all descendant notes reviewed. Later quote-remint behavior changes quote content and preserves old tombstones; unchanged highlight identity stays covered. No host-source drift after accepted tailnet evidence; no new live deployment verification claimed. All descendants closed, linked-plan schema valid, named phase count matches closed phases, plan already status done, and no epic-symbol entries. Fresh global links validation has 64 legacy errors, none affecting campaign plans. No remaining batch-scope blocker found. Preserve closed/done normally; no force. Campaign remains ongoing with 124 unresolved tasks and bounded batch 7 being proposed from an.6.6.6.5.6. No symvision recipe is available.

[2026-10-24T16:28:17Z · bob-cli-an.6.6.6.5.6.land--2] POST-BATCH-6 READINESS RECHECK (2026-10-24): 33 descendants; prior security, vault restore, and stable-highlight identity evidence plus all descendant notes reviewed. Later quote-remint behavior changes quote content and preserves old tombstones; unchanged highlight identity stays covered. No host-source drift after accepted tailnet evidence; no new live deployment verification claimed. All descendants closed, linked-plan schema valid, named phase count matches closed phases, plan already status done, and no epic-symbol entries. Fresh global links validation has 64 legacy errors, none affecting campaign plans. No remaining batch-scope blocker found. Preserve closed/done normally; no force. Campaign remains ongoing with 124 unresolved tasks and bounded batch 7 being proposed from an.6.6.6.5.6. No symvision recipe is available.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-an.1](bob-cli-an.1.md) | Secure Athena supervisor control and its executable chain | ✓ closed | medium | 2026-10-21 | 0 | 0 |
| [bob-cli-an.2](bob-cli-an.2.md) | Remove user-writable code from root hourly jobs | ✓ closed | medium | 2026-10-21 | 0 | 0 |
| [bob-cli-an.3](bob-cli-an.3.md) | Restrict monitoring endpoints to verified clients | ✓ closed | medium | 2026-10-21 | 0 | 0 |
| [bob-cli-an.4](bob-cli-an.4.md) | Preserve ignored vault content off host | ✓ closed | medium | 2026-10-21 | 1 | 1 |
| [bob-cli-an.5](bob-cli-an.5.md) | Preserve highlight IDs across annotation insertion | ✓ closed | medium | 2026-10-21 | 1 | 1 |

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.4/README.md) | [bob-cli-an.4](bob-cli-an.4.md) | 1 |
| [bbugyi200.athena.bob-cli-an.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.5/README.md) | [bob-cli-an.5](bob-cli-an.5.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.5.md) | [bob-cli-an.6.5](bob-cli-an.6.5.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.1/README.md) | [bob-cli-an.6.6.1](bob-cli-an.6.6.1.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.2.md) | [bob-cli-an.6.6.2](bob-cli-an.6.6.2.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.3.md) | [bob-cli-an.6.6.3](bob-cli-an.6.6.3.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.4/README.md) | [bob-cli-an.6.6.4](bob-cli-an.6.6.4.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.5/README.md) | [bob-cli-an.6.6.5](bob-cli-an.6.6.5.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.1.md) | [bob-cli-an.6.6.6.1](bob-cli-an.6.6.6.1.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.2.md) | [bob-cli-an.6.6.6.2](bob-cli-an.6.6.6.2.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.3.md) | [bob-cli-an.6.6.6.3](bob-cli-an.6.6.6.3.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.4/README.md) | [bob-cli-an.6.6.6.4](bob-cli-an.6.6.6.4.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.1/README.md) | [bob-cli-an.6.6.6.5.1](bob-cli-an.6.6.6.5.1.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.2.md) | [bob-cli-an.6.6.6.5.2](bob-cli-an.6.6.6.5.2.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.3/README.md) | [bob-cli-an.6.6.6.5.3](bob-cli-an.6.6.6.5.3.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.4/README.md) | [bob-cli-an.6.6.6.5.4](bob-cli-an.6.6.6.5.4.md) | 2 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.5.md) | [bob-cli-an.6.6.6.5.5](bob-cli-an.6.6.6.5.5.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.1/README.md) | [bob-cli-an.6.6.6.5.6.1](bob-cli-an.6.6.6.5.6.1.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.2.md) | [bob-cli-an.6.6.6.5.6.2](bob-cli-an.6.6.6.5.6.2.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.3/README.md) | [bob-cli-an.6.6.6.5.6.3](bob-cli-an.6.6.6.5.6.3.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.4.md) | [bob-cli-an.6.6.6.5.6.4](bob-cli-an.6.6.6.5.6.4.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.1/README.md) | [bob-cli-an.6.6.6.5.6.5.1](bob-cli-an.6.6.6.5.6.5.1.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.2/README.md) | [bob-cli-an.6.6.6.5.6.5.2](bob-cli-an.6.6.6.5.6.5.2.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.3.md) | [bob-cli-an.6.6.6.5.6.5.3](bob-cli-an.6.6.6.5.6.5.3.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.4/README.md) | [bob-cli-an.6.6.6.5.6.5.4](bob-cli-an.6.6.6.5.6.5.4.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.1/README.md) | [bob-cli-an.6.6.6.5.6.5.5.1](bob-cli-an.6.6.6.5.6.5.5.1.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.2](bob-cli-an.6.6.6.5.6.5.5.2.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.3](bob-cli-an.6.6.6.5.6.5.5.3.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.4](bob-cli-an.6.6.6.5.6.5.5.4.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.5](bob-cli-an.6.6.6.5.6.5.5.5.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.1/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.1](bob-cli-an.6.6.6.5.6.5.5.6.1.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.2](bob-cli-an.6.6.6.5.6.5.5.6.2.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.3](bob-cli-an.6.6.6.5.6.5.5.6.3.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.4](bob-cli-an.6.6.6.5.6.5.5.6.4.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.5](bob-cli-an.6.6.6.5.6.5.5.6.5.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.1/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.1.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.2.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.3.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.4.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.5.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.1.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.1.md) | 0 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.2.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.3.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.4.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.5.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3.md) | 1 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4.md) | 2 |
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5.md) | 1 |

… and 12 more agents

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`51ad4f4`](https://github.com/bobs-org/bob-cli/commit/51ad4f4c77a318519b2039dc1e743ec9c737304f) | feat(highlights-ref): stabilize highlight IDs across sidecar order | [bob-cli-an.5](bob-cli-an.5.md) | 2026-10-21 13:47:57 EDT |
| bob-cli | [`019ffb5`](https://github.com/bobs-org/bob-cli/commit/019ffb5ac4ee1b122fc3a576509acf774a80cf31) | docs(vault-sync): document authored content coverage for vault git backup | [bob-cli-an.4](bob-cli-an.4.md) | 2026-10-22 06:58:44 EDT |
| bob-cli | [`e860379`](https://github.com/bobs-org/bob-cli/commit/e860379a3561eaa400275365ce6788226388aaf9) | docs(vault-sync): justify the gkeep migrate-tasks receipt exclusion | [bob-cli-an](README.md) | 2026-10-23 12:37:43 EDT |
| bob-cli--plans | [`bob-cli--plans@9e07e1b`](https://github.com/bobs-org/bob-cli--plans/commit/9e07e1b059fc04f940022bcf0a0fb2ba0325e265) | chore(backlog): mark batch 1 security and durability plan done | [bob-cli-an](README.md) | 2026-10-23 12:39:25 EDT |
| bob-cli | [`9885bde`](https://github.com/bobs-org/bob-cli/commit/9885bde15100fcf41d5dcc99053c443a184d04d6) | fix(ref): allocate unique IDs from output stems | [bob-cli-an.6.5](bob-cli-an.6.5.md) | 2026-10-23 13:32:20 EDT |
| bob-cli--plans | [`bob-cli--plans@47ac730`](https://github.com/bobs-org/bob-cli--plans/commit/47ac7305e366d008043dfae4dfa40043b8e59b8b) | chore(plans): mark backlog\_batch2\_athena\_hardening\_and\_ref\_ids done | [bob-cli-an.6](bob-cli-an.6.md) | 2026-10-23 17:25:11 EDT |
| bob-cli | [`fb535ef`](https://github.com/bobs-org/bob-cli/commit/fb535ef66d679830e70c5791483248f53760ad20) | fix(ref): resolve relative PDF paths before mapping | [bob-cli-an.6.6.5](bob-cli-an.6.6.5.md) | 2026-10-23 17:48:59 EDT |
| bob-cli | [`37594eb`](https://github.com/bobs-org/bob-cli/commit/37594eb22b89cd403a9fc95e811d1d4e7e421900) | fix(webclip): embed static CID TrueType faces instead of Type 3 | [bob-cli-an.6.6.4](bob-cli-an.6.6.4.md) | 2026-10-23 18:07:21 EDT |
| bob-cli | [`21e674d`](https://github.com/bobs-org/bob-cli/commit/21e674d7aa1e11c065fb5b5fe1ed38ffa4fc860d) | feat(time): honor configured day timezone | [bob-cli-an.6.6.3](bob-cli-an.6.6.3.md) | 2026-10-23 18:21:24 EDT |
| bob-cli | [`339578c`](https://github.com/bobs-org/bob-cli/commit/339578cbe833e0a62f53cfa70fc4e2f4d7fc4d08) | fix(time): date ref captures and Keep notes in the configured day timezone | [bob-cli-an.6.6](bob-cli-an.6.6.md) | 2026-10-24 04:28:14 EDT |
| bob-cli | [`0544315`](https://github.com/bobs-org/bob-cli/commit/05443159b9198948e253b0f3d21c7817ea067591) | fix(time): run a DATE clock command in the configured timezone | [bob-cli-an.6.6](bob-cli-an.6.6.md) | 2026-10-24 04:39:12 EDT |
| bob-cli | [`c7e0dab`](https://github.com/bobs-org/bob-cli/commit/c7e0dab6903008ef80a979980446503761bb38cb) | fix(ref): keep the library spelling for PDFs reached through a symlink | [bob-cli-an.6.6](bob-cli-an.6.6.md) | 2026-10-24 05:24:47 EDT |
| bob-cli--plans | [`bob-cli--plans@8a7199e`](https://github.com/bobs-org/bob-cli--plans/commit/8a7199e5b45ca43b763af8df3e369aee9bad07a4) | chore(plans): mark backlog batch 3 done | [bob-cli-an.6.6](bob-cli-an.6.6.md) | 2026-10-24 05:34:27 EDT |
| bob-cli | [`30f10f1`](https://github.com/bobs-org/bob-cli/commit/30f10f154afb119a51a5ebf27264538342973c88) | fix(ci): persist scratch vault git identity | [bob-cli-an.6.6.6.1](bob-cli-an.6.6.6.1.md) | 2026-10-24 06:04:06 EDT |
| bob-plugins | [`bob-plugins@e6b2ec2`](https://github.com/bobs-org/bob-plugins/commit/e6b2ec2dba4c4a6b865faccbc2e3cad59fef4f10) | fix(plugins): repair frozen-clock tests and reverse BLOCKS links | [bob-cli-an.6.6.6.3](bob-cli-an.6.6.6.3.md) | 2026-10-24 06:13:05 EDT |
| bob-cli | [`0afeb2f`](https://github.com/bobs-org/bob-cli/commit/0afeb2f3e744ee2ee775172d5c161eadd45e247b) | feat(capture)!: refuse unknown flags via capture\_flag\_guard | [bob-cli-an.6.6.6.2](bob-cli-an.6.6.6.2.md) | 2026-10-24 06:27:36 EDT |
| bob-cli | [`3d62fb5`](https://github.com/bobs-org/bob-cli/commit/3d62fb548fde190cddad0e8d5b2b80a23bde1e0c) | fix(capture): walk mixed short clusters before unknown-flag refusal | [bob-cli-an.6.6.6](bob-cli-an.6.6.6.md) | 2026-10-24 07:33:27 EDT |
| bob-cli--plans | [`bob-cli--plans@0a8ca46`](https://github.com/bobs-org/bob-cli--plans/commit/0a8ca4610cc97eacdda6b71b01867d9c78035aca) | chore(plans): mark backlog batch 4 epic plan done | [bob-cli-an.6.6.6](bob-cli-an.6.6.6.md) | 2026-10-24 07:34:52 EDT |
| bob-cli | [`ae025fd`](https://github.com/bobs-org/bob-cli/commit/ae025fd0f374225350ac8edbf74bca0ad89bd05a) | fix(task-status-hooks): dedupe completed Task Link into occupied Pomodoro | [bob-cli-an.6.6.6.5.4](bob-cli-an.6.6.6.5.4.md) | 2026-10-24 08:01:57 EDT |
| bob-plugins | [`bob-plugins@0dbd767`](https://github.com/bobs-org/bob-plugins/commit/0dbd767123e8b6d2decb722a18bf2ea43afd1192) | test(task-status-cycler): no duplicate daily Task Link into completed fallback | [bob-cli-an.6.6.6.5.4](bob-cli-an.6.6.6.5.4.md) | 2026-10-24 08:03:42 EDT |
| bob-cli | [`215d93c`](https://github.com/bobs-org/bob-cli/commit/215d93c7eb806e033b084951eea38db3dd8906c0) | fix(highlights-ref): keep heading-shaped wrap lines inside quotes | [bob-cli-an.6.6.6.5.1](bob-cli-an.6.6.6.5.1.md) | 2026-10-24 08:05:05 EDT |
| bob-cli | [`adb9c32`](https://github.com/bobs-org/bob-cli/commit/adb9c324364b0a383d4f71bb25f5b3c86c4dfaab) | fix(capture): reuse completed multi-word pomodoro names without forking spelling | [bob-cli-an.6.6.6.5.3](bob-cli-an.6.6.6.5.3.md) | 2026-10-24 08:05:23 EDT |
| bob-cli | [`bff7bc7`](https://github.com/bobs-org/bob-cli/commit/bff7bc724b5ac854c554ed916a13f5802dede634) | fix(highlights): exclude color-grouped setext title-prefixed marker mirrors | [bob-cli-an.6.6.6.5.2](bob-cli-an.6.6.6.5.2.md) | 2026-10-24 08:41:38 EDT |
| bob-cli | [`8ba5f8d`](https://github.com/bobs-org/bob-cli/commit/8ba5f8d78347698df9667ac9dfd186ace1275a05) | test: cover reconcile completed-fallback dedupe and drop live-vault sidecar test | [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) | 2026-10-24 09:30:10 EDT |
| bob-cli--plans | [`bob-cli--plans@2b31408`](https://github.com/bobs-org/bob-cli--plans/commit/2b31408a05bef2949a1f5e80cef0de23e309eb35) | chore(plans): mark backlog batch 5 epic done | [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) | 2026-10-24 09:31:07 EDT |
| bob-plugins | [`bob-plugins@42f86c8`](https://github.com/bobs-org/bob-plugins/commit/42f86c8381c4bdf21d51e1ee7d915314285749e2) | fix(navigation): follow task positions through generated BLOCKS edits | [bob-cli-an.6.6.6.5.6.2](bob-cli-an.6.6.6.5.6.2.md) | 2026-10-24 10:18:14 EDT |
| bob-cli | [`5d1f8ec`](https://github.com/bobs-org/bob-cli/commit/5d1f8ecca3a389332348fd8e3d637eb9c9d466a5) | fix(highlights-ref): keep hard-wrapped quote lines inside color-grouped highlights | [bob-cli-an.6.6.6.5.6.1](bob-cli-an.6.6.6.5.6.1.md) | 2026-10-24 10:20:34 EDT |
| bob-plugins | [`bob-plugins@3a7368a`](https://github.com/bobs-org/bob-plugins/commit/3a7368a1c8cc94bfde9fe6c5ac217c16f5bf6e49) | fix(navigation): preserve project promotion anchors across frontmatter writes | [bob-cli-an.6.6.6.5.6.3](bob-cli-an.6.6.6.5.6.3.md) | 2026-10-24 10:47:21 EDT |
| bob-cli--plans | [`bob-cli--plans@200c7ac`](https://github.com/bobs-org/bob-cli--plans/commit/200c7ac89799b193acaa73da6e4e0c550f37ab29) | docs(plans): mark backlog batch 6 complete | [bob-cli-an.6.6.6.5.6](bob-cli-an.6.6.6.5.6.md) | 2026-10-24 12:28:47 EDT |
| bob-cli | [`e3754c0`](https://github.com/bobs-org/bob-cli/commit/e3754c0ddbb8531265668fbfcedab227e6ae4884) | feat(web-clip): improve Gist author and title metadata | [bob-cli-an.6.6.6.5.6.5.2](bob-cli-an.6.6.6.5.6.5.2.md) | 2026-10-24 12:50:17 EDT |
| bob-cli | [`f2524e8`](https://github.com/bobs-org/bob-cli/commit/f2524e8053471e73421aaf75430a03bd0cd485e9) | fix(highlights-ref): normalize URL identity escapes for shared dedupe key | [bob-cli-an.6.6.6.5.6.5.1](bob-cli-an.6.6.6.5.6.5.1.md) | 2026-10-24 12:55:53 EDT |
| bob-cli | [`ae993b5`](https://github.com/bobs-org/bob-cli/commit/ae993b5bbcd4c2b00b153b8ff96303b4efa9d67e) | fix(capture): resolve close headline after ledger edits | [bob-cli-an.6.6.6.5.6.5.3](bob-cli-an.6.6.6.5.6.5.3.md) | 2026-10-24 13:12:24 EDT |
| bob-cli | [`a75c55f`](https://github.com/bobs-org/bob-cli/commit/a75c55f990ece7b12521c22f0c61f4bc1e45b38c) | fix(highlights-ref): limit the %40 URL identity alias to Medium author paths | [bob-cli-an.6.6.6.5.6.5](bob-cli-an.6.6.6.5.6.5.md) | 2026-10-25 07:44:19 EDT |
| bob-cli--plans | [`bob-cli--plans@63eb788`](https://github.com/bobs-org/bob-cli--plans/commit/63eb788c0ec26db11a5abe1eaf1255d5adea3dd5) | chore(plans): mark backlog batch 7 and its landing tale done | [bob-cli-an.6.6.6.5.6.5](bob-cli-an.6.6.6.5.6.5.md) | 2026-10-25 07:45:23 EDT |
| bob-plugins | [`bob-plugins@ab71502`](https://github.com/bobs-org/bob-plugins/commit/ab7150284f726e54a4442d455ba0c11d81433d56) | test(nav): de-flake 1000-task stage-ranker 16ms budget with warmed best-of-7 timing | [bob-cli-an.6.6.6.5.6.5.5.4](bob-cli-an.6.6.6.5.6.5.5.4.md) | 2026-10-25 08:00:14 EDT |
| bob-cli | [`f4f6a9c`](https://github.com/bobs-org/bob-cli/commit/f4f6a9caa3968a1dc2751baa4cfb2faca804f670) | test(native): route lib-test executable stubs through fork-safe shared writer | [bob-cli-an.6.6.6.5.6.5.5.5](bob-cli-an.6.6.6.5.6.5.5.5.md) | 2026-10-25 08:09:00 EDT |
| bob-cli--plans | [`bob-cli--plans@1fd04a0`](https://github.com/bobs-org/bob-cli--plans/commit/1fd04a079b3b88d14acb0201086d54c715686c9e) | chore(plans): mark backlog batch 8 epic plan done | [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) | 2026-10-25 08:41:59 EDT |
| bob-cli | [`f255819`](https://github.com/bobs-org/bob-cli/commit/f255819acae8185061c0c3bd4300f74aa9f11f8a) | fix(ref-library): prune .git during snapshot traversal | [bob-cli-an.6.6.6.5.6.5.5.6.5](bob-cli-an.6.6.6.5.6.5.5.6.5.md) | 2026-10-25 08:58:14 EDT |
| bob-cli | [`0e75ca5`](https://github.com/bobs-org/bob-cli/commit/0e75ca56901ff6f023416eb0b119d348d8aaf860) | test(capture): make related perf gate tolerate parallel load | [bob-cli-an.6.6.6.5.6.5.5.6.4](bob-cli-an.6.6.6.5.6.5.5.6.4.md) | 2026-10-25 09:05:07 EDT |
| bob-cli | [`6292c35`](https://github.com/bobs-org/bob-cli/commit/6292c35b61aa230b24b070523341b85576eeae54) | fix(cli): exit 0 quietly on EPIPE instead of panicking | [bob-cli-an.6.6.6.5.6.5.5.6.1](bob-cli-an.6.6.6.5.6.5.5.6.1.md) | 2026-10-25 09:10:13 EDT |
| bob-cli | [`f1ab0df`](https://github.com/bobs-org/bob-cli/commit/f1ab0df9d37759b330f628aee343024577b99140) | fix(cli): quiet EPIPE guard keeps usage-error exit 2 and panic output | [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) | 2026-10-25 09:58:47 EDT |
| bob-cli--plans | [`bob-cli--plans@af3b30c`](https://github.com/bobs-org/bob-cli--plans/commit/af3b30c5c2d6b941b95a4f684e4420d2c813db23) | chore(plans): mark batch 9 plan done after EPIPE hook closeout | [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) | 2026-10-25 09:59:38 EDT |
| bob-cli | [`7e8ffed`](https://github.com/bobs-org/bob-cli/commit/7e8ffedd292dc901ba7d14f57fcd72a0b09a6bcf) | fix(url-routing): keep explicit non-default ports in dedupe and display URLs | [bob-cli-an.6.6.6.5.6.5.5.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.1.md) | 2026-10-25 10:16:07 EDT |
| bob-cli | [`633bc3f`](https://github.com/bobs-org/bob-cli/commit/633bc3f6045b5d80e252c7d1f31780d2f438030d) | docs(capture): clarify unknown-flag guard in TEXT help | [bob-cli-an.6.6.6.5.6.5.5.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.2.md) | 2026-10-25 10:16:59 EDT |
| bob-cli | [`3eebe47`](https://github.com/bobs-org/bob-cli/commit/3eebe47f459207d61d05801347a90dde41b0a909) | fix(highlights): require pdftotext for diagram PDF assertions | [bob-cli-an.6.6.6.5.6.5.5.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.4.md) | 2026-10-25 10:24:19 EDT |
| bob-cli | [`8994514`](https://github.com/bobs-org/bob-cli/commit/89945148d2ed4f051e6d969cfc0f4bd6d66ed40d) | feat(ref-doctor): flag id/stem mismatches and duplicate ids with rename repair | [bob-cli-an.6.6.6.5.6.5.5.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.3.md) | 2026-10-25 10:35:51 EDT |
| bob-cli | [`ba52374`](https://github.com/bobs-org/bob-cli/commit/ba523746df6fd21308193bbc14f7b59a76ba9529) | fix(ref-doctor): fold reference ids ASCII-only and drop pandoc from the repair test | [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) | 2026-10-25 11:00:19 EDT |
| bob-cli--plans | [`bob-cli--plans@2d0fa85`](https://github.com/bobs-org/bob-cli--plans/commit/2d0fa854ce4865da83ebf775b6f936b28cd07e43) | chore(plans): mark backlog batch 10 plan done | [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) | 2026-10-25 11:02:33 EDT |
| bob-cli | [`41cd374`](https://github.com/bobs-org/bob-cli/commit/41cd37487779a54187675445531557d3ab26879d) | fix(ref-doctor): accept the duplicate-avoiding \_N id suffix | [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) | 2026-10-25 11:25:05 EDT |
| bob-plugins | [`bob-plugins@c07b125`](https://github.com/bobs-org/bob-plugins/commit/c07b1257178e76034ee668e4a4d040e1cbb5d0ed) | fix(nav-hotkeys): restore Task Card close cleanup in onClose | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.2.md) | 2026-10-25 11:42:01 EDT |

… and 11 more commits

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.1--3][1] | Verify the parent epic remains open after closing its phase | 1 |
| read-by | [agent:bob-cli-an.4][2] | Need epic context for phase an.4 | 2 |
| read-by | [agent:bob-cli-an.5][3] | Need parent epic context and decisions | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.5--2][4] | Confirm the phase ancestor was left unclosed | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.land][5] | Parent traversal after batch-7 landing: confirm status, plan, and parent link | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.land--2][6] | Recheck campaign root prior landing and descendant readiness | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.land][7] | Recheck closed plan ancestors of bob-cli-an.6.6.6.5 after landing | 1 |
| read-by | [agent:bob-cli-an.6.land][8] | Need the parent link, previous landing note, and campaign context | 1 |
| read-by | [agent:bob-cli-an.land][9] | Need the epic scope, children, and linked plan file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.5.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.land.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.land.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md
[9]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md

<!-- sase:referenced-by:end -->
