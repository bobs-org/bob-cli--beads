# Bead: bob-cli-ib.6 — Move athena and Mac jobs into the data and cut over

[Bead Pages](../README.md) / [bob-cli-ib](README.md) / bob-cli-ib.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5w.linker.w1.md) · **Assignee:** `bob-cli-ib.6` · **Size:** medium
**Created:** 2026-11-07 12:43:37 EST · **Closed:** 2026-11-07 15:54:17 EST
**Plan:** [202611/crontab\_as\_code.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/crontab_as_code.md)

## Description

migrate: move the live athena and Mac jobs into cron: data with an atomic cutover, update bob-cli docs, and converge the fleet through a post-commit apply.

## Notes

[2026-11-07T20:53:14Z · bob-cli-ib.6] PROPOSED FOLLOW-UP: delete cron.retire from the chezmoi home/.chezmoidata.yaml once `cronctl status --all` prints `cron.retire can be deleted` — it holds 12 legacy athena lines and 3 legacy mac lines; the mac entries stay live until the Mac applies (it is often asleep).

[2026-11-07T20:53:18Z · bob-cli-ib.6] PROPOSED FOLLOW-UP: upgrade athena chezmoi from v2.13.1 (~/.nix-profile/bin/chezmoi), then move the cron: data from home/.chezmoidata.yaml to home/.chezmoidata/cron.yaml — v2.13.1 is the fleet floor that forced the single-file data and whole-output partials.

[2026-11-07T20:53:22Z · bob-cli-ib.6] PROPOSED FOLLOW-UP: remove apollo duplicate ~/go/bin/chezmoi dev build — apollo carries both ~/bin/chezmoi (v2.70.2) and ~/go/bin/chezmoi (dev), and cronctl discovery probes ~/bin before ~/go/bin.

[2026-11-07T20:53:26Z · bob-cli-ib.6] PROPOSED FOLLOW-UP: make the sase epic watchdog (e.g. ~/.local/state/sase-epic-watchdog/sase-1r2/watchdog.sh) derive XDG_RUNTIME_DIR/DBUS_SESSION_BUS_ADDRESS itself — retiring athena legacy DISPLAY/DBUS/XDG crontab env lines (per plan) means watchdog lines below the managed block now get only cron defaults plus MAILTO, so a post-reboot `sase bead work -y` relaunch may lose systemd-run --user scope escaping; owned by the sase project, not bob-cli.

[2026-11-07T20:53:30Z · bob-cli-ib.6] PROPOSED FOLLOW-UP: chezmoi tests/bash/poseidon_chezmoi_isolation_test.sh still fails the same 2 cases ("Mac ignores poseidon files", "Cargo config renders only on athena") on the clean base 16701bfa; already recorded by bob-cli-ib.4 and bob-cli-ib.5, no task bead yet; all other 432 bashunit tests pass with this phase.

[2026-11-07T20:54:17Z · bob-cli-ib.6] Verified: chezmoi home/.chezmoidata.yaml cron: now holds athena jobs bob-nightly + pass-git-sync (enabled) and tman + init-bg (enabled: false), mac jobs bob-highlights-sync/bob-projects-sync/bob-task-reconcile on the documented :00/:05/:10 stagger with --retry-timeout 120 (decision mac_schedule=documented), and cron.retire with 12 athena + 3 mac legacy lines copied from fresh crontab -l / ssh mac crontab -l (decision cutover=retire; watchdog line excluded). cronctl check --source ok (3 machines, 7 jobs, crontab -n syntax check); diff athena/mac --source show every legacy job retired in the same install that adds its managed line, watchdog kept; sync --dry-run --block/--retire preview of athena removes exactly the 12 lines; render byte-identical on chezmoi v2.13.1 and v2.70.2; cronrun --dry-run resolves all 5 enabled jobs (athena locally under env -i, mac over SSH); mac bob task reconcile --help lists --retry-timeout. bob-cli docs: vault-git-sync.md Mac scheduled maintenance rewritten (cron: data source, cronctl status/diff/logs, /crontab flow, cronrun failure-only mail; no hand-install claim, crontab - procedure, or /var/tmp paths), plus minimal fixes in task-status-hooks.md and obsidian-sync-exclusions.md; just docs-check passed. chezmoi just lint + fmt-check green; just test-bash 432/434 with the 2 poseidon_chezmoi_isolation failures reproducing identically on the clean base (recorded as follow-up). Post-commit convergence staged as monitor n7hy5x: checkout cronctl apply athena apollo mac, with a follow-up that runs status --all and reports.

## Dependencies

- **Depends on:** [bob-cli-ib.2](bob-cli-ib.2.md) ✓ · ⧖ 2026-11-07
- **Depends on:** [bob-cli-ib.4](bob-cli-ib.4.md) ✓ · ⧖ 2026-11-07
- **Depends on:** [bob-cli-ib.5](bob-cli-ib.5.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ib.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.6.md) | [bob-cli-ib.6](bob-cli-ib.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`591bde8`](https://github.com/bobs-org/bob-cli/commit/591bde8dc82b4aacc08ad511602434b57d29cb0b) | docs(cron): point Mac scheduled maintenance at the chezmoi cron: data | [bob-cli-ib.6](bob-cli-ib.6.md) | 2026-11-07 15:55:07 EST |
| chezmoi | [`chezmoi@6af21b4`](https://github.com/bbugyi200/dotfiles/commit/6af21b405fa1b0888f169c0908ef9c0340baf4a0) | feat(cron): migrate athena and Mac jobs into cron: data | [bob-cli-ib.6](bob-cli-ib.6.md) | 2026-11-07 15:55:32 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ib.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.land.md

<!-- sase:referenced-by:end -->
