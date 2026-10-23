# Bead: bob-cli-an.6.1 — Move daily, weekly, and monthly root cron onto root-owned code

[Bead Pages](../README.md) / [bob-cli-an.6](bob-cli-an.6.md) / bob-cli-an.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md) · **Assignee:** `bob-cli-an.6.1` · **Size:** medium
**Created:** 2026-10-23 12:41:09 EDT · **Closed:** 2026-10-23 14:22:34 EDT
**Plan:** [202610/backlog\_batch2\_athena\_hardening\_and\_ref\_ids.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md)

## Description

periodic-cron: resolve bob-cli-au by extending the reviewed tailnet root-cron installation to every daily, weekly, and monthly root entrypoint and verifying their complete executable chains.

## Notes

[2026-10-23T17:05:26Z · bob-cli-an.6.1] Baseline 2026-10-23 as bryan: /etc/cron.{daily,weekly,monthly} 5 entrypoints are symlinks to bryan:bryan 0755 files (daily_jobs, daily_backup, weekly_jobs, weekly_backup, monthly_backup); live hourly pair byte-identical to tailnet hosts/athena/root-cron (dbb7368). Chain: backup tiers source bryan backup.sh; jobs tiers source bryan jobs.sh which sources $HOME/.profile (anacron sets HOME=/home/bryan, so root sources bryan profile as root) and evals bryan-PATH helpers; clean_filesystem self-escalates via sudo. sudo requires password (sudo -l prompts; 00-bryan-password-required), so jobs die at first sudo under cron (daily log shows only chown_log_files started). Hourly marker 8.5h stale, daily 5.5d, weekly 27.5d, monthly 183.5d: freshness is bob-cli-1a scope, verifier reports it without failing.

