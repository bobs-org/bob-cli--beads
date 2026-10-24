# Bead: bob-cli-an.6 — Backlog batch 2: Athena root, listener, and backup hardening plus reference ID allocation

[Bead Pages](../README.md) / [bob-cli-an](README.md) / bob-cli-an.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md) · **Assignee:** `bob-cli-an.6.land`
**Created:** 2026-10-23 12:41:09 EDT · **Closed:** 2026-10-23 17:19:59 EDT
**Plan:** [202610/backlog\_batch2\_athena\_hardening\_and\_ref\_ids.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch2_athena_hardening_and_ref_ids.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md

<!-- sase:links:end -->

## Description

Close five prioritized task beads by removing the remaining Bryan-to-root cron chains, committing hourly-tier backup rotations despite benign rsync churn, restricting Athena's remaining wildcard control listeners, and making new reference IDs follow their stems without cross-type collisions. The lander continues the backlog through further epics of at most five phases and five task beads until every project task bead is closed.

## Notes

[2026-10-23T21:12:55Z · bob-cli-an.6.land] LANDER FOLLOW-UP TRIAGE (bob-cli-an.6.land): (1) 6.1 #4 fixture stubs + bryan-owned backup parents: DECLINED as already addressed; 6.2 restore-stubs quarantined the stubs under /var/backups/bob-cli-an.6.2/stub-rotations and restored real daily/weekly/monthly from -2, and 6.1 #6 made the installer protect /mnt/hercules/backup (root:bryan 0750) and its category parents; verifier now checks both. (2) 6.2 #3 confirm daily/weekly/monthly advance: no duplicate; CREATED bob-cli-b2 (medium). Daily/weekly first run after install is 2026-10-24 ~01:00 EDT and monthly ~2026-11-21; their own failure cause was never observed (anacron mails go to Gmail; gog token expired). (3) 6.2 #3 optional summarize_backup_mail.py CODE_RE over-count: epic-introduced, FIXED by the lander in tailnet (match rsync's '(code N)' only). (4) 6.4 #1 rfserver X-Forwarded-For trust: CREATED bob-cli-b3 (small). (5) 6.5 #1 six undocumented BOB_REF_* controls: DECLINED as resolved; bob-docs lint passes on 7e3bdb2e (134016ce documented them). Lander discoveries: Multivisor web UI GET / returns 500 TemplateNotFound in the 2025 pipx install (API 401 fine), CREATED bob-cli-b4 (medium). master CI red at just check-scripts (coordination self-test pre-sync commit lacks git identity on the runner; root cause confirmed in script lines 133-153), CREATED bob-cli-b5 (small ci). just docs-check generated drift docs/develop/decisions.md, CREATED bob-cli-b6 (xsmall ci). bob-mac-capture CI red on 1c35b30 and 6e1f84c, the same 3 RefsLibraryTests scan tests, CREATED bob-cli-b7 (medium ci). bob-cli-8o note #1 optional doctor id/stem check plus live data (1 duplicate id and 3 id/stem mismatches found by a read-only ~/bob/ref scan), CREATED bob-cli-b8 (medium feature). b5-b7 originate in closed epic bob-cli-at, not this epic. Epic-caused remainder fixed by the lander: phase 6.4 left no durable tailnet record of its uncommitted ~/db/bin rfserver edit or its /etc/environment change. Added tailnet hosts/athena/rfserver/ (README with client matrix, apply/verify/rollback steps, server-loopback.patch, and a copy of the boundary test), corrected the stale 23401 sentence in the monitoring README, and refreshed the tailnet README index for the all-tier root-cron chain and rfserver.

[2026-10-23T21:19:59Z · bob-cli-an.6.land] Landing verified (bob-cli-an.6.land, 2026-10-23). All five phases are closed, and their tasks were closed with live evidence: au, av, aw, 1a, and 8o. ROOT CRON (au): every hourly, daily, weekly, and monthly entrypoint is a root-owned regular file from tailnet 642c4fe/1055f2f. The lander's verify_root_cron.py as bryan passed 105/105, with all payloads byte-identical to source and every bryan write/create denied; gate sudo-2ef446df passed 132/132 plus the nobody probes. BACKUP (1a): backup.sh from tailnet 0d0e2dd commits on rsync 24 and keeps 23 and other codes fatal. Two consecutive scheduled hourly commits (gap 3604s) were followed by a fresh marker at 16:43, and a restore sample matches. Daily, weekly, and monthly have not run since the install, so confirming them is filed as bob-cli-b2. LISTENERS (av, aw): from apollo, 8052 and 23401 are refused on the tailnet, and 8052, 8100, and 23401 are filtered on the WAN. 8100 is tailnet-only per decision multivisor_web_access=tailnet; the nft table and unit are byte-identical to tailnet c785507 and the unit is active and enabled. verify_user_supervisor.py exits 0 (authenticated control of root and user supervisors). rfserver binds 127.0.0.1:23401, loopback bad-token POST returns 401, and the boundary test passes. REF IDS (8o): 9885bde1 makes the id follow the output stem, and the collision walk spans every type directory plus recorded ids across ref/. Its CI is green; the lander's just check on integrated master 134016ce exits 0, and bob-docs lint passes. INTEGRATION: post-start commits 0aec807c, cd4bc7a0, faa9a757, 134016ce, and 7e3bdb2e (bob-cli-at) do not touch id allocation or conflict with it. Their red CI and generated docs drift were routed as b5, b6, and b7. EPIC-CAUSED REMAINDER FIXED: phase 6.4 had no durable rfserver record, so the lander added tailnet 05c6a5b (hosts/athena/rfserver README, patch, and test copy; monitoring README; index rows) and fixed the summarize_backup_mail CODE_RE over-count. FOLLOW-UPS: created b2, b3, b4, b5, b6, b7, and b8; declined 6.1 #4 as already addressed and 6.5 #1 as already resolved (see triage note). SWEEP: 23 tasks closed as resolved with evidence; uncertain findings are recorded on 3h, 4o, 73, 91, and 5m, and the snooze prerequisites on 3o (met) and 6q (not met). No epic symbols.

[2026-10-23T21:25:58Z · bob-cli-an.6.land] CONTINUATION (bob-cli-an.6.land, 2026-10-23): a fresh enumeration after landing and the obsolescence sweep found 138 unresolved tasks: 134 ready and 4 snoozed (3o with its prerequisite met; 6q, aa, and ah not met). None are claimed or in progress. The successor epic 'Backlog batch 3: rfserver suspension, backup tier freshness, Eastern day boundary, web-clip quote fidelity, and relative ref paths' was authored and validated, and is being submitted through sase plan propose (scratch sase_plan_backlog_batch3_rfserver_backups_day_zone_webclip_fonts_ref_paths.md). It owns exactly bob-cli-b3 (rfserver-suspension), bob-cli-b2 (backup-tier-freshness), bob-cli-2q (day-timezone), bob-cli-85 (webclip-static-fonts), and bob-cli-9a (ref-relative-paths), all independent. It carries one reviewer decision (day_timezone, default config) and the verbatim continuation contract. Ranking: security (b3), content loss (b2), then silent corruption by reach and corroboration (2q, 85, 9a). Deferred with reasons: 7q is a design change to the accepted capture-link-drops-blocking-deps decision; 4r now affects only 2 color-grouped notes; the CI blockers b5, b6, and b7 have their own triage gates. Next candidates: 8a, al, 4r, 79, and b8; CI b5, b6, and b7; corroborated 7i, 6v, 3w, and 5l; Athena b4, 8r, and 9x. The backlog campaign is not complete.

[2026-10-24T11:29:35Z · bob-cli-an.6.6.6.land] RECHECK after descendant bob-cli-an.6.6.6 closed (2026-10-24). an.6.6 and an.6.6.6 are closed; epic-symbols empty; linked plan 202610/backlog_batch2_athena_hardening_and_ref_ids.md already status: done. No unfinished descendants. Parent stays closed. Backlog campaign continues.

[2026-10-24T11:29:47Z · bob-cli-an.6.6.6.land] Rechecked after descendant an.6.6.6 closed; already done.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md) | [bob-cli-an.6](bob-cli-an.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@47ac730`](https://github.com/bobs-org/bob-cli--plans/commit/47ac7305e366d008043dfae4dfa40043b8e59b8b) | chore(plans): mark backlog\_batch2\_athena\_hardening\_and\_ref\_ids done | [bob-cli-an.6](bob-cli-an.6.md) | 2026-10-23 17:25:11 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.1--1][1] | need epic scope for 6.1 vs 6.2 split | 1 |
| read-by | [agent:bob-cli-an.6.6.land][2] | Need the parent landing notes | 2 |
| read-by | [agent:bob-cli-an.6.land][3] | Need the epic scope, children, and linked plan file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md

<!-- sase:referenced-by:end -->
