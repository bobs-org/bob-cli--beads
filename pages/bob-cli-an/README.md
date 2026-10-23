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

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_security_and_durability.md

<!-- sase:links:end -->

## Description

Close five prioritized task beads by removing Athena privilege-boundary exposures, restricting monitoring access, preserving ignored vault content, and stabilizing annotation identities. The lander continues the backlog through further epics of at most five phases and five task beads until every project task bead is closed.

## Notes

[2026-10-23T16:31:50Z · bob-cli-an.land] LANDER FOLLOW-UP TRIAGE (bob-cli-an.land): (1) an.2 #3, daily/weekly/monthly root cron bryan-writable chains: created bob-cli-au (medium). (2) an.2 #6, rsync exit-24 discards rotations: semantic duplicate of canceled bob-cli-1a. Recorded a +1 with post-close evidence (hourly rotations land only every third run; latest 04:24 at 12:25; daily, weekly, and monthly also stale), which reopened it as READY. (3) an.3 #2, dead clipster_server scrape: created bob-cli-ax (small). (4) an.3 #3, rfserver 0.0.0.0:23401 boundary: created bob-cli-aw (large); 23401 is reachable from apollo. (5) an.4 #4, apollo .bob/gkeep/migrate-tasks/*.json: declined as a task, because docs/gkeep.md defines these as bob gkeep migrate-tasks crash-recovery and commit-retry receipts (machine-local state). The lander recorded that exclusion justification in docs/vault-git-sync.md, as the proposal's own alternative asked. (6) Lander discovery: Bryan's user supervisord serves unauthenticated multivisor-rpc on 0.0.0.0:8052 (reachable from apollo), and Multivisor web binds 0.0.0.0:8100. Created bob-cli-av (medium). Epic-caused remainder fixed by the lander: phase an.3 never committed its tailnet install source. It was recovered from the workspace-11 SASE rescue patch, verified byte-identical to all seven installed files, and staged in tailnet hosts/athena/monitoring with README install, verify, and rollback steps plus tailnet README index rows.

[2026-10-23T16:32:01Z · bob-cli-an.land] Verified all five phases (an.1-an.5 closed) and closed their tasks with live evidence: 8u, 96, 97, 1g, and 9o. Supervisor: no 8051 listener, 8001 loopback-only, root config 0600, bridge running as bryan over IPC; source in tailnet 6af6375. Root cron: hourly entries are root-owned regular files, byte-identical to tailnet dbb7368, and rotations still land. Monitoring: 9090, 9091, 9100, 9101, and 9093 are loopback-only; remote probes from apollo are denied; the nft boundary service is enabled. The phase's uncommitted tailnet source was recovered from the SASE rescue patch, verified byte-identical to the installed files, and staged for commit. Vault: 4b62d0ac's 80 paths are on origin/master, and no authored-class path remains ignored. Highlight IDs: 51ad4f4c stable planner with regression tests; later epic bob-cli-ap's tucked groups build on the same plan; highlights_ref 596/596 pass; just check exits 0 on c07a65cc; just docs-check passes. Integration: post-start commits reviewed; only bob-cli-ap touched epic code, and it already uses the ID plan. Follow-ups: created bob-cli-au, av, aw, and ax; reopened bob-cli-1a by +1; declined the migrate-tasks receipts task and recorded the exclusion in docs/vault-git-sync.md (see the epic triage note). No epic symbols.

