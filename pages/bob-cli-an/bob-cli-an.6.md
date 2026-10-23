# Bead: bob-cli-an.6 — Backlog batch 2: Athena root, listener, and backup hardening plus reference ID allocation

[Bead Pages](../README.md) / [bob-cli-an](README.md) / bob-cli-an.6

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md) · **Assignee:** `bob-cli-an.6.land`
**Created:** 2026-10-23 12:41:09 EDT
**Plan:** [202610/backlog\_batch2\_athena\_hardening\_and\_ref\_ids.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch2_athena_hardening_and_ref_ids.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md

<!-- sase:links:end -->

## Description

Close five prioritized task beads by removing the remaining Bryan-to-root cron chains, committing hourly-tier backup rotations despite benign rsync churn, restricting Athena's remaining wildcard control listeners, and making new reference IDs follow their stems without cross-type collisions. The lander continues the backlog through further epics of at most five phases and five task beads until every project task bead is closed.

## Notes

[2026-10-23T21:12:55Z · bob-cli-an.6.land] LANDER FOLLOW-UP TRIAGE (bob-cli-an.6.land): (1) 6.1 #4 fixture stubs + bryan-owned backup parents: DECLINED as already addressed; 6.2 restore-stubs quarantined the stubs under /var/backups/bob-cli-an.6.2/stub-rotations and restored real daily/weekly/monthly from -2, and 6.1 #6 made the installer protect /mnt/hercules/backup (root:bryan 0750) and its category parents; verifier now checks both. (2) 6.2 #3 confirm daily/weekly/monthly advance: no duplicate; CREATED bob-cli-b2 (medium). Daily/weekly first run after install is 2026-10-24 ~01:00 EDT and monthly ~2026-11-21; their own failure cause was never observed (anacron mails go to Gmail; gog token expired). (3) 6.2 #3 optional summarize_backup_mail.py CODE_RE over-count: epic-introduced, FIXED by the lander in tailnet (match rsync's '(code N)' only). (4) 6.4 #1 rfserver X-Forwarded-For trust: CREATED bob-cli-b3 (small). (5) 6.5 #1 six undocumented BOB_REF_* controls: DECLINED as resolved; bob-docs lint passes on 7e3bdb2e (134016ce documented them). Lander discoveries: Multivisor web UI GET / returns 500 TemplateNotFound in the 2025 pipx install (API 401 fine), CREATED bob-cli-b4 (medium). master CI red at just check-scripts (coordination self-test pre-sync commit lacks git identity on the runner; root cause confirmed in script lines 133-153), CREATED bob-cli-b5 (small ci). just docs-check generated drift docs/develop/decisions.md, CREATED bob-cli-b6 (xsmall ci). bob-mac-capture CI red on 1c35b30 and 6e1f84c, the same 3 RefsLibraryTests scan tests, CREATED bob-cli-b7 (medium ci). bob-cli-8o note #1 optional doctor id/stem check plus live data (1 duplicate id and 3 id/stem mismatches found by a read-only ~/bob/ref scan), CREATED bob-cli-b8 (medium feature). b5-b7 originate in closed epic bob-cli-at, not this epic. Epic-caused remainder fixed by the lander: phase 6.4 left no durable tailnet record of its uncommitted ~/db/bin rfserver edit or its /etc/environment change. Added tailnet hosts/athena/rfserver/ (README with client matrix, apply/verify/rollback steps, server-loopback.patch, and a copy of the boundary test), corrected the stale 23401 sentence in the monitoring README, and refreshed the tailnet README index for the all-tier root-cron chain and rfserver.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.land/README.md) | [bob-cli-an.6](bob-cli-an.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.1--1][1] | need epic scope for 6.1 vs 6.2 split | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.1.md

<!-- sase:referenced-by:end -->
