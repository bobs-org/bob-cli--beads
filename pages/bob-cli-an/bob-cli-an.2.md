# Bead: bob-cli-an.2 — Remove user-writable code from root hourly jobs

[Bead Pages](../README.md) / [bob-cli-an](README.md) / bob-cli-an.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12v.md) · **Assignee:** `bob-cli-an.2` · **Size:** medium
**Created:** 2026-10-21 12:58:23 EDT · **Closed:** 2026-10-22 06:39:21 EDT
**Plan:** [202610/backlog\_security\_and\_durability.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_security_and_durability.md)

## Description

root-cron: resolve bob-cli-96 while preserving hourly jobs and backups and verifying their complete executable chains.

## Notes

[2026-10-21T22:32:36Z · bob-cli-an.2] Baseline (2026-10-21, as bryan on athena): /etc/cron.hourly/hourly_jobs and hourly_backup are root-owned symlinks resolving to bryan:bryan 0755 /home/bryan/db/bin/cron.jobs/cron.hourly/* (sha256 1a58a0eb... / ad286761...). Full chain inventoried: hourly_jobs execs bryan-owned prometheus_disk_space_textfile (fbf780f4...), hourly_backup sources bryan-owned backup.sh (fa5c49b0...); interpreters (/usr/bin/bash), rsync, and all PATH helpers are root-owned; /var/lib/prometheus/node-exporter is root:root 0755 (collector genuinely needs root); backup destination /mnt/hercules/backup is bryan:bryan 700 with root-owned rotations, source /home needs root for full read, so both jobs stay on root (user-crontab move would silently narrow coverage). Pre-change verifier run exits 1: both entrypoints FAIL as symlinks, bryan can open both for writing (proves bob-cli-96).

[2026-10-21T22:32:44Z · bob-cli-an.2] Prepared fix (tailnet repo, hosts/athena/root-cron/): /etc/cron.hourly entries become regular root:root 0755 files pinning PATH and sourcing /usr/local/lib/athena-cron/{backup.sh,prometheus_disk_space_textfile} by absolute path; lib is a reviewed copy with only hardening diffs (pinned #!/usr/bin/bash, PATH export, RSYNC=/usr/bin/rsync, absolute /usr/bin/sudo; rotation/filter/atomic-mv behavior byte-identical per diff). install_root_cron.py (root-only, baseline-guarded, atomic replace, manifest under /var/backups/bob-cli-an.2/, --rollback restores pre-change state into the backup dir) runs verify_root_cron.py itself post-install. Non-priv validation done: bash -n x4, py_compile x2, installer baseline/validate_payload OK and refuses non-root, sim install/rollback/reinstall incl. same-second backups and cron-dir cleanliness, scratch backup (2 runs, rotation+hardlinks, exit 0), scratch collector (exit 0, correct prom format). Remaining: privileged gate (install, verify incl. nobody probes, run-parts --test, live exercise of both entrypoints, restore-sample cmp) then close this phase; task bob-cli-96 stays open for the lander.

[2026-10-21T22:32:48Z · bob-cli-an.2] PROPOSED FOLLOW-UP: /etc/cron.daily, weekly, and monthly contain the same bryan-symlink shape (daily_backup, daily_jobs, weekly_backup, weekly_jobs) executing as root; this phase migrates only the two hourly chains per bob-cli-96 scope.

[2026-10-21T22:44:33Z · bob-cli-an.2] Cautionary evidence (2026-10-21): an exercise dry-run as bryan accidentally executed the LIVE hourly_backup chain (not a scratch copy) against the real BACKUP_DIR. It failed safe exactly as designed for non-root: every destructive op hit Permission denied, exit 1, zero rotation changes (hourly/backup.txt still 1792617853, rotation mtimes untouched). This independently proves the backup genuinely requires root and cannot move to a user crontab. Side effect was limited to throwaway .hourly staging (91 bryan-owned partial entries); cleaned unprivileged via chmod+rm, staging dir now absent, rotations verified intact. Lesson recorded: validate backup logic only with overridden BACKUP_DIR (done, exit 0) or as root post-install.

[2026-10-22T10:30:02Z · bob-cli-an.2--2] Validation (2026-10-22, athena, as bryan): gate sudo-226fbe88 ledger = install exit 0 (46/46), verify exit 0 (46/46 incl. bryan+nobody denial probes), schedule lists both jobs. Live now: /etc/cron.hourly files byte-identical to tailnet hosts/athena/root-cron source, run-parts lists both, exporter fresh (~590s), hourly marker fresh (~274s, root-owned rotations), non-priv verify 41/41 (nobody probes SKIP as bryan). exercise exit 2: COLLECTOR 0, BACKUP 16 (rsync vanished-file code 24 on active .sase scratch + rm staging race during 344s full /home backup), RESTORE_SAMPLE_OK. Backup logic is byte-identical to pre-change baseline (hardening only), so this is the pre-existing bob-cli-1a exit-24 flake, not a hardening regression; regular hourly runs since succeed (marker fresh). Re-exercise now hits TOO_SOON guard (marker <30min) for fast EXERCISE_OK via gate.

[2026-10-22T10:30:06Z · bob-cli-an.2--2] PROPOSED FOLLOW-UP: treat rsync exit 24 (vanished files) as warning-not-fatal in backup.sh so hourly /home rotations commit instead of discarding on active-tree churn — detail: exercise BACKUP exit 16 driven by rsync code 24 on short-lived .sase scratch files plus an rm staging race; restore sample still matched; cites canceled bob-cli-1a; explicitly out of this phase scope (byte-identical rotation behavior preserved per bob-cli-96).

[2026-10-22T10:39:10Z · bob-cli-an.2--3] Validation (2026-10-22, bob-cli-an.2--3 close): gate sudo-0822b975 ledger exercise exit 0 EXERCISE_OK (COLLECTOR 0, BACKUP 1 TOO_SOON guard 663s since last hourly), verify-after exit 0 46/46 incl bryan+nobody denial probes; non-priv re-verify 41/41 (nobody SKIP as bryan), schedule run-parts lists both jobs, live /etc/cron.hourly + /usr/local/lib/athena-cron byte-identical to tailnet hosts/athena/root-cron source, exporter fresh 0s and backup marker fresh 662s at gate time.

[2026-10-22T10:39:21Z · bob-cli-an.2--3] install exit 0 46/46, verify exit 0 46/46 incl bryan+nobody denial probes, schedule lists both hourly jobs, exercise EXERCISE_OK (collector 0, backup 1 TOO_SOON guard), verify-after 46/46, live files byte-identical to tailnet source, exporter and backup marker fresh

## Dependencies

- **Depends on:** [bob-cli-an.1](bob-cli-an.1.md) ✓ · ⧖ 2026-10-21
- **Blocks:** [bob-cli-an.3](bob-cli-an.3.md) ✓ · ⧖ 2026-10-21
- **Blocks:** [bob-cli-an.4](bob-cli-an.4.md) ✓ · ⧖ 2026-10-21

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.2--3][1] | Need phase scope | 1 |
| read-by | [agent:bob-cli-an.4][2] | Need prior phase pattern | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.land--2][3] | Review every ancestor phase note for unresolved follow-ups and completion | 1 |
| read-by | [agent:bob-cli-an.land][4] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md

<!-- sase:referenced-by:end -->