[2026-10-23T16:37:30Z · bob-cli-an.land] CONTINUATION (bob-cli-an.land, 2026-10-23): fresh enumeration after this landing found 155 unresolved tasks (151 ready, 4 snoozed: 3o, 6q, aa, ah; none claimed or in progress). Successor epic 'Backlog batch 2: Athena root, listener, and backup hardening plus reference ID allocation' was authored and submitted through sase plan propose (scratch sase_plan_backlog_batch2_athena_hardening_and_ref_ids.md). It owns exactly bob-cli-au (periodic-cron), bob-cli-1a (backup-rotation, after periodic-cron), bob-cli-av (user-supervisor), bob-cli-aw (rfserver-port, after user-supervisor), and bob-cli-8o (ref-id-allocation), with one reviewer decision (multivisor_web_access, default tailnet) and the verbatim continuation contract. Ranking: security first (au, av, aw), backup content loss next (1a), then the top silent identity defect (8o, chosen over 9a on age and live-vault impact). Next candidates: 9a, 8a, 79, al, 2q, ax; heavily corroborated 6m, 6v, 6w, 7i; detection 8r, 9x. The backlog campaign is not complete.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-an.1](bob-cli-an.1.md) | Secure Athena supervisor control and its executable chain | ✓ closed | medium | 2026-10-21 | 1 | 0 |
| [bob-cli-an.2](bob-cli-an.2.md) | Remove user-writable code from root hourly jobs | ✓ closed | medium | 2026-10-21 | 1 | 0 |
| [bob-cli-an.3](bob-cli-an.3.md) | Restrict monitoring endpoints to verified clients | ✓ closed | medium | 2026-10-21 | 1 | 0 |
| [bob-cli-an.4](bob-cli-an.4.md) | Preserve ignored vault content off host | ✓ closed | medium | 2026-10-21 | 1 | 1 |
| [bob-cli-an.5](bob-cli-an.5.md) | Preserve highlight IDs across annotation insertion | ✓ closed | medium | 2026-10-21 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-an: Backlog batch 1: Athena security and vault durability [closed]"]
    n1["bob-cli-an.1: Secure Athena supervisor control and its executable chain [closed]"]
    n2["bob-cli-an.2: Remove user-writable code from root hourly jobs [closed]"]
    n3["bob-cli-an.3: Restrict monitoring endpoints to verified clients [closed]"]
    n4["bob-cli-an.4: Preserve ignored vault content off host [closed]"]
    n5["bob-cli-an.5: Preserve highlight IDs across annotation insertion [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n2 -.-> n3
    n2 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.1.md) | [bob-cli-an.1](bob-cli-an.1.md) | 0 |
| [bbugyi200.athena.bob-cli-an.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.2.md) | [bob-cli-an.2](bob-cli-an.2.md) | 0 |
| [bbugyi200.athena.bob-cli-an.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.3.md) | [bob-cli-an.3](bob-cli-an.3.md) | 0 |
| [bbugyi200.athena.bob-cli-an.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.4/README.md) | [bob-cli-an.4](bob-cli-an.4.md) | 1 |
| [bbugyi200.athena.bob-cli-an.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.5/README.md) | [bob-cli-an.5](bob-cli-an.5.md) | 1 |
| [bbugyi200.athena.bob-cli-an.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.land/README.md) | [bob-cli-an](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`51ad4f4`](https://github.com/bobs-org/bob-cli/commit/51ad4f4c77a318519b2039dc1e743ec9c737304f) | feat(highlights-ref): stabilize highlight IDs across sidecar order | [bob-cli-an.5](bob-cli-an.5.md) | 2026-10-21 13:47:57 EDT |
| bob-cli | [`019ffb5`](https://github.com/bobs-org/bob-cli/commit/019ffb5ac4ee1b122fc3a576509acf774a80cf31) | docs(vault-sync): document authored content coverage for vault git backup | [bob-cli-an.4](bob-cli-an.4.md) | 2026-10-22 06:58:44 EDT |
| bob-cli | [`e860379`](https://github.com/bobs-org/bob-cli/commit/e860379a3561eaa400275365ce6788226388aaf9) | docs(vault-sync): justify the gkeep migrate-tasks receipt exclusion | [bob-cli-an](README.md) | 2026-10-23 12:37:43 EDT |
| bob-cli--plans | [`bob-cli--plans@9e07e1b`](https://github.com/bobs-org/bob-cli--plans/commit/9e07e1b059fc04f940022bcf0a0fb2ba0325e265) | chore(backlog): mark batch 1 security and durability plan done | [bob-cli-an](README.md) | 2026-10-23 12:39:25 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.1--3][1] | Verify the parent epic remains open after closing its phase | 1 |
| read-by | [agent:bob-cli-an.4][2] | Need epic context for phase an.4 | 2 |
| read-by | [agent:bob-cli-an.5][3] | Need parent epic context and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.5/README.md

<!-- sase:referenced-by:end -->
