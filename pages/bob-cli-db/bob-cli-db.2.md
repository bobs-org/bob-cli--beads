# Bead: bob-cli-db.2 — Split the live JOB blocks and add WRITE

[Bead Pages](../README.md) / [bob-cli-db](README.md) / bob-cli-db.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ar.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ar.w0.md) · **Assignee:** `bob-cli-db.2` · **Size:** small
**Created:** 2026-10-27 17:11:11 EDT · **Closed:** 2026-10-27 18:01:26 EDT
**Plan:** [202610/write\_theme\_and\_job\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/write_theme_and_job_split.md)

## Description

vault_migrate: hide JOB, split its 89 blocks with the planned mapping in one vault commit, pin WRITE (and the standing set), and verify list, stats, and sync.

## Notes

[2026-10-27T22:01:26Z · bob-cli-db.2] Hid JOB, split all 89 live JOB entries in vault commit 542b61da (bob themes split: JOB → BUILD, CHORE, PLAN, READ, WRITE) with unmapped 0 kept 0 remaining 0: READ 37, CHORE 23, WRITE 17, PLAN 10 (exempt), BUILD 2. No added or dropped mapping rows (2026-10-27 open row moved L64→L68). Pinned WRITE magenta, BUILD yellow, READ green, FIX blue, CHORE aqua. Verified: themes list -a -f json has JOB absent, WRITE magenta pinned visible (17 entries), renamed_reappeared empty, no WRITE hue collision; stats worked 2026-10-01..2026-10-27 total 6720m unchanged (theme split only); vault-sync post-sync ok (split sha 542b61da local=remote, then journal pin commit 4e5f16a5). Undo: git -C ~/bob revert 542b61da && bob vault-sync; then bob themes unhide JOB and bob themes color NAME auto. epic-symbols empty. No bob-cli file changes.

## Dependencies

- **Depends on:** [bob-cli-db.1](bob-cli-db.1.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-db.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-db.2/README.md) | [bob-cli-db.2](bob-cli-db.2.md) | 0 |