[2026-10-23T17:05:37Z · bob-cli-an.6.1] Prepared fix in tailnet hosts/athena/root-cron (uncommitted, same-turn commit via final declaration): 3 hardened backup entrypoints (logic byte-identical to bryan originals modulo env pinning, absolute lib source, #!/usr/bin/bash normalization); 2 drop-priv wrappers (root runs only bash+sudo -u bryan; vendoring rejected as wider trust surface; user-crontab rejected: loses anacron catch-up/logs/mail). Installer/verifier/exercise extended to 7 entrypoints + 4 tiers; verifier checks wrapper drop-only shape with tamper negative controls; rotation staleness informational (bob-cli-1a/6.2 owns advancement). Nonpriv validation all green: bash -n x9, py_compile x3, pre-install verifier exit 1 with exactly the 15 expected FAILs (5 symlinks x entrypoint/content/denial), content probes 5/5 PASS with 3/3 negative rejections, scratch backup tiers exit 0 with rotations (incl forced-January yearly), sim install/reinstall/rollback + both baseline guards verified. Remaining: privileged gate (install, verify incl nobody probes, run-parts x4, exercise), then close.

[2026-10-23T17:42:21Z · bob-cli-an.6.1--1] Gate ledger (sudo-08f73598, approved): install ran, exit 1 with 80/83 verifier checks passing. All 80 cover the phase contract: 7 entrypoints root-owned non-symlink with safe parents, libdir/lib files, hardened/wrapper content incl negative-control shapes, tools+PATH dirs, run-parts lists all 7 across 4 tiers, exporter fresh, hourly marker stale-informational, hourly newest root-owned, bryan+nobody denial probes all denied. The only 3 FAILs were live daily/weekly/monthly rotation newest-dir ownership. Diagnosis: (1) verifier scope leak -- rotation-output ownership is not a root-executed part, so it cannot fail this phases acceptance (no root-executed part bryan-replaceable; scheduler lists all tiers); advancement/provenance is bob-cli-1a, owned by phase 6.2. (2) Those 3 newest dirs are pre-change fixture stubs run as bryan today 12:54/12:59/13:03 (each holds only probe.txt=/home plus fresh backup.txt); real data intact at -2 (daily-2 Oct18, weekly-2 Sep26, monthly-2 Apr23 -- the plan-evidence dates). Fix in tailnet source (uncommitted, same-turn commit via final declaration): verify_root_cron.py reports newest-rotation ownership instead of failing it (docstring/comment/README updated); installer untouched and its baseline guard accepts current live state (new files carry bob-cli-an.6.1, hourly carry bob-cli-an.2). Nonpriv re-validation all green: bash -n x9, py_compile x3, verifier-as-bryan exit 0 73/73 (nobody probes SKIP without root, as designed), scratch exercise --scratch-only exit 0 with daily/weekly/monthly rotations committed incl forced-January yearly branch. Ready for re-gate with the unchanged README 7-command batch (install, verify, exercise, schedule x4); bead stays open until that gate lands.

[2026-10-23T17:42:30Z · bob-cli-an.6.1--1] PROPOSED FOLLOW-UP: phase bob-cli-an.6.2 (backup-rotation) must clean up fixture stubs at /mnt/hercules/backup/home/daily, weekly, monthly newest (bryan-owned, contain only probe.txt + today backup.txt from pre-change fixture runs as bryan) and restore the rotation chains from -2 (which hold the real Oct18/Sep26/Apr23 newest) before proving scheduled advancement, or its advancement proof will rotate fixture content and destroy the real newest; also note /mnt/hercules/backup and /mnt/hercules/backup/home parents are bryan-owned, which the verifier does not check.

[2026-10-23T18:04:47Z · bob-cli-an.6.1] Continuation review: source landed as tailnet 642c4fe and all 9 installed payloads match; non-root verifier passes 73/73. Found acceptance harness ran Bryan-owned originals directly as root, so replacing it with scratch UID/argument/exit probes. Also reproduced Bash arithmetic command execution from a crafted backup.txt value (no live mutation); backup root and home parent are Bryan-owned, making markers replaceable. Closing this remaining root-executed input path in backup.sh with timestamp validation and fail-closed destination checks; phase 6.2 should preserve these security guards when changing rsync exit handling.

[2026-10-23T18:13:54Z · bob-cli-an.6.1] Prepared continuation fix in tailnet hosts/athena/root-cron: backup.sh validates bounded decimal timestamp data before arithmetic and refuses writable root destination ancestors or symlinked rotation/staging paths; installer protects backup root as root:bryan 0750 and ten system category parents as root:root 0755, preserving contents and personal child directories, and now backs up/restores helper files on rollback. Verifier includes exact installed/source parity, backup-parent metadata, and denial probes. Exercise uses scratch UID/argument/exit probes (never executes Bryan-owned originals), no longer runs live backup, and verifies fixture bytes in all four backup tiers. Validation: unittest 10 PASS + 1 root-only SKIP, bash -n all 9 payloads, Python syntax all modules, git diff --check, scratch daily/weekly/monthly/yearly PASS. Current verifier expected 103/108: 1 pending helper update, 2 writable backup parents, 2 matching denial failures. No epic symbols. Remaining: reviewed sudo batch install + root tests + safe exercise + verifier + run-parts x4, then close ONLY this phase. Phase 6.2 still owns preexisting fixture cleanup and rsync-24/freshness; retain the new root-boundary guards.

[2026-10-23T18:22:34Z · bob-cli-an.6.1--1] Verified approved sudo gate sudo-2ef446df-5e84-45d5-bc44-5f893a750d53 (manifest sha256 22a531894460dad39a58dd5313ef7f4a7ec39c4effdc0acc598a32fbbdd87a72): all 8 commands ran with exit 0. All 11 boundary regressions passed including root refusal of writable/user-owned parents, timestamp injection and symlink guards, strict wrapper validation, and entry/helper rollback. Install and final root verification each passed 132/132 checks including all 9 source/live payload comparisons, protected executable and backup parents, and real bryan/nobody write denial. Safe exercise passed collector refresh, restore sample, both wrappers uid=1000 with preserved arguments and exit 37, and daily/weekly/monthly/yearly scratch rotations; no live backup rotations or user-owned originals were executed. run-parts lists all 7 entries across 4 tiers. Continuation recheck passed 108/108 as bryan with nobody skipped as expected, all 9 payloads still byte-identical; git diff --check passed. No epic-symbol entries. Tailnet continuation source and tests are included in the SASE final declaration after existing implementation commit 642c4fe. Phase 6.2 retains fixture-stub cleanup and rsync-24/rotation freshness, preserving these security guards; backup parents are now protected. Only this phase is closed; bob-cli-au and ancestors remain for the lander.

## Dependencies

- **Blocks:** [bob-cli-an.6.2](bob-cli-an.6.2.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.1.md) | [bob-cli-an.6.1](bob-cli-an.6.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.1--1][1] | Need latest phase scope, decisions, design, and remaining acceptance notes | 3 |
| read-by | [agent:bob-cli-an.6.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.land/README.md

<!-- sase:referenced-by:end -->
